# Ex03 Time Table
# Date:
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using `<table>` tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM
views.py
```
from django.shortcuts import render
def new(request):
    return render(request,'priyan.html')
```
settings.py
```
from pathlib import Path
import os
BASE_DIR = Path(__file__).resolve().parent.parent
SECRET_KEY = 'django-insecure-)lsu253x(#381c^k1%lxb7ib^fs^gaqkncwuz0m1+x9)g)zuer'
DEBUG = True
ALLOWED_HOSTS = []
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'timetable',
]
MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]
ROOT_URLCONF = 'experi.urls'
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
WSGI_APPLICATION = 'experi.wsgi.application'
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]
LANGUAGE_CODE = 'en-us'
TIME_ZONE = 'UTC'
USE_I18N = True
USE_TZ = True
STATIC_URL = 'static/'
DEFAULT_AUTO_FIELD = 'django.db.models.BigAutoField'
```
urls.py
```
from django.contrib import admin
from django.urls import path
from timetable import views

urlpatterns = [
    # path('admin/', admin.site.urls),
    path('timetable',views.new)
]
```
timetable
```
<html>
    <head>
        <title>Time table</title>
        <center>
        <h1>time table</h1>
    </center>
    </head>


    <hr>
    <center>
    {% load static %}
    <img src="{% static 'images\secc logo.jpeg' %}">
    </center>
    <center>
        <h1>slot timetable-Priyan U (24900703)</h1>
        <hr>
        <style>
            th{
                background-color: red;
            }
            td{
                background-color: blueviolet;
                color: white;
            }
        </style>
    <div> 
    <table border="1" >
        <tr>
            <th >Time table</th>
            <th >Monday</th>
            <th >Tuesday</th>
            <th >Wednesday</th>
            <th >Thrusday</th>
            <th >Friday</th>
            <th >saturday</th>
        </tr>
        <tr >
            <th >8:00 to 10:00</th>
            <td>Digital electronics</td>
            <td></td>
            <td>Engineering design</td>
            <td></td>
            <td>Calculas and Matrix</td>
            <td></td>
        </tr>
        <tr>
            <th >10:00 to 12:00</th>
            <td >Fundamentals of web app development</td>
            <td>Physics</td>
            <td>python programming</td>
            <td></td>
            <td>career development class</td>
            <td>Calculas and Matrix</td>
        </tr>
        <tr>
            <th >12:00 to 1:00</th>
            <th colspan="6">LUNCH</th>
        </tr>
        <tr>
            <th>1:00 to 3:00</th>
            <td>Engineering design</td>
            <td >Digital electronics</td>
            <td>Mentor meeting</td>
            <td >Fundamentals of web app development</td>
            <td >python programming</td>
            <td >Physics</td>
        </tr>
        <tr >
            <th>3:00 to 5:00</th>
            <td colspan="5"></td>
            <td>Fundamentals of web app development</td>
        </tr>
    </table>
</div>   
<hr>
<table>
    <tr>
        <th>S.No</th>
        <th>Subject Code</th>
        <th>Subject Name</th>
    </tr>
    <tr>
        <th>1</th>
        <td>19EE404</td>
        <td>Digital Electronics</td>
    </tr>
    <tr>
        <th>2</th>
        <td>19AI414</td>
        <td>Fundamentals of Web Application Development</td>
    </tr>
    <tr>
        <th>3</th>
        <td>19AI302</td>
        <td>Engineering Design and Modelling</td>
    </tr>
    <tr>
        <th>4</th>
        <td>SH3214</td>
        <td>Physics for Quantum Computing</td>
    </tr>
    <tr>
        <th>5</th>
        <td>19AI301</td>
        <td>Python Programming</td>
    </tr>
    <tr>
        <th>6</th>
        <td>19MA201</td>
        <td>Calculas and Matrix Algebra</td>
    </tr>
    <tr>
        <th>7</th>
        <td>19EY708</td>
        <td>Career Development Skills</td>
    </tr>
</table>

</html>    
```
# OUTPUT
![alt text](<Screenshot 2024-12-02 114226.png>)








# RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
