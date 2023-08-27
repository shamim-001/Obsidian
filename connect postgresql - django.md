#django-packages #django-postgres 
[install postgresql](https://youtu.be/tducLYZzElo)

------------------------------------------------

```
pip3 install psycopg2-binary
```

create a database named `multivendor_ecommerce` or any other in the `pgAdmin4`

`settings.py`:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'storefront',
        'USER': 'postgres',
        'PASSWORD': 'root',
        'HOST': 'localhost',
    }
}
```

run `python3 manage.py runserver`