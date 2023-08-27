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
Django creates reverse relationship

# 25: Resolving Circular Relationships 
circular dependency
`related_name="+"` -> it tells django not to create reverse relationship

# 26: Generic Relationships
`from django.contrib.contenttypes.models import ContentType`
- special model for allowing generic relationship

```python
content_type= models.ForeignKey(ContentType,on_delete=models.CASCADE)

object_id = models.PositiveIntegerField()

content_object = GenericForeignKey()
```

