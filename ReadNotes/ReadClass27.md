# Django Models
## What is a Model?
A model is the single, definitive source of information about your data. It contains the essential fields and behaviors of the data you’re storing. Generally, each model maps to a single database table.

The basics:
- Each model is a Python class that subclasses django.db.models.Model.
- Each attribute of the model represents a database field.
- With all of this, Django gives you an automatically-generated database-access API; see Making queries.

## Fields
The most important part of a model – and the only required part of a model – is the list of database fields it defines. Fields are specified by class attributes. Be careful not to choose field names that conflict with the models API like clean, save, or delete.

### Field types
Each field in your model should be an instance of the appropriate Field class. Django uses the field class types to determine a few things:
- The column type, which tells the database what kind of data to store (e.g. INTEGER, VARCHAR, TEXT).


### Field options
Each field takes a certain set of field-specific arguments (documented in the model field reference). For example, CharField (and its subclasses) require a max_length argument which specifies the size of the VARCHAR database field used to store the data.

### Explain the purpose and basic structure of Django models. How do they help in creating and managing database schema in a Django application?
Django models are a way to interact with the database using Python code. It allows you to create, retrieve, update, and delete records from the database by calling Python code instead of writing SQL queries.

### Describe the primary features and functionality of the Django Admin interface. How can it be customized to suit the specific needs of a project?
Django Admin is a built-in app that allows you to perform CRUD operations on your models. It is a quick and easy way to manage your database.

### Briefly outline the key components and workflow of a Django application, as discussed in the Beginner’s Guide to Django. How do these components interact with each other to create a functional web application?
- Django ORM: Django ORM is a way to interact with the database using Python code. It allows you to create, retrieve, update, and delete records from the database by calling Python code instead of writing SQL queries.

- Django Admin: Django Admin is a built-in app that allows you to perform CRUD operations on your models. It is a quick and easy way to manage your database.

- Django Views: Django views are Python functions that take a web request and return a web response. They are the bridge between models and templates.

- Django Templates: Django templates are HTML files that contain placeholders for dynamic data. They are rendered by views and displayed in the browser.