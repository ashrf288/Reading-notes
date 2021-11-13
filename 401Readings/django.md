## Django


Django includes dozens of extras you can use to handle common web development tasks. Django takes care of user authentication, content administration, site maps, RSS feeds, and many more tasks — right out of the box

**Django requires Python.Python includes a lightweight database called SQLite so you won’t need to set up a database just yet.**


## Creating a project

initial setup. Namely, you’ll need to auto-generate some code that establishes a Django project – a collection of settings for an instance of Django, including database configuration, Django-specific options and application-specific settings.


`django-admin startproject mysite`

This will create a mysite directory in your current directory

### django project tree

```
mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```
+ The outer **mysite/** root directory is a container for your project.

+ **manage.py:** A command-line utility that lets you interact with this Django project in various ways.

+ The inner **mysite/** directory is the actual Python package for your project

+** mysite/__init__.py:** An empty file that tells Python that this directory should be considered a Python package


+ **mysite/settings.py:** Settings/configuration for this Django project


+ **mysite/urls.py**: The URL declarations for this Django project; a “table of contents” of your Django-powered site.


+ **mysite/asgi.py**: An entry-point for ASGI-compatible web servers to serve your project.

+** mysite/wsgi.py:** An entry-point for WSGI-compatible web servers to serve your project. 


## The development server

`$ python manage.py runserver`

It’s intended only for use while developing.


By default, the runserver command starts the development server on the internal IP at port 8000.

If you want to change the server’s port, pass it as a command-line argument. For instance, this command starts the server on port 8080:
`$ python manage.py runserver 8080`


The development server automatically reloads Python code for each request as needed. You don’t need to restart the server for code changes to take effect. However, some actions like adding files don’t trigger a restart, so you’ll have to restart the server in these cases.



## To create your app
 make sure you’re in the same directory as manage.py and type this command:

`$ python manage.py startapp polls`

 To call the view, we need to map it to a URL - and for this we need a URLconf.

To create a URLconf in the polls directory, create a file called urls.py.



 **The path() function is passed four arguments, two required: route and view, and two optional: kwargs, and name. At this point, it’s worth reviewing what these arguments are for.**

 + **route** is a string that contains a URL pattern. When processing a request, Django starts at the first pattern in urlpatterns and makes its way down the list, comparing the requested URL against each pattern until it finds one that matches.


 + **view** When Django finds a matching pattern, it calls the specified view function with an HttpRequest object as the first argument and any “captured” values from the route as keyword arguments. We’ll give an example of this in a bit.

 + **kwargs** Arbitrary keyword arguments can be passed in a dictionary to the target view. We aren’t going to use this feature of Django in the tutorial.

 + **name** Naming your URL lets you refer to it unambiguously from elsewhere in Django, especially from within templates. This powerful feature allows you to make global changes to the URL patterns of your project while only touching a single file.



## Database setup

By default, the configuration uses SQLite. If you’re new to databases, or you’re just interested in trying Django, this is the easiest choice. SQLite is included in Python, so you won’t need to install anything else to support your database.

![](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Introduction/basic-django.png)



Django code is written using design principles and patterns that encourage the creation of maintainable and reusable code. In particular, it makes use of the Don't Repeat Yourself (DRY) principle so there is no unnecessary duplication, reducing the amount of code.

Handling the request (views.py)
Views are the heart of the web application, receiving HTTP requests from web clients and returning HTTP responses. In between, they marshal the other resources of the framework to access databases, render templates
