# set up django project
```md
mkdir <project folder name>

cd project folder

code .
```
- [x] 
```py
python3 -m venv .venv
```
- [x] 
```py
.venv/bin/activate
```
- [x] 
```py
python3 -m pip install django djangorestframework
```
- [x] 
```
pip freeze > requirements.txt
```
- [x] 
```
pip install -r requirements.txt
```
- [x] 
```
django-admin startproject <<name>> .
```
- [x] 
Every app name should be unique
```
python3 manage.py startapp <<name>>
```

- [x] Again
```py
python3 -m pip install django djangorestframework
```

- [x] 
// Run the following 2 cmd whenever you make change in model.py file
```py
python3 manage.py migrate
```
- [x] 
```py
python3 manage.py makemigrations
```
- [x] 
```
python3 manage.py createsuperuser
```
- [x] 
project>settings.py 
```
INSTALLED_APPS = [
    "app_name",
    . . . 
]
```

project's urls.py in project_name/urls.py

- [x] 
```py
python3 manage.py runserver
```
