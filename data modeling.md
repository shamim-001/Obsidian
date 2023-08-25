[Go to](###here)

# 17: Introduction to Data Modeling 
![[Pasted image 20230721193422.png]]
![[Pasted image 20230721193451.png]]

- Django automatically create 'id' for each model


# 18: Building an E-commerce Data Model

# 19: Organizing Models in Apps
# 20: Creating Models 
created two models: Product and Customer

# 21: Choice Fields

# 22: Defining One-to-one Relationships 
parent -> child

# 23: Defining a One-to-many Relationship 
`collection: models.ForeignKey(Collection,on_delete=models.PROTECT)` -> it means , if you delete the collection, the products will not  be deleted.

- parent class should be defined before the child class.

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

