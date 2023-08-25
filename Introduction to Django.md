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

# lesson_10 
- each app provides certain piece of functionality 
- every time you create an app, you have register it on installed_app [] in `settings.py` file.

# lesson_12: mapping urls to views
# lesson_13: using templates
# lesson_14: Debugging Django Applications in VSCode
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
