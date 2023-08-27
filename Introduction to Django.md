# lesson_5 - Introduction to django
## Django features
- The admin site
- Object-relational Mapper (ORM)
- Authentication
- Cashing

# lesson_6 - How the web works
- Back-end runs on a web server, data processing, validating business logic etc.
- client -> (request) -> server
- server -> (response) -> client
- response can be : html or data in json format
- Server is a gateway to the data
- API is like a remote of a tv

# lesson_10 : creating your first app
[Default django apps functionality](https://chat.openai.com/c/8be53d2b-bf2b-4ae5-9825-322e4194e628)

- each app provides certain piece of functionality 
- every time you create an app, you have register it on installed_app [] in `settings.py` file.

```python
python3 manage.py startapp app_playground
```

### the functionality of each file and folder in a default Django app:
[Chatgpt link](https://chat.openai.com/c/2a5bce75-a56c-4233-bd00-7c3c44c094cb)

1. **`/__init__.py`**: An empty file that signifies the directory as a Python package, allowing it to be imported and recognized as a module.

2. **`/admin.py`**: In this file, you register the application's models to make them accessible and manageable through the Django admin interface.

3. **`/apps.py`**: This file contains configuration settings for the app, including metadata such as its human-readable name.

4. **`/models.py`**: In this file, you define the data models using Django's ORM. Models represent database tables, and their fields define the table's columns.

5. **`/tests/`**: This folder is meant for writing unit tests to ensure your app's functionality is working as expected and remains stable during development.

6. **`/views.py`**: Define views in this file. Views handle incoming HTTP requests, process the data, and return appropriate responses, often in HTML format.

7. **`/urls.py`**: Here, you define the URL patterns for your app. It maps specific URLs to their corresponding views, directing the flow of user requests.

8. **`/migrations/`**: Django automatically generates and manages this folder. It stores scripts that apply changes to the database schema as you modify your models, helping you keep the database structure synchronized with code changes.

# 11: Creating views

![[Pasted image 20230826152318.png]]

# lesson_15: Using Django Debug Toolbar 
[django-debug-toolbar-installation](https://django-debug-toolbar.readthedocs.io/en/latest/installation.html)

make sure your pipenv is activated
```bash
pipenv install django-debug-toolbar
```

`settings.py`
```python
INSTALLED_APPS = [
    # ...
    "debug_toolbar",
    # ...
]

MIDDLEWARE = [
    # ... on the top
    "debug_toolbar.middleware.DebugToolbarMiddleware",
    # ...
]

INTERNAL_IPS = [
    # ...
    "127.0.0.1",
    # ...
]
```

project folder/`urls.py`
```python
import debug_toolbar

urlpatterns = [
    # ...
    path("__debug__/", include("debug_toolbar.urls")),
]
```
