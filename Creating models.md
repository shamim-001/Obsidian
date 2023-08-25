```bash
python3 manage.py migrate
```

From now whenever you create or modify the `models.py` file, run the following two commands ->
```bash
python3 manage.py makemigrations
```

```bash
python3 manage.py migrate
```

`app_polls/models.py` ->
```python
from django.db import models


class Question(models.Model):
    question_text = models.CharField(max_length=200)
    pub_date = models.DateTimeField("date published")


class Choice(models.Model):
    question = models.ForeignKey(Question, on_delete=models.CASCADE)
    choice_text = models.CharField(max_length=200)
    votes = models.IntegerField(default=0)
```

