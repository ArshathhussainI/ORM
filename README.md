# Ex02 Django ORM Web Application
## Date: 20-11-2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![387142076-e852e084-3662-49ad-8a24-eccc044006a4](https://github.com/user-attachments/assets/13d2e14f-0012-4067-acda-75b414576236)


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
Admins.py
from django.contrib import admin
from .models import loan,loanadmin
admin.site.register(loan,loanadmin)

models.py
from django.db import models
from django.contrib import admin
class loan (models.Model):
    loan_id=models.IntegerField(primary_key=True)
    loan_type =models.CharField(max_length=30)
    loan_amnt =models.FloatField()
    cust_acntno =models.IntegerField()
    cust_name=models.CharField(max_length=50)
 
class loanadmin(admin.ModelAdmin):
    list_display=('loan_id','loan_type','loan_amnt','cust_acntno','cust_name')



## OUTPUT
![Screenshot 2024-11-18 160809](https://github.com/user-attachments/assets/fec1008e-5d42-49b5-93d5-6498592e43d0)

![Screenshot 2024-11-18 161057](https://github.com/user-attachments/assets/c96d607f-fd62-43d7-afd3-716be8dfc77c)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
