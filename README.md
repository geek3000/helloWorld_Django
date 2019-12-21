# HELLO WORLD WITH DJANGO

Django is a framework help you to create web app in python

## Installation
use pip to install django

```bash
pip install Django
```

## Create hello world application
First create project

```bash
django-admin startproject hello_world
```
After use manage.py file in project directory to create application

```bash
python manage.py startapp hello_world_app
```
and now modify settings.py file

```python
INSTALLED_APPS = [

    'django.contrib.admin',

    'django.contrib.auth',

    'django.contrib.contenttypes',

    'django.contrib.sessions',

    'django.contrib.messages',

    'django.contrib.staticfiles',

    'hello_world_app',

]
```

### Add view to application

Create a view in views.py
```python
from django.http import HttpResponse
from django.shortcuts import render

def home(request):
    return HttpResponse("""
        <h1>Hello World !</h1>
        <p>Fedora Community!!!! !</p>""")
```

After add route in urls.py
```python
path('', views.home)
```
```python
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', views.home),
]
```



## Learn more!
to learn more about djano see [documentation](https://docs.djangoproject.com/)
