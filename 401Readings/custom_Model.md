## Custom User Model

for a real-world project, the official Django documentation highly recommends using a `custom user model` instead. This provides far more flexibility down the line so, as a general rule, always use a custom user model for all new Django projects.


 **There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser.**


 **AbstractBaseUser requires much, much more work.**


 + update config/settings.py
+ create a new CustomUser model
+ create new UserCreation and UserChangeForm
+ update the admin



## Superuser

It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out. On the command line type the following command and go through the prompts.

 ` python manage.py createsuperuser`



 ## django x

 DjangoX can be installed via Pip, Pipenv, or Docker depending upon your setup. To start, clone the repo to your local computer and change into the proper directory.


```
$ git clone https://github.com/wsvincent/djangox.git
$ cd djangox
```
Pip
```
$ python3 -m venv djangox
$ source djangox/bin/activate
(djangox) $ pip install -r requirements.txt
(djangox) $ python manage.py migrate
(djangox) $ python manage.py createsuperuser
(djangox) $ python manage.py runserver
```
```
Pipenv
$ pipenv install
$ pipenv shell
(djangox) $ python manage.py migrate
(djangox) $ python manage.py createsuperuser
(djangox) $ python manage.py runserver
```

Docker
```
$ docker build .
$ docker-compose up -d
$ docker-compose exec web python manage.py migrate
$ docker-compose exec web python manage.py createsuperuser
```
For Docker, the INTERNAL_IPS configuration in config/settings.py must be updated to the following:
```
# config/settings.py
# django-debug-toolbar
```


## Setup
# Run Migrations
(djangox) $` python manage.py migrate`

# Create a Superuser
(djangox) $ `python manage.py createsuperuser`

# Confirm everything is working:
(djangox) $ `python manage.py runserver`


