<!--
https://pypi.org/project/readme-generator/
https://pypi.org/project/python-readme-generator/
https://pypi.org/project/django-readme-generator/
-->

[![](https://img.shields.io/pypi/pyversions/django-postgres-dropdb.svg?longCache=True)](https://pypi.org/project/django-postgres-dropdb/)
[![](https://img.shields.io/pypi/v/django-postgres-dropdb.svg?maxAge=3600)](https://pypi.org/project/django-postgres-dropdb/)
[![Travis](https://api.travis-ci.org/andrewp-as-is/django-postgres-dropdb.py.svg?branch=master)](https://travis-ci.org/andrewp-as-is/django-postgres-dropdb.py/)

#### Installation
```bash
$ [sudo] pip install django-postgres-dropdb
```

#### Commands
command|`help`
-|-
`python manage.py dropdb` |drop postgres database

#### Executable modules
usage|`__doc__`
-|-
`python -m django_postgres_dropdb [alias]` |drop postgres database

#### Examples
example 1 - management command:

`settings.py`

```python
INSTALLED_APPS+=['django_postgres_dropdb']

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': os.getenv('DB_NAME'),
        'USER': os.getenv('DB_USER'),
        'PASSWORD': os.getenv('DB_PASS'),
        'HOST': os.getenv('DB_HOST'),
        'PORT': os.getenv('DB_PORT'),
    }
}
```

```bash
$ python manage.py dropdb
$ python manage.py dropdb "default"
```

example 2 - python module cli:

`settings.py`

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': os.getenv('DB_NAME'),
        'USER': os.getenv('DB_USER'),
        'PASSWORD': os.getenv('DB_PASS'),
        'HOST': os.getenv('DB_HOST'),
        'PORT': os.getenv('DB_PORT'),
    }
}
```

```bash
$ export DJANGO_SETTINGS_MODULE=settings
$ python -m django_postgres_dropdb
$ python -m django_postgres_dropdb "default"
```

#### Related projects
+   [django-postgres-createdb](https://pypi.org/project/django-postgres-createdb/)
+   [django-postgres-dropdb](https://pypi.org/project/django-postgres-dropdb/)

<p align="center">
    <a href="https://pypi.org/project/django-readme-generator/">django-readme-generator</a>
</p>