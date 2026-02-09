# Ex01 Django ORM Web Application
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 car

# PROGRAM
models.py
```
from django.db import models
from django.contrib import admin

class Car(models.Model):
    brand = models.CharField(max_length=100)
    model = models.CharField(max_length=100)
    year = models.IntegerField()
    price = models.FloatField()
    body_design = models.CharField(max_length=100)
    drive_type = models.CharField(max_length=100)
    fuel_type = models.CharField(max_length=100)
    seats = models.IntegerField()
    color = models.CharField(max_length=50)
    mileage = models.FloatField()

class CarAdmin(admin.ModelAdmin):
    list_display = ('brand', 'model', 'year', 'price','body_design','drive_type', 'fuel_type','seats','color','mileage')
```
admins.py
```
from django.contrib import admin
from .models import Car,CarAdmin

admin.site.register(Car,CarAdmin)
```

# OUTPUT

<img width="1265" height="668" alt="image" src="https://github.com/user-attachments/assets/8fa52701-7391-4e1a-85c0-3dfbfdf49072" />


# RESULT
Thus the program for creating a database using ORM hass been executed successfully
