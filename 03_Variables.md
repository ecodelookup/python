# Variables

Python has no command for declaring variables.<br>
In python variables are created when you assign value to them.<br>
Variable names are case-sensitive.<br>
String variables can be declared either by using single or double quotes<br>


## Variable Names

A variable can have a short name (like x and y) or a more descriptive name (age, carname, total_volume). Rules for Python variables:
- A variable name must start with a letter or the underscore character
- A variable name cannot start with a number
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
- Variable names are case-sensitive (age, Age and AGE are three different variables)

~~~
x = 5
y = "hello"
x = "John"
# is the same as
x = 'John'
~~~


## Casting   
If you want to specify the data type of a variable, this can be done with casting.
~~~
x = str(3)    # x will be '3'
y = int(3)    # y will be 3
z = float(3)  # z will be 3.0 
~~~


## Get The variable type
You can get the data type of a variable with the **type()** function
~~~
x = 5
y = "John"
print(type(x))
print(type(y))
~~~~


## Many Values to Multiple Variables

Python allows you to assign values to multiple variables in one line:
~~~
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
~~~

**Note:** Make sure the number of variables matches the number of values, or else you will get an error.
One Value to Multiple Variables

## Assign the same value to multiple variables in one line:
~~~
x = y = z = "Orange"
print(x)
print(y)
print(z)
~~~


## Unpack a Collection
If you have a collection of values in a list, tuple etc. Python allows you extract the values into variables. This is called unpacking.

~~~
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)
~~~