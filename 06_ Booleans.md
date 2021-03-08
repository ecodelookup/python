# Python Booleans
Booleans represent one of two values: 'True' or 'False'.
When you run a condition in an if statement, Python returns True or False:

Almost any value is evaluated to True if it has some sort of content.
Any string is True, except empty strings.
Any number is True, except 0.
Any list, tuple, set, and dictionary are True, except empty ones.

~~~
a = 200
b = 33
if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a") 
~~~

The **bool()** function allows you to evaluate any value, 
and give you True or False in return,

~~~
print(bool("Hello"))
print(bool(15))
#evaluate variables
x = "Hello"
y = 15
print(bool(x))
print(bool(y))
~~~

There are not many values that evaluate to False, except empty values, such as (), [], {}, "", 
the number 0, and the value None. And of course the value False evaluates to False.

~~~
bool(False)
bool(None)
bool(0)
bool("")
bool(())
bool([])
bool({}) 
~~~