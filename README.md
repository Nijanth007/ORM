# Ex02 Django ORM Web Application
## Date: 24-09-2025

## AIM
To develop a Django application to store and retrieve data from Car Inventory Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

<img width="931" height="500" alt="image" src="https://github.com/user-attachments/assets/63aa7363-720f-423a-bfe0-d0688bced95e" />


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

models.py

```
from django.db import models

# Create your models here.
class Car(models.Model):
    id = models.IntegerField(primary_key=True)
    brand = models.CharField(max_length=15)
    model =models.CharField(max_length=30)
    year = models.DateField()
    price = models.IntegerField()
    type = models.CharField(max_length=10)

```

admin.py

```
from django.contrib import admin
from .models import Car
# Register your models here.

admin.site.register(Car)

class CarAdmin(admin.ModelAdmin):
    list_display = ('id','brand','model','year','price')
```

## OUTPUT

![WhatsApp Image 2025-09-23 at 21 36 28_a1a93a57](https://github.com/user-attachments/assets/caf7a273-7f82-47ac-99bf-3c1e7e3b3500)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
