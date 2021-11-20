## Docker

Docker is. A way to implement Linux containers!

**Linux containers**

+ Containers are a lightweight alternative to Virtual Machines

+ Dockerfile is a list of instructions for creating an image

+ Virtual Machines are like homes: stand-alone buildings with their own infrastructure including 

 and heating, as well as a kitchen, bathrooms, bedrooms, and so on. Docker containers are like apartments: they share common infrastructure like plumbing and heating, but come in various sizes that match the exact needs of an owner.

## Install version

`docker --version`



Docker Compose is an additional tool that is automatically included with Mac and Windows downloads of Docker. However if you are on Linux, you will need to add it manually. You can do this by running the command sudo pip install docker-compose after your Docker installation is complete.


A good command to inspect Docker is docker info which we can run now. It will contain a lot of output but focus on the top lines which show we now have 1 container which is stopped and 1 image.


## files 

Order matters in Dockerfiles since they are executed from top-to-bottom. First we use FROM to install python:3.7-alpine as our base image and set two environment variables with ENV. The first, PYTHONDONTWRITEBYTECODE will remove .pyc files from our container which is a good optimization


(Because of layer caching when a step changes in the Dockerfile, all subsequent work needs to be redone.)


Multiple services can run within a Docker host–for example, we might add a db service for a running PostgreSQL database in the future–but for now we have a single web service.




# Library Website and API

(We cannot build a web API with only Django Rest Framework)


## differences between traditional Django and Django REST Framework : 


##  Traditional Django

**The files have the following roles:**

+ __init__.py is a Python way to treat a directory as a package; it is empty
+ asgi.py stands for Asynchronous Server Gateway Interface and is a new option in Django 3.0+

+ settings.py contains all the configuration for our project
+ urls.py controls the top-level URL routes
+ wsgi.py stands for Web Server Gateway Interface and helps Django serve the eventual web pages
+ manage.py executes various Django commands such as running the local web server or creating a new app.



### Models

This is a basic Django model where we import models from Django on the top line and then

### Admin 

start entering data into our new model via the built-in Django app



## Django REST Framework

Django REST Framework is added just like any other third-party app. 

` pipenv install djangorestframework~=3.11.0`


Add it to the INSTALLED_APPS config in our settings.py

The api app will not have its own database models so there is no need to create a migration file and run migrate to update the databas

##  URLs


Then create a urls.py file within the api app.


 `touch api/urls.py`

 And update it as follows:
```
# api/urls.py
from django.urls import path
from .views import BookAPIView

urlpatterns = [
    path('', BookAPIView.as_view()),
]
```


## Views

some developers will call an API views file apiviews.py or api.py

Within our views.py file, update it to look like the following:

```

# api/views.py
from rest_framework import generics

from books.models import Book
from .serializers import BookSerializer


class BookAPIView(generics.ListAPIView):
    queryset = Book.objects.all()
    serializer_class = BookSerializer

```

The only two steps required in our view are to specify the queryset which is all available books, and then the serializer_class which will be BookSerializer.


## Serializers

A serializer translates data into a format that is easy to consume over the internet, typically JSON.

Make a serializers.py file within our api app.

` touch api/serializers.py`


## cURL


We can use the popular cURL program to execute HTTP requests via the command line.All we need for a basic GET request it to specify curl and the URL we want to call.


## resources

1- [djangoforapis](https://djangoforapis.com/library-website-and-api/)


2- [beginners-guide-to-docker](https://wsvincent.com/beginners-guide-to-docker/)
