# Django REST Framework & Docker

*  it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore. The entire development environment is isolated: programming language, software packages, databases, and more.

* we now longer have to mess around with virtual environments.

* Docker is really just Linux containers which are a type of virtualization.

## Containers vs Virtual Environments

Virtual environments are used to isolate Python software packages locally.


# Library Website and API

Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.


## Traditional Django


First we need a dedicated directory on our computer to store the code. This can live anywhere but for convenience, if you are on a Mac, we can place it in the Desktop folder. The location really does not matter; it just needs to be easily accessible.

```
$ cd ~/Desktop
$ mkdir code && cd code

```


Now we are within the code folder which will be the location for all the code in this book. The next step is to create a dedicated directory for our library site, install Django via Pipenv, and then enter the virtual environment using the shell command. You should always use a dedicated virtual environment for every new Python project.


```

$ mkdir library && cd library
$ pipenv install django~=3.1.0
$ pipenv shell
(library) $

```
Pipenv creates a Pipfile and a Pipfile.lock within our current directory. The (library) in parentheses before the command line shows that our virtual environment is active.

A traditional Django website consists of a single project and one (or more) apps representing discrete functionality. Let’s create a new project with the startproject command. Don’t forget to include the period . at the end which installs the code in our current directory. If you do not include the period, Django will create an additional directory by default.


```
(library) $ django-admin startproject config .
```

## First app

The typical next step is to start adding apps, which represent discrete areas of functionality. A single Django project can support multiple apps.

Each app has a __init__.py file identifying it as a Python package. There are 6 new files created:

1. admin.py is a configuration file for the built-in Django Admin app
2. apps.py is a configuration file for the app itself
3. the migrations/ directory stores migrations files for database changes
4. models.py is where we define our database models
5. tests.py is for our app-specific tests
6. views.py is where we handle the request/response logic for our web app


# Django REST Framework

Django REST Framework is added just like any other third-party app.

## Serializers
A serializer translates data into a format that is easy to consume over the internet, typically JSON, and is displayed at an API endpoint. We will also cover serializers and JSON in more depth in following chapters. For now I want to demonstrate how easy it is to create a serializer with Django REST Framework to convert Django models to JSON.
