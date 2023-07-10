# Django Settings Best Practices
- django-admin startproject mysite
- cd mysite
- python manage.py startapp polls
- python manage.py migrate
- python manage.py runserver
- python manage.py createsuperuser
- python manage.py makemigrations polls
- python manage.py sqlmigrate polls 0001
- python manage.py migrate
- python manage.py shell
- python manage.py test polls

# Whitenoise

## what is Whitenoise?
- WhiteNoise allows your web app to serve its own static files, making it a self-contained unit that can be deployed anywhere without relying on nginx, Amazon S3 or any other external service. (It’s also designed to work nicely with Django apps that are using Django’s staticfiles app.)


- pip install whitenoise
- Add whitenoise to your middleware after the SecurityMiddleware (if you are using it) and before all other middleware except for Django’s GZipMiddleware (if you are using it):
- MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'whitenoise.middleware.WhiteNoiseMiddleware',
    # ...
]
- Add WhiteNoise to the top of your INSTALLED_APPS:
- INSTALLED_APPS = [
    'whitenoise.runserver_nostatic',  # < As per Whitenoise documentation
    # ...
]
- Add a STATICFILES_STORAGE setting to tell WhiteNoise where to store your static files in production. The default is the same as Django’s, but with the addition of the WhiteNoise middleware. This means that if you’re already using Django’s CachedStaticFilesStorage there’s no need to change anything.
- STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'
- Finally, make sure you have DEBUG = False in your settings file. That’s it, you’re done!

# CORS

## what is CORS?
- Cross-Origin Resource Sharing (CORS) is a mechanism that uses additional HTTP headers to tell browsers to give a web application running at one origin, access to selected resources from a different origin. A web application executes a cross-origin HTTP request when it requests a resource that has a different origin (domain, protocol, and port) than its own origin.

## How CORS works?
- CORS works by adding a special header to responses from a server to the client. This header is called Access-Control-Allow-Origin. It specifies what domains can access the resource. If the client is on a different domain than the server, it will make a request to the server, which will respond with the Access-Control-Allow-Origin header that specifies which domains can access the resource.

- pip install django-cors-headers
- Add corsheaders to your INSTALLED_APPS setting:
- INSTALLED_APPS = (
    ...
    'corsheaders',
    ...
)
- Add the CorsMiddleware after the Django SecurityMiddleware (if you are using it) and before Django’s CommonMiddleware:
- MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'corsheaders.middleware.CorsMiddleware', # < CorsMiddleware after SecurityMiddleware
    'django.middleware.common.CommonMiddleware',
    ...
]
- Add the following to your settings:
- CORS_ORIGIN_ALLOW_ALL = True
- CORS_ALLOW_CREDENTIALS = True
- CORS_ORIGIN_WHITELIST = (
    'localhost:3000',
)
- CORS_ORIGIN_REGEX_WHITELIST = (
    'localhost:3000',
)
- CORS_ALLOW_METHODS = (
    'DELETE',
    'GET',
    'OPTIONS',
    'PATCH',
    'POST',
    'PUT',
)




