#deployment 
# packages
```bash
pip3 install dj-database-url
```

`settings.py`
```python
DEBUG = False
ALLOWED_HOSTS = ['.vercel.app']

```

`wsgi.py`
```python
app = application
```

`vercel.json`
```json
{
  "builds": [
    {
      "src": "moviereviews/wsgi.py",
      "use": "@vercel/python",
      "config": { "maxLambdaSize": "15mb", "runtime": "python3.9" }
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "moviereviews/wsgi.py"
    }
  ]
}

```

# Django project links

https://moviereview-app.vercel.app/

