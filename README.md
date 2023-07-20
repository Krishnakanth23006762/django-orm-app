# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

### ER Diagram:
![ERDIAGRAM](ERDIAGRAM.jpg)

## DESIGN STEPS

### STEP 1: Create folder 'ex02' under the directory 'unit2'

### STEP 2: Clone the Github repository into the directory 'ex02' using the command "git clone <url>"

### STEP 3: Under the folder "django-orm-app", enter the directory titled "dataproject" and go to the file settings.py

### STEP 4: Return to the parent folder "dataproject" and install the application myapp using the second command "python3 manage.py startapp myapp"

### STEP 5: Under the directory "myapp" open "models.py"


## PROGRAM
### models.py:
```py
from django.db import models
from django.contrib import admin

# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    phonenumber=models.IntegerField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','phonenumber')
    ```
### admin.py
```py
from django.contrib import admin
from .models import Student,StudentAdmin
# Register your models here.
admin.site.register(Student,StudentAdmin)
```
## OUTPUT

### Student List:
![Studentlist](student.PNG)

### error file:
![error](error.PNG)


## RESULT
The program is executed successfully
