# SEP

Projeto SEP - Sociedade Equestre Portuguesa

https://www.sociedadeequestre.pt


# Instalation Part I - Configuration Base

Create github repositorie

Clone repositorie on VScode

Create virtual environment
py -m venv venv

Enter virtual environment
.\venv\scripts\activate

Upgrade pip
py -m pip install --upgrade pip

Create file requirements.txt
Necessary apps for project
py -m pip install -r .\requirements.txt

Create project Django (the project is created in base folder with dot in the final)
django-admin startproject mysite .

Edit mysite/settins.py
```python
LANGUAGE_CODE = 'pt'
TIME_ZONE = 'Europe/Lisbon'
```

Create database apps - migrate
py manage.py migrate

Initialize server manage.py
py .\manage.py runserver

Open link
http://127.0.0.1:8000/

commit - config_base


# Instalation - Part II - Configuration Users

Create app users
py manage.py startapp users

Edit <project_name>/settins.py
```python
INSTALLED_APPS = [
    # Users apps
    'users.apps.UsersConfig',
]

'DIRS': [ BASE_DIR / "templates" ],

# User Model
AUTH_USER_MODEL = 'users.User'
```

Copy users/admin.py
Copy users/apps.py
Copy users/forms.py
Copy users/models.py

Delete db.sqlite3

Create model - makemigrations
py manage.py makemigrations

Create database apps - migrate
py manage.py migrate

Create super user
py manage.py createsuperuser

commit - config_users


# Instalation - Part III - Configuration App

Create app
py manage.py startapp <app_name>

Edit <project_name>/settins.py
```python
INSTALLED_APPS = [
    # My apps
    '<app_name>.<(A)pp_name>Config',
]
```

Edit <app_name/>models.py
Edit <app_name/>admin.py
Edit <app_name/>views.py
Edit <project_name/>urls.py

commit - config_users


# Requirements

List all requirements
pip freeze

Add all requirements
pip freeze > requirements.txt

Install all requirements
py -m pip install -r .\requirements.txt


# Fixtures

Load fixtures to database
py manage.py loaddata <fixtures>
