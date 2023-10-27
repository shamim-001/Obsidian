[[django setup]]
# URLs, Views, templates
- Each time a user types in a URL, the request passes through urls.py and sees whether the URL matches any defined paths so that the Django server can return an appropriate response.

client request -> `ulrs.py` <- Response object returned from (`view.py`)

- the view contains the business logic or the "what."
- The URLs control the route and entry point into a page.
- such as the main ' ' path (the URL), which links to the
`movieViews.home` (view) function that returns the `home.html` (template) code.

When a user types a URL into the browser, sends a request to our site, goes through `urls.py`, connects to a Django view, and our Django server uses a template to respond with HTML.

## Passing data into templates
```python
def home(request):
return render(request, 'home.html', {'name':'Greg
Lim'})
```
In `home.html` {{ name }} accesses the 'name' key in the dictionary and thus retrieves the 'Greg Lim' value.

# action in form element
For input, we specify `name="searchMovie"` to reference the input and retrieve its value. We have action=" " in the form tag. The empty " " string specifies that upon clicking on submit, we submit the form to the same page – that is, home.html. If we want to submit the form to another page – for example, the about page – we will have `<form action="{% url 'about' %}">`.

By default, a form submission sends a GET request if the type of request is not specified. Thus, we access the request with request.GET and specify the name of the input field, searchMovie – that is, request.GET.get('searchMovie') – to get the input value.

# Django model
- Each model is a class that extends `django.db.models.Model`.
- Each model attribute represents a database column.
- With all of this, Django provides us with a set of useful methods to create, update, read, and delete (CRUD) model information from a database.

We assign CharField to both title and description. image is of ImageField, and we specify the upload_to option to specify a subdirectory of MEDIA_ROOT (found in settings.py) to use for uploaded images. url is of URLField, a CharField for a URL. Because not all movies have URLs, we specify blank=True to indicate that this field is optional.

`pillow` adds image processing capabilities to our Python interpreter.

### Accessing the Django admin interface
```bash
python3 manage.py createsuperuser
```

### Configuring for images 
`settings.py`
```python
import os

MEDIA_ROOT = os.path.join(BASE_DIR,'media')
MEDIA_URL = '/media/'
```

### Serving the stored images
`project/urls.py`
```python
from django.conf.urls.static import static
from django.conf import settings
urlpatterns = [
…
]
urlpatterns += static(settings.MEDIA_URL,document_root=settings.MEDIA_ROOT)
```

# Displaying Objects from Admin
```python
from .models import Movie
def home(request):
	searchTerm = request.GET.get('searchMovie')
	movies = Movie.objects.all()
	return render(request, 'home.html',
	{'searchTerm':searchTerm, 'movies': movies})
```

