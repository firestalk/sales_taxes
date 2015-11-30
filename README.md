# Sales Taxes problem solution

The Problem
---

Basic sales tax is applicable at a rate of 10% on all goods, except books, food, and medical 
products that are exempt. Import duty is an additional sales tax applicable on all imported goods 
at a rate of 5%, with no exemptions. 
  
When I purchase items I receive a receipt which lists the name of all the items and their price 
(including tax), finishing with the total cost of the items, and the total amounts of sales taxes 
paid.  The rounding rules for sales tax are that for a tax rate of n%, a shelf price of p contains 
(np/100 rounded up to the nearest 0.05) amount of sales tax. 
  
Write an application that prints out the receipt details for these shopping baskets... 
  
Input: 
  
Input 1: 

1 book at 12.49 

1 music CD at 14.99 

1 chocolate bar at 0.85 
  

Input 2: 

1 imported box of chocolates at 10.00 

1 imported bottle of perfume at 47.50 
  

Input 3: 

1 imported bottle of perfume at 27.99 

1 bottle of perfume at 18.99 

1 packet of headache pills at 9.75 

1 box of imported chocolates at 11.25 
  
Output: 
  
Output 1: 

1 book : 12.49 

1 music CD: 16.49 

1 chocolate bar: 0.85 

Sales Taxes: 1.50 

Total: 29.83 
  
Output 2: 

1 imported box of chocolates: 10.50 

1 imported bottle of perfume: 54.65 

Sales Taxes: 7.65 

Total: 65.15 
  
Output 3: 

1 imported bottle of perfume: 32.19 

1 bottle of perfume: 20.89 

1 packet of headache pills: 9.75 

1 imported box of chocolates: 11.85 

Sales Taxes: 6.70 

Total: 74.68 

========== 


Actually, as this problem is  not so big, there are only two classes and few first-class functions.
___

Design Aspect
---
As this problem is quite simple, I decided to write an item class to store it's attributes, and class that represents shopping cart to add items and calculate totals. At least, it was quite obvious to me.

Some first-class functions are used in two classes at one time, so they was placed separately of this classes.

Catalog with items was stored in separate file (data/catalog.json) to make it simple to modify in future. JSON-format was used because it is wery similar to python dictionary (in our case).
___

Usage
---
Only standard library was used, so to run this solution, you need only **Python 3**.

Go to directory where *sales_taxes.py* and *sales_taxes_tests.py* files stored.

To run tests, type ```python3 sales_taxes_tests.py``` first. Add ```-v``` argument if you want verbosity.

To run solution, type ```python3 sales_taxes.py [PATH TO ORER FILE]```, for example:

To test input 1: ```python3 sales_taxes.py data/order_1.txt```

To test input 2: ```python3 sales_taxes.py data/order_2.txt```

To test input 3: ```python3 sales_taxes.py data/order_3.txt```

Additionally, *test_order.txt* file was added to demonstrate parsing file with spaces.
