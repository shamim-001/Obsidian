#setup 
- [setup](#Setup)
	- [manage.py](#manage.py)
	- [view.py](#view.py)
	- [mapping urls to views](#mapping_urls_to_views)
	- [Using templates](#templates)

[[django rest framework]]

# Setup
install virtual environment
```bash
pip3 install pipenv
```

```bash
pipenv install django
```

```bash
python3 -m django --version
```

-> activate pipenv by running ->
```bash
pipenv shell
```

Create the project folder, 
```bash
django-admin startproject <project name> .
```

```
pip3 freeze
```

```
pip3 freeze > requirements.txt
```

```
pip3 install -r requirements.txt
```

==Setup database==
[[connect postgresql - django]]

for running the project
```bash
python3 manage.py runserver `portnumber(optional)`
```

start app
```bash
python3 manage.py startapp <appname>
```

-> Register the app in project's `settings.py installed app` array

```python
INSTALLED_APPS = [
	...........,
	'app name',
]
```

# view.py
- request -> response
- request handler
- action
```python
from django.shortcuts import render
from django.http import HttpResponse

# Create your views here.

def function_name(request):
	# pull data from db
	# transform data
	# send email etc

def say_hello(request):
	return HttpResponse("Hello django")
```

# mapping_urls_to_views
app folder/ `urls.py` -> 
```python
from django.urls import path
from . import views
#URLConf
urlpatterns = [
	path('hello/',views.say_hello)
]
```
root/ `urls.py`
```python
from django.urls import path,include
urlpatterns = [
	#........#
	path('playground/',include('playground.urls'))
]
```

# templates
`app_folder -> templates folder -> name.html`

`views.py`
```python
def say_hello(request):
	return render(request,'hello.html'{'name':'Shamim'})
```
`hello.html` // double {} for passing variable
```html
	{% if name %}
	<h1>Hello, {{name}}</h1>
	{% else %}
	<h1>Hello Django</h1>
	{% endif %}
```
