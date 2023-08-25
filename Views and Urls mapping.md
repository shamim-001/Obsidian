![[Pasted image 20230810160927.png]]

- To call the view, we need to map it to a URL

Create a new file in the app_polls folder called `urls.py`

In the `polls/urls.py` file include the following code:
```python
from django.urls import path

from . import views

urlpatterns = [
    path("", views.index, name="index"),
]
```

`mysite/urls.py`
```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path("polls/", include("polls.urls")),
    path("admin/", admin.site.urls),
]
```
