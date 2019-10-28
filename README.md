# supermarket-kata2
kata - on java /springboot env. - output a shoppingbasket
This is a variation of a popular kata described in http://codekata.com/kata/kata01-supermarket-pricing/. 
The aim of the exercise is to build a solution using <b>the TDD methodologie, /relevant pattern</b> to organize the code.
 # Exerice
 ----------
 Please write a program to represent the following scenario:

We are a national supermarket chain that is interested in starting to use special offers in our stores. We stock the following products:
Item	Price (£)
Apple	0.20
Orange	0.50
Watermelon	0.80

We would like to allow the following special offers:
•	Buy One Get One Free on Apples
•	Three For The Price Of Two on Watermelons
We would like to see the output for an example basket containing the following items:
Item	Quantity	Price (£)
Apple	4	0.40
Orange	3	1.5
Watermelon	5	3.2

#Solution :
------------
1/
The solution  is based on th MVC pattern:
the supermarket business data : is in model classes
The supermarket business logic is in service layer
the vew layer is not relevant in this user story.

2/
The solution is guided by the idea of coding minimum classes, with minimum dependances.
To achieve this goal spring-boot is used for bean injection and 
the appropriate offer to apply on a product is  
by using the unique method declared in a functionnal interface - [apply]
a OfferProcessorManager class invok the method apply (from the functionnal 
interface) via a lambda expression on different OfferProcessor classes.

# enry point of the project:
the main class SpringSuperMarketAPP

# Possible improvements
could be done on jUnit tests specially - 
the jUnit tests implemented covers part of the code (the service classes only).
