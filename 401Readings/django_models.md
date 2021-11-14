## Using models

Django web applications access and manage data through Python objects referred to as models. Models define the structure of stored data, including the field types and possibly also their maximum size, default values,


## Designing the  models

When designing your models it makes sense to have separate models for every "object" (a group of related information). In this case, the obvious objects are books, book instances, and authors.

You might also want to use models to represent selection-list options (e.g. like a drop down list of choices), rather than hard coding the choices into the website itself 

Once we've decided on our models and field, we need to think about the relationships. Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).



## Model definition

Models are usually defined in an application's models.py file. They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata. The code fragment below shows a "typical" model, named MyModelName:


 features inside the model:

## Fields

A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables. Each database record (row) will consist of one of each field value. 


## Metadata
You can declare model-level metadata for your Model by declaring class Meta, as shown.
```
class Meta:
    ordering = ['-my_field_name']
```

One of the most useful features of this metadata is to control the default ordering of records returned when you query the model type. 



## Methods

Minimally, in every model you should define the standard Python class method __str__() to return a human-readable string for each object.


Another common method to include in Django models is get_absolute_url(), which returns a URL for displaying individual model records on the website 




## Model management

Once you've defined your model classes you can use them to create, update, or delete records, and to run queries to get all records or particular subsets of records

+ creatibg records

You can access the fields in this new record using the dot syntax, and change the values. You have to call `save()` to store modified values to the database.


+ Searching for records

We can get all records for a model as a QuerySet, using objects.all(). The QuerySet is an iterable object, meaning that it contains a number of objects that we can iterate/loop through.


Django's `filter()` method allows us to filter the returned QuerySet to match a specified text or numeric field against particular criteria. For example, to filter for books that contain "wild" in the title and then count them, we could do the following.


##  Django admin


+ Registering models 

First, open admin.py in the catalog application (/locallibrary/catalog/admin.py). It currently looks like this — note that it already imports django.contrib.admin


Register the models by copying the following text into the bottom of the file. This code imports the models and then calls admin.site.register to register each of them.


+ Creating a superuser


  You can create a "superuser" account that has full access to the site and all needed permissions using manage.py.


  + logging in and using the site

  To login to the site, open the /admin URL (e.g. http://127.0.0.1:8000/admin) and enter your new superuser userid and password credentials (you'll be redirected to the login page, and then back to the /admin URL after you've entered your details).


  + Advanced configuration

1- Register a ModelAdmin class

2- Configure list views


3-Add list filters


4- Organize detail view layout

5- Inline editing of associated records
