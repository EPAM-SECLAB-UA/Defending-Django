
# Резюме: Безпечна конфігурація Django за зворотним проксі-сервером

## Основна проблема

Django не бачить безпосереднього HTTPS-з'єднання клієнта і покладається на заголовки від проксі-сервера (наприклад, `X-Forwarded-Proto`), щоб визначити, чи запит безпечний. Якщо ці сигнали неправильні або підроблені, Django можна обдурити.

## Типові проблеми

**1. Підробка заголовків**
- Зловмисники можуть підробити `X-Forwarded-Proto: https`
- Django вважатиме запит безпечним і встановить cookies з прапором `Secure` через звичайний HTTP
- Результат: витік session cookies

**2. Помилки CSRF**
- Проксі-сервери часто переписують заголовки `Host` та `Origin`
- Django відхиляє легітимні CSRF-запити
- Проблема виявляється лише в production після розгортання за ALB, Cloudflare або Nginx

**3. Безкінечні редіректи**
- При увімкненому `SECURE_SSL_REDIRECT = True` Django намагається перенаправити всі HTTP-запити на HTTPS
- Якщо Django не розпізнає запит як безпечний, виникає цикл редиректів

## Правильна конфігурація

**1. Налаштування проксі-сервера**
```nginx
proxy_set_header Host              $host;
proxy_set_header X-Forwarded-Proto $scheme;
proxy_set_header X-Real-IP         $remote_addr;
proxy_set_header X-Forwarded-For   $proxy_add_x_forwarded_for;
```

**2. Налаштування Django**
```python
# Вказати Django, якому заголовку довіряти
SECURE_PROXY_SSL_HEADER = ('HTTP_X_FORWARDED_PROTO', 'https')

# Примусове використання HTTPS
SECURE_SSL_REDIRECT = True
SESSION_COOKIE_SECURE = True
CSRF_COOKIE_SECURE = True
SECURE_HSTS_SECONDS = 31536000
SECURE_HSTS_INCLUDE_SUBDOMAINS = True

# Обмеження доменів
ALLOWED_HOSTS = ["yourapp.com", "www.yourapp.com"]
CSRF_TRUSTED_ORIGINS = ["https://yourapp.com"]
```

## Альтернативні методи безпеки

- **PROXY Protocol**: надійніший спосіб передачі інформації про клієнта
- **Mutual TLS**: взаємна автентифікація між проксі та Django
- **Приватні мережі (VPC)**: ізоляція трафіку
- **TLS Passthrough**: Django сам обробляє TLS

## Тестування конфігурації

1. Перевірити, як Django визначає схему запиту
2. Спробувати підробити заголовки
3. Перевірити прапори secure у cookies
4. Підтвердити наявність HSTS
5. Протестувати CSRF origins
6. Перевірити поведінку редиректів

## Головний висновок

**Ніколи не довіряйте проксі-серверу сліпо.** Створіть чіткий контракт довіри між проксі та Django, протестуйте його та дотримуйтесь. Проксі має видаляти клієнтські заголовки та встановлювати власні надійні значення, а Django повинен довіряти лише явно налаштованим заголовкам.
