
# Defending-Django

https://www.securitycompass.com/training_courses/dja201-defending-django/

# Курс з безпеки Django

## Цілі навчання курсу

У цьому курсі ви дізнаєтеся, що потрібно робити, щоб скористатися перевагами **вбудованих функцій безпеки Django** та забезпечити додаткові рівні захисту для вашого додатку. Ви навчитеся налаштовувати свої проєкти безпечно, щоб запобігати атакам під час виконання, та як захистити адміністративну консоль.

Ви також дізнаєтеся, як виявляти безпечні та небезпечні практики для захисту вашого додатку від поширених експлойтів, таких як **клікджекінг, міжсайтовий скриптинг** та **XML зовнішні сутності**. Цей курс також досліджує, як захиститися від інших експлойтів за допомогою налаштувань Django, як керувати користувачами та захищати ваше продакшн середовище.

## Опис

Цей курс був створений для розробників, які вже мають деякий досвід програмування на **Python та розробки веб-додатків** з платформою Django. Мета цього курсу — висвітлити безпечні способи створення веб-додатків, максимально використовуючи вбудовані функції безпеки Django, та розвинути те, що ви вже знаєте про використання платформи Django.

## План курсу

### 1. Налаштування Django проєкту
- Чотирьохчастинна структура Django
- Django settings.py
- Про Django settings.py
- Захист секретного ключа
- Де зберігати секретний ключ та інші секрети
- Як отримати доступ до секретних ключів
- Встановлення Django SecurityMiddleware
- Список MIDDLEWARE
- Захист транспортного рівня
- Налаштування параметрів HSTS
- Політика Referrer
- Нова політика за замовчуванням у Django 3.1+
- Налаштування облікового запису суперкористувача
- Змінні середовища
- Використання змінних середовища

### 2. Захист від експлойтів 1.
- Блокування клікджекінгу
- Заголовок X-Frame-Options
- Активація захисту від клікджекінгу
- Звільнення view від захисту клікджекінгу
- Про XSS
- Захист HTML коду від експлуатації XSS
- Тимчасове відключення захисту шаблонів Django
- Про CSRF
- Захист Django від CSRF
- Впровадження захисту CSRF
- Використання захисту CSRF з окремими view
- Блокування MIME або content sniffing
- Активація захисту від content або MIME sniffing
- Про вразливість XML зовнішніх сутностей (XXE)
- Блокування вразливостей XXE за допомогою пакету defusedxml
- Перехід з XML на JSON

### 3. Захист від експлойтів 2.
- Про COOP
- Зробіть свій веб-сайт "Cross-Origin Isolated"
- Валідація хостів
- Створення списку ALLOWED_HOSTS
- Django Object-Relational Mappers (ORM)
- Параметризація сирих SQL запитів
- Екранування та санітизація символьних рядків
- Автоматичне екранування
- Захист автоматичного екранування
- HTML санітизація за допомогою django-bleach
- Блокування ін'єкції Python коду
- Безпечне використання eval(), exec() та execfile()
- Серіалізація/парсинг вводу

### 4. Управління користувачами
- Аутентифікація користувачів Django
- Користувацька валідація паролів у Django
- Обмеження спроб аутентифікації користувачів
- Налаштування django-defender
- Кастомізація django-defender
- Двофакторна аутентифікація (2FA)
- Розгортання 2FA у Django
- Впровадження безпечного управління сесіями
- Варіанти зберігання сесій у Django
- Метод Cached_db
- Налаштування зберігання сесій
- Налаштування cookies сесій
- Контент, завантажений користувачами
- Захист контенту, завантаженого користувачами
- Зберігання контенту, завантаженого користувачами
- Налаштування сервера для контенту користувачів
- Налаштування моделі Django

### 5. Захист продакшн середовища
- Вимкнення DEBUG у продакшені
- Продакшн сервер бази даних
- Оновлення пароля та привілеїв для адміністратора бази даних
- Перенесення деталей бази даних до .env файлу
- Доступ до інформації бази даних з .env файлу
- Створення .gitignore файлу для .env файлу
- Захист вихідного коду та чутливих даних
- Зміна URL адміністратора Django за замовчуванням
- Перейменування каталогу документації адміністратора за замовчуванням
- Обмеження доступу до конкретних IP адрес
- Django-admin-honeypot
- Встановлення django-admin-honeypot
- Тестування модулів Django
- Впровадження юніт тестів
- Запуск manage.py check –deploy
- Використання логування та моніторингу в Django додатках
- Налаштування логування Django
- Розуміння ваших Python залежностей
- Використання pip для створення списку залежностей requirements
- Оновлення Django

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# Django Security Course

## Course Learning Objectives

In this course, you'll learn what you need to do to take advantage of **Django's built-in security features** and provide other layers of protection to your app. You'll learn how to set up your projects securely to prevent attacks at run-time and how to secure the admin console.

You will also learn how to identify secure and insecure practices to protect your application against common exploits, such as **clickjacking, cross-site scripting**, and **XML External Entities**. This course also explores how to defend against other exploits using Django settings, how to manage users, and securing your production environment.

## Description

This course was created for developers who already have some experience coding in **Python and developing web applications** with the Django platform. The purpose of this course is to highlight secure ways of creating web applications, making the best use of Django's built-in security features, and to build on what you already know about using the Django platform.


## Course Outline

### 1. Setting Up a Django Project
- Django's Four-Part framework
- Django settings.py
- About Django settings.py
- Securing the secret key
- Where to store secret key and other secrets
- How to access secret keys
- Installing Django SecurityMiddleware
- The MIDDLEWARE list
- Securing the Transport Layer
- Configuring HSTS settings
- Referrer policy
- New default policy in Django 3.1+
- Setting up the superuser account
- Environment variables
- Using environment variables

### 2. Defending Against Exploits 1.
- Blocking clickjacking
- The X-Frame-Options header
- Activating clickjacking protection
- Exempting a view from clickjacking protection
- About XSS
- Protecting HTML code from XSS exploitation
- Temporarily disabling Django's template protection
- About CSRF
- Django's CSRF defense
- Implementing CSRF protection
- Using CSRF protection with single views
- Blocking MIME or content sniffing
- Activating content or MIME sniffing protection
- About XML External Entities (XXE) vulnerability
- Blocking XXE vulnerabilities with the defusedxml package
- Switching from XML to JSON

### 3. Defending Against Exploits 2.
- About COOP
- Make your website "Cross-Origin Isolated"
- Validating hosts
- Create a list of ALLOWED_HOSTS
- Django Object-Relational Mappers (ORM)
- Parameterize raw SQL queries
- Escaping and sanitizing character strings
- Auto escaping
- Safeguard auto escaping
- HTML sanitation using django-bleach
- Blocking Python code injection
- Use eval(), exec(), and execfile() safely
- Serialization/Input parsing

### 4. User Management
- Django user authentication
- Custom password validation in Django
- Throttling user authentications
- Configuring django-defender
- Customizing django-defender
- Two-Factor Authentication (2FA)
- Deploying 2FA in Django
- Implementing secure session management
- Session storage options in Django
- Cached_db method
- Setting up session storage
- Configuring session cookies
- User-uploaded Content
- Securing user-uploaded content
- Storing user-uploaded content
- Configuring server for user-uploaded content
- Configuring Django model

### 5. Securing the Production Environment
- Turn off DEBUG in production
- Production database server
- Update password and privileges for the database admin
- Transferring database particulars to .env file
- Access database information from the .env file
- Create a .gitignore file for .env file
- Protect source code and sensitive data
- Change the default Django admin URL
- Rename the default admin docs directory
- Restrict access to specific IP addresses
- Django-admin-honeypot
- Install django-admin-honeypot
- Test Django modules
- Implement unit tests
- Run manage.py check –deploy
- Use logging and monitoring in Django applications
- Set up Django logging
- Understand your Python dependencies
- Use pip to create a dependencies requirements list
- Update Django

  -----------------------------------------------------------------------------------


# Проектування системи дозволів для Django SaaS

 Побудова комплексної системи дозволів для багатоорендних SaaS-додатків на Django, що включає ролі, політики, безпеку на рівні рядків та асинхронні перевірки.

![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*GeFQAbjBl17OV0tzkWcTsA.png)


# Посилання

- Modern DevSecOps Practices for Django Developers (2025 Edition), https://medium.com/@Am_Issath/modern-devsecops-practices-for-django-developers-2025-edition-d007d61791c9
- Django Internationalization: Because the World Speaks More Than English (And Your App Doesn’t), https://medium.com/@Am_Issath/django-internationalization-because-the-world-speaks-more-than-english-and-your-app-doesnt-8968ea951dd4
- How to Implement OAuth 2.0 Authentication in Django, https://medium.com/@Am_Issath/how-to-implement-oauth-2-0-authentication-in-django-c9ecf251a5ef
- Building a Django Enterprise-Ready Roles and Permissions System, https://medium.com/@eagnoun/building-a-django-enterprise-ready-roles-and-permissions-system-5eb9136427fb
- Nginx for Django + Hugo: Reverse Proxy Like a Pro, https://medium.com/@anzaloquin/nginx-for-django-hugo-reverse-proxy-like-a-pro-2c4f7f5cb378
- Stop Trusting Your Reverse Proxy: Secure Django the Right Way, https://medium.com/@anas-issath/stop-trusting-your-reverse-proxy-secure-django-the-right-way-ec45bad71c34
- How to Deploy a Django REST API with Nginx and Gunicorn on Ubuntu (Step-by-Step Guide), https://medium.com/@jinalpatel001212/how-to-deploy-a-django-rest-api-with-nginx-and-gunicorn-on-ubuntu-step-by-step-guide-600d8e3c84a4
- Protecting Your Django Application: Building a Custom Rate Limiter with Redis Middleware (Part 1), https://medium.com/@sizanmahmud08/protecting-your-django-application-building-a-custom-rate-limiter-with-redis-middleware-part-1-a5088a5776c9
- Load Testing Django Rate Limiting: Stress Testing with Locust and Advanced Redis Patterns (Part 2), https://medium.com/@sizanmahmud08/load-testing-django-rate-limiting-stress-testing-with-locust-and-advanced-redis-patterns-part-2-c174db329f91
- The Art of Writing Clean Django Code — Part 2, https://medium.com/@djangowiki/the-art-of-writing-clean-django-code-part-2-31201ac07cd0
- The Art of Writing Clean Django Code — Part 3, https://medium.com/@djangowiki/the-art-of-writing-clean-django-code-part-3-54e924a22635
- Stop Using Django’s Default Settings — Do This Instead, https://medium.com/the-pythonworld/stop-using-djangos-default-settings-do-this-instead-ea6f814dc1a1

# Django SaaS

- Designing a Django SaaS Permission System (Roles, Policies, RLS, and Async Checks), https://medium.com/@yogeshkrishnanseeniraj/designing-a-django-saas-permission-system-roles-policies-rls-and-async-checks-5f63f9288b25
- SaaS Applications with Django: Introduction to Building Scalable Software Solutions [Part 1/7], https://medium.com/@mathur.danduprolu/saas-applications-with-django-introduction-to-building-scalable-software-solutions-part-1-7-d0228bc3761b
- SaaS Applications with Django: User Management and Role-Based Access Control [Part 3/7], https://medium.com/@mathur.danduprolu/saas-applications-with-django-user-management-and-role-based-access-control-part-3-7-a8ff2b8c6490
- SaaS Applications with Django: Ensuring Security for Your SaaS Platform [Part 6/7], https://medium.com/@mathur.danduprolu/saas-applications-with-django-ensuring-security-for-your-saas-platform-part-6-7-80bbfabfbd07
- Django and Microservices Architecture: A Comprehensive Guide [Part 1/7], https://medium.com/@mathur.danduprolu/django-and-microservices-architecture-a-comprehensive-guide-part-1-7-6505e42cc38d
- Django and Microservices Architecture: Database Management for Microservices [Part 4/7], https://medium.com/@mathur.danduprolu/django-and-microservices-architecture-database-management-for-microservices-part-4-7-17f4ddd72d50
- Django and Microservices Architecture: Securing Microservices [Part 6/7], https://medium.com/@mathur.danduprolu/django-and-microservices-architecture-securing-microservices-part-6-7-bd5b9a8307b9
- 



# Django Aplication
- Day 9: Building a Sentiment Analysis Tool with Django and NLT, https://medium.com/@mathur.danduprolu/day-12-building-a-sentiment-analysis-tool-with-django-and-nlt-3272fb05d985
- 


# Authentication
- Django and React -Implementing Token Authentication with Simple JWT🤖, https://medium.com/@sarathkumarrs/django-and-react-implementing-token-authentication-with-simple-jwt-b2a4f290f401
- OAuth Implementation from scratch — React Native with Expo(Django Backend), https://medium.com/@sarathkumarrs/oauth-implementation-from-scratch-react-native-with-expo-django-backend-8f1dec117224


# NGINX
- Deploying and Monitoring NGINX in a Production Environment [Part 7/7], https://medium.com/@mathur.danduprolu/deploying-and-monitoring-nginx-in-a-production-environment-part-7-7-81e548bb2c56
- A Practical Guide to Blue/Green Deployments Using Nginx, https://medium.com/@Adewuumii/a-practical-guide-to-blue-green-deployments-using-nginx-3fcd1001ccc3
- 


# REST API 
- 🚀 8 REST API Design Rules That Separate Senior Engineers from Beginners, https://medium.com/write-a-catalyst/8-rest-api-design-rules-that-separate-senior-engineers-from-beginners-1d5d2409e54d
- Django REST API: Swagger Docs & Testing Made Simple, https://medium.com/@sarathkumarrs/django-rest-api-swagger-docs-testing-made-simple-21da7eb0485b
- Django Rest Framework Best Practices, https://medium.com/@Tech_girlll/django-rest-framework-best-practices-419cbe6d81d6
- 

# SECURE DOCKER
- A Complete Guide to Secure Docker-Compose Applications With Traefik, https://medium.com/@rragesh/a-complete-guide-to-secure-docker-compose-applications-with-traefik-bde8b143839d
- 

