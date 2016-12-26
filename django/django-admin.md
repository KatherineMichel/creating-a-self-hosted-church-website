# Django Admin

One of the most powerful aspects of Django is the ability to easily create an admin interface based on model metadata.

## How It Works

The admin interface is included in the project-level URLs

    url(r'^admin/', admin.site.urls),

The model is imported and registered in the app-level admin.py

    from django.contrib import admin
    from .models import Post

    admin.site.register(Post)

## Logging In

The admin interface URL will be:

    www.domain-name/admin

In order to login, create a superuser username, password and email

    $ python manage.py createsuperuser


