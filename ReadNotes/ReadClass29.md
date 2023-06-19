# Django Custum User Model

Django comes with a built-in User model for authentication, however the official Django documentation highly recommends using a custom user model for new projects. The reason is if you want to make any changes to the User model down the road, using a custom user model from the beginning makes this quite easy.

## Setup

To start, create a new Django project from the command line. We need to do several things:

- create and navigate into a dedicated directory called accounts for our code
- install Django
- make a new Django project called config
- make a new app accounts
- start the local web server
- Here are the commands to run:

```bash
$ cd ~/Desktop
$ mkdir accounts && cd accounts
$ pipenv install django~=3.1.0
$ pipenv shell
(accounts) $ django-admin.py startproject config .
(accounts) $ python manage.py startapp accounts
(accounts) $ python manage.py runserver
```

## AbstractUser vs AbstractBaseUser

There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work.

## Custom User Model

Creating our initial custom user model requires four steps:

- update config/settings.py
- create a new CustomUser model
- create new UserCreation and UserChangeForm
- update the admin

## Superuser

```bash

$ python manage.py createsuperuser
```

## Templates

```bash
$ mkdir templates
$ touch templates/base.html
$ mkdir templates/registration
$ touch templates/registration/login.html
$ touch templates/registration/signup.html
```

## Forms

```bash
$ mkdir accounts/forms.py
```

## Login and Logout

```bash

$ touch accounts/views.py
```

## Restricting Access

```bash
$ mkdir templates/registration
$ touch templates/registration/logged_out.html
```

## Next Steps

- Add email authentication
- Add “forgot password” functionality
- Add password validation
- Add password reset functionality
- Add email address verification
- Add OAuth via social networks
- Add API endpoints for integration with other services
- Add tests
- Add i18n
- Add CI/CD
- Add Docker
- Add Bootstrap
- Add logging
- Add security
- Add permissions


## What are the key benefits of using a Django Custom User Model, and how does it differ from the default Django User Model? 

- The default Django user model is not suitable for modern
+ The default Django user model contains only basic fields like username, email, password, etc. It is not suitable for modern web applications. So, we need to create a custom user model.
- The default Django user model contains only basic fields like username, email, password, etc. It is not suitable for modern web applications. So, we need to create a custom user model.

## Explain the process of creating and implementing a Custom User Model in Django, including the necessary changes to settings.py and the required model fields. 

- Creating a custom user model in Django is a two-step process. First, we need to update the AUTH_USER_MODEL setting to point to our new custom user model. The custom user model we’re going to build is called CustomUser and is located in the users app. The second step is to create a new CustomUserCreationForm and CustomUserChangeForm. These forms will override the default user creation and change forms used by Django. We do this so that we can use our email address instead of a username for authentication.

## What is DjangoX and how does it complement or extend the functionality of Django?

- DjangoX is a framework for building Django projects. It is a collection of open-source Django apps and projects that form the basis for new Django projects. It is a collection of open-source Django apps and projects that form the basis for new Django projects.