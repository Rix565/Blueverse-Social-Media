# Blueverse

Your personal discussion and interaction platform, with a Miiverse look!

# Install

This is a classical Django application. It can be used on reverse proxies, WSGI, and more.
## Requirements
You need a UNIX system. (fuck Windows)

You need:
- Python 3.7+
- PIP3
- Git
- (optional but recommended) a MySQL/Postgres SQL Server.
- A shell access.

Modules:
```
pip3 install Django urllib3 lxml passlib bcrypt pillow django-markdown-deux django-markdown2
```
After this step is done, you can start getting and configuring the server.
## Cloning the repository & configuring the server
Clone this repository using git:

```
git clone https://github.com/Rix565/Blueverse-Social-Media/
```

After this, go under the Blueverse-Social-Media/closedverse directory and open the settings.py file.

This is where you will configure your instance of Blueverse.

By default it uses a SQLite3 database, but it is strongly encouraged to switch under MySQL/Postgres, which you can do <a href="https://docs.djangoproject.com/fr/4.0/ref/databases/">there.</a>


Now let's move to the interesting part: the actual installation part!
## Install

First, let's start by setting up the database (you must have configured it in closedverse/settings.py):
```
python3 manage.py makemigrations
python3 manage.py makemigrations ban
python3 manage.py makemigrations closedverse_main
python3 manage.py migrate
```
Second, let's create your super-admin account so that you can manage your own instance:
```
python3 manage.py createsuperuser
```

Follow the on-screen instructions.

Now we can finally start the server as a standalone application:
```
python3 manage.py runserver
```
Go to the URL precised by the server output, and here you go! Your instance is online!

You can also switch under a reverse-proxy & WSGI server & everything that is compatible with Django, but I'll let you search this on Google.

# Other projects that this is based on

This is based on <a href="https://github.com/ArianKordi/Closedverse">Closedverse</a>, a Miiverse Clone from 2017.
