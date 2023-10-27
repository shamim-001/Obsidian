#setup 

# Setup
1. **Install the Python3 venv module.**

```
sudo apt install python3-venv
```

2. **Create a new directory for your Django project.**

```
mkdir my_django_project
cd my_django_project
```

3. **Create a virtual environment for your project.**

```
python3 -m venv .venv
```

4. **Activate the virtual environment.**

```
source .venv/bin/activate
```

5. **Install Django.**

```
pip3 install django django-jazzmin
```

6. **Verify that Django is installed correctly.**

```
python3 -m django --version
```

```
deactivate
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
# install packages
[[django rest framework and Related packages]]

# Create database
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
