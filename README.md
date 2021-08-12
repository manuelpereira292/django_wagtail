# django_wagtail

Testing Django With Wagtail

# Instalation Part I - Configuration Base

Create github repositorie

Clone repositorie on VScode

Create virtual environment
py -m venv venv

Enter virtual environment
.\venv\scripts\activate

Upgrade pip
py -m pip install --upgrade pip

pip install wagtail

pip install wagtail --upgrade

Create project Wagtail (the project is created in base folder with dot in the final)
wagtail start mysite .

Create file requirements.txt
Necessary apps for project
py -m pip install -r .\requirements.txt

Edit mysite/settins.py
```python
LANGUAGE_CODE = 'pt'
TIME_ZONE = 'Europe/Lisbon'
```

Create database apps - migrate
py manage.py migrate

Initialize server manage.py
py .\manage.py runserver

Create super user
py manage.py createsuperuser

Open link
http://127.0.0.1:8000/

commit - config_base
