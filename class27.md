# Django Models

## Overview

Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.**Once** you've chosen what database you want to use, you don't need to talk to it directly at all — you just write your model structure and other code, and Django handles all the dirty work of communicating with the database for you.

## Designing the LocalLibrary models

* We need to store information about books (title, summary, author, written language, category, ISBN) and that we might have multiple copies available (with globally unique id, availability status, etc.). We might need to store more information about the author than just their name, and there might be multiple authors with the same or similar names. We want to be able to sort information based on book title, author, written language, and category.

* When designing your models it makes sense to have separate models for every "object" (a group of related information). In this case, the obvious objects are books, book instances, and authors.

* You might also want to use models to represent selection-list options (e.g. like a drop down list of choices), rather than hard coding the choices into the website itself — this is recommended when all the options aren't known up front or may change. Obvious candidates for models, in this case, include the book genre (e.g. Science Fiction, French Poetry, etc.) and language (English, French, Japanese).

* Once we've decided on our models and field, we need to think about the relationships. Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).

<img src="img/django_model.PNG">


## Model primer

1- Model definition : `models.py`

2- Fields : ` my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')`

3- Metadata :
```
 class Meta:
    ordering = ['-my_field_name']
```

## Defining the LocalLibrary Models

* from django.db import models

## Re-run the database migrations

```
python3 manage.py makemigrations
python3 manage.py migrate
```


# Django Admin

## Overview:


The Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records. This can save you a lot of time during development, making it very easy to test your models and get a feel for whether you have the right data. The admin application can also be useful for managing data in production, depending on the type of website.

## Registering models 

* First, open admin.py in the catalog application (/locallibrary/catalog/admin.py).

## Creating a superuser

`python3 manage.py createsuperuser`




