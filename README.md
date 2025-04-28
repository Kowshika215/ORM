# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



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

Model Program
```
from django.db import models

class bankloan(models.Model):
    loan_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=20)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    loan_term = models.IntegerField()
    interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
```
Admin Program
```
from django.contrib import admin
from .models import bankloan

class BankLoanAdmin(admin.ModelAdmin):
    list_display = ('loan_id', 'customer_name', 'account_type', 'loan_amount', 'loan_term', 'interest_rate')
    list_filter = ('account_type', 'loan_term')
    search_fields = ('customer_name', 'account_type')

admin.site.register(bankloan, BankLoanAdmin)
```

## OUTPUT

![Screenshot 2025-04-28 192739](https://github.com/user-attachments/assets/ebd437a8-250d-4404-92de-7c92d7c813d9)



## RESULT
Thus the program for creating movies database using ORM hass been executed successfully
