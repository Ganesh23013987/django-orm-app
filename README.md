# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Install myapp using 'python manage py startapp [your app name]   command

### STEP 2:
First edit 'setting.py'and then edit 'models.py'and then edit 'admin.py'with the appropriate codes.

### STEP 3:
Create a user name and password using for your django 'python manage.py createsuperuser'
and then run the program using 'python manage.py runserver[your port number]'

### STEP 4:
login with your username and password in django and select student table and then add 10 students details.

### STEP 5:
End the program

## PROGRAM:
## code to write in models.py
```
from django.db import models
from django.contrib import admin

# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    number=models.IntegerField()

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','number')

```
## program to write in admin.py 
```
from django.contrib import admin
from .models import Student,StudentAdmin

# Register your models here.
admin.site.register(Student,StudentAdmin)
```

## OUTPUT
![image](https://github.com/Ganesh23013987/django-orm-app/assets/147473768/60364a56-5901-4b84-b50b-bb5f41c6e472)

## RESULT:
Then, the program is successfully executed.
