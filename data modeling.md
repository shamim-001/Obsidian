# 17: Introduction to Data Modeling 
![[Pasted image 20230721193422.png]]
![[Pasted image 20230721193451.png]]

- Django automatically create 'id' for each model


# 18: Building an E-commerce Data Model
![[Pasted image 20230826153301.png]]

![[Pasted image 20230826153352.png]]

![[Pasted image 20230826153545.png]]

![[Pasted image 20230826153611.png]]



# 19: Organizing Models in Apps
![[Pasted image 20230826154054.png]]

![[Pasted image 20230826154112.png]]




# 20: Creating Models 
created two models: Product and Customer
`app_store/model.py`
```python
from django.db import models

class Product(models.Model):
    title = models.CharField(max_length=255)
    description = models.TextField()
    price = models.DecimalField(max_digits=10, decimal_places=2)
    inventory = models.IntegerField()
    last_update = models.DateTimeField(auto_now=True)

class Customer(models.Model):
    first_name = models.CharField(max_length=255)
    last_name = models.CharField(max_length=255)
    email = models.EmailField(unique=True)
    phone = models.CharField(max_length=20, unique=True)
    birth_date = models.DateField(null=True)

```


# 21: Choice Fields

`app_store/models.py`
```python
from django.db import models

class Product(models.Model):
    title = models.CharField(max_length=255)
    description = models.TextField()
    price = models.DecimalField(max_digits=10, decimal_places=2)
    inventory = models.IntegerField()
    last_update = models.DateTimeField(auto_now=True)

class Customer(models.Model):
    MEMBERSHIP_CHOICES_BRONZE = 'B'
    MEMBERSHIP_CHOICES_SILVER = 'S'
    MEMBERSHIP_CHOICES_GOLD = 'G'

    MEMBERSHIP_CHOICES = [
        (MEMBERSHIP_CHOICES_BRONZE, 'Bronze'),
        (MEMBERSHIP_CHOICES_SILVER, 'Silver'),
        (MEMBERSHIP_CHOICES_GOLD, 'Gold'),
    ]

    first_name = models.CharField(max_length=255)
    last_name = models.CharField(max_length=255)
    email = models.EmailField(unique=True)
    phone = models.CharField(max_length=20, unique=True)
    birth_date = models.DateField(null=True)
    membership = models.CharField(
        max_length=1, choices=MEMBERSHIP_CHOICES, default=MEMBERSHIP_CHOICES_BRONZE)

class Order(models.Model):
    PAYMENT_STATUS_PENDING = 'P'
    PAYMENT_STATUS_COMPLETE = 'C'
    PAYMENT_STATUS_FAILED = 'F'

    PAYMENT_STATUS_CHOICES = [
        (PAYMENT_STATUS_PENDING, 'Pending'),
        (PAYMENT_STATUS_COMPLETE, 'Complete'),
        (PAYMENT_STATUS_FAILED, 'Failed'),
    ]

    placed_at = models.DateTimeField(auto_now_add=True)
    payment_status = models.CharField(
        max_length=1, choices=PAYMENT_STATUS_CHOICES, default=PAYMENT_STATUS_PENDING)

```


1. `auto_now_add=True`: This option sets the field to the current timestamp when a new instance of the model is created. It's used to track the initial creation time and remains unchanged thereafter.
    
2. `auto_now=True`: This option updates the field to the current timestamp every time the model instance is saved (updated). It's used to track the last modification time.

# 22: Defining One-to-one Relationships 
parent -> child
- primary keys don't allow duplicate value

```python
from django.db import models

class Address(models.Model):
    customer = models.OneToOneField(
        Customer, on_delete=models.CASCADE, primary_key=True)
    street = models.CharField(max_length=255)
    city = models.CharField(max_length=255)
```
- The `Address` model includes a `OneToOneField` named `customer`, which establishes a one-to-one relationship with the `Customer` model. This means that each `Address` instance is associated with a single `Customer` instance.
    
- The `on_delete=models.CASCADE` argument specifies that if the associated `Customer` instance is deleted, the corresponding `Address` instance should also be deleted.


# 23: Defining a One-to-many Relationship 
`collection: models.ForeignKey(Collection,on_delete=models.PROTECT)` -> it means , if you delete the collection, the products will not  be deleted.

- parent class should be defined before the child class.
```python
class Collection(models.Model):
    title = models.CharField(max_length=255)
    description = models.TextField()

    def __str__(self):
        return self.title

class Product(models.Model):
    collection = models.ForeignKey(Collection, on_delete=models.PROTECT)
    # Other fields for Product model

class Order(models.Model):
    customer = models.ForeignKey(Customer, on_delete=models.PROTECT)
    # Other fields for Order model

class OrderItem(models.Model):
    order = models.ForeignKey(
        Order, on_delete=models.PROTECT)
    product = models.ForeignKey(Product, on_delete=models.PROTECT)
    quantity = models.PositiveSmallIntegerField()
    unit_price = models.DecimalField(max_digits=6, decimal_places=2)

    def __str__(self):
        return f"{self.product.title} - {self.quantity}"

```


# 24: Defining Many-to-many Relationships 
Django automatically creates reverse relationship

Django automatically generates reverse query names for ForeignKey and OneToOneField relationships, and how naming conflicts can occur.

Consider the following models:

```python
from django.db import models

class Author(models.Model):
    name = models.CharField(max_length=100)

class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.ForeignKey(Author, on_delete=models.CASCADE)
```

In this example, we have two models: `Author` and `Book`. The `Book` model has a ForeignKey relationship with the `Author` model through the `author` field.

Django automatically generates a reverse query name for the ForeignKey relationship in the `Book` model. The reverse query name is used to access the related objects from the "many" side of the relationship. By default, Django creates this name using the lowercase name of the related model followed by `_set`.

In this case, the reverse query name for the `Book` model's ForeignKey relationship to the `Author` model will be `book_set`.

Now, let's say we add another ForeignKey relationship from the `Author` model to the `Book` model:

```python
class Author(models.Model):
    name = models.CharField(max_length=100)
    featured_book = models.ForeignKey(Book, on_delete=models.SET_NULL, null=True)
```

In this case, Django will generate another reverse query name for the new ForeignKey relationship in the `Author` model. Since both the `Book` model's `author` field and the `Author` model's `featured_book` field point to each other, a naming conflict can occur.

To avoid this naming conflict, you can use the `related_name` attribute to specify a unique reverse query name for one of the ForeignKey relationships. This is exactly what the `related_name` attribute does – it allows you to override the default reverse query name generated by Django.

For example:

```python
class Author(models.Model):
    name = models.CharField(max_length=100)
    featured_book = models.ForeignKey(Book, on_delete=models.SET_NULL, null=True, related_name='featured_authors')

class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.ForeignKey(Author, on_delete=models.CASCADE)
```

In this updated code, the `related_name` attribute `"featured_authors"` is added to the `featured_book` ForeignKey field in the `Author` model. This avoids the naming conflict and provides a clear way to access featured authors from the `Book` model.


A many-to-many relationship is a type of relationship between two models where multiple instances of one model can be associated with multiple instances of another model, and vice versa. This is often used when you have situations where objects of both models can have a "many" relationship with each other.

For example, a product can have multiple promotions and a promotion can have multiple products

# 25: Resolving Circular Relationships 
circular dependency
`related_name="+"` -> it tells django not to create reverse relationship

![[Pasted image 20230828143638.png]]


# 26: Generic Relationships
`from django.contrib.contenttypes.models import ContentType`
- special model for allowing generic relationship

```python
content_type= models.ForeignKey(ContentType,on_delete=models.CASCADE)

object_id = models.PositiveIntegerField()

content_object = GenericForeignKey()
```

