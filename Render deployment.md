#deployment 
https://youtu.be/AgTr5mw4zdI

https://dashboard.render.com/

# Database
- after creating database, copy external database link
`project/urls.py`
```python
from django.contrib.staticfiles.urls import staticfiles_urlpatterns

urlpatterns += staticfiles_urlpatterns()
```

```bash
pip3 install dj-database-url gunicorn django-environ python-dotenv
```

```bash
pip3 freeze > requirements.txt
```

`project/settings.py`
```python
import dj_database_url

from dotenv import load_dotenv 
load_dotenv()

import environ
env = environ.Env()
environ.Env.read_env()

SECRET_KEY = os.environ.get("SECRET_KEY")

ALLOWED_HOSTS = ['*']
DEBUG = False

DATABASES = {
	'default': dj_database_url.parse(env("DATABASE_URL"))
}


```

`root_directory/.env` and `.env` should be included in `gitignore` file
```python
DATABASE_URL = external_url
SECRET_KEY = django-insecure-v64li3)j@vn-=16_ng7oj4*)f08q0g0m#xcr8d1e_vr16+ic&g
```

```bash
python3 manage.py migrate
```

- create superuser

# Web service
// Start command
```
gunicorn moviereviews.wsgi:application
```

> Advanced
![[Pasted image 20230924152323.png]]
