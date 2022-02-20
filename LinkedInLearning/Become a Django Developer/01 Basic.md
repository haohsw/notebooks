## Install Django
- Run command: `python -m pip install Django`
## Create new project
- Run command: `django-admin startproject mysite`
## Create new app
- Run command: `python manage.py startapp app`
## Run server
- Run command: `python manage.py runserver`
## Route
### Config app route in project
- `path('app/', include('app.urls'))`
### Config app route in app
- `path('',  views.index, name='index')`