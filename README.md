<img src="https://github.com/mynameisone/Ecom/blob/master/images/Phoenix.png?raw=true" align="right" height="150"/>

# Unio [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome#readme)

**This is unio where all the nerds catch up =)**

## To create a project
Type _django-admin startproject project_name_ in a terminal then once the location of a terminal is inside project_nime folder type _django-admin startapp accounts_ to create an accounts foulder then create static and templates folder.

## To connect to a db
Type _pip install version_of_requirement_for_your_system.whl_ in a terminal then _pip install mysqlclient_ and then check if everything is fine by typing _python manage.py check_ if no issues, then migrate by typing _python manage.py migrate_ and then run the server.

## To have a simple view:
To avoid some warnings insert _"python.analysis.disabled": [
        "unresolved-import"
    ]_ into settings.json in .vscode
```
## view.py
from django.views.generic import TemplateView

class HomePage(TemplateView):
    template_name = 'index.html'

# urls.py
from django.conf.urls import url, include
from django.urls import path
from django.contrib import admin
from . import views

urlpatterns = [
    url(r'^admin/', admin.site.urls),
    url(r'^$', views.HomePage.as_view(), name='home')
]
```

## Some features of the website: 
 * Groups (similar to subreddits)
 * Multiple Users and Authorizations
 * Posts in groups (similar to a tweet)
 * Linking user profiles with @ symbol.
 * Multiple applications.