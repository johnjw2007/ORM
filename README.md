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
Models:
```
from django.db import models
from django.contrib import admin
class Bank(models.Model):
    customer_id = models.IntegerField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)  
    monthly_interest = models.DecimalField(max_digits=5, decimal_places=2)  
    due_date = models.DateField()

    def __str__(self):
        return self.customer_name  # Optional, for better representation in admin or shell

class BankAdmin(admin.ModelAdmin):
    list_display = ('customer_id', 'customer_name', 'account_type', 'loan_amount', 'monthly_interest', 'due_date')
admin.site.register(Bank, BankAdmin)
```
Admin:
```
from django.contrib import admin
from .models import Bank, Loandetails

admin.site.register(Bank)
admin.site.register(Loandetails)
```
## OUTPUT
![image](https://github.com/user-attachments/assets/b0844099-9af6-49db-ab02-de684681b923)
![image](https://github.com/user-attachments/assets/6f5a99ba-e37f-44e6-a871-3adc188cd4a5)

## RESULT
Thus, the program for creating movie database using ORM has been executed successfully.
