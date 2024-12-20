# Problem Description
The basic function of an ATM machine is, you insert your card and pin, if the pin matches, it lets you withdraw money from your account and deducts the same from your account. Don't forget to handle cases like insufficient balance and no cash available. The more realistic ATM model you build the better.

# Solution Overview
## ATM_simple 
A user is asked for account number and pin. Which is passed to ATM class. Here in each method we need to check whether account exists and is the user authenticated means he is using correct pin. 

## ATM_with_call_method
__call__() gets called before every method call we need to add a logic here to exclude methods where we want to bypass. This is hard to maintain in long term as developer may forget to add the check when they add new methods.

## ATM_with_decorator
In simple there is quite a bit of redundant code in each method of ATM class. So we use a decorator which is called before all the methods with @pre_method_call annotation. This is quite clean solution as we do not want the login method call to be intercepted. We need it only before deposit and withdrawl.
