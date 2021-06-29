# Django-greenplum

Django ORM third party backend for Greenplum db

## requirements

Django

psycopg2

## use



```python

# Copy the django-greenplum to your porject root dir

DATABASES = {

    'default': {

        'ENGINE': 'django-greenplum',

        'NAME': 'django-test',

        'USER': 'gpadmin',

        'PASSWORD': 'xxxxxx',

        'HOST': '127.0.0.1',

        'PORT': '5432',

    }

}

```



## notice

1. Here we use the primary key as the distribution key by default, and because greenplus does not support multiple unique keys in the same table, please do not define the unique attribute in your model class.

2. Because of the above reasons, the default admin, auth, application will not be used. This problem may be fixed later

