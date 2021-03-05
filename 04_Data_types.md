# DATA TYPES 

## Built-in Data Types

Python has the following data types built-in by default, in these categories

|Type               | identifier                  |
|-------------------|-----------------------------|
|Text Type: 		|str                          |
|Numeric Types: 	|int, float, complex          |
|Sequence Types: 	|list, tuple, range           |
|Mapping Type: 		|dict                         |
|Set Types: 		|set, frozenset               |
|Boolean Type: 		|bool                         |
|Binary Types: 		|bytes, bytearray, memoryview |

- you can get the data type of any object by using the type() function:

### String 
~~~
x = "Hello World"
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### integer
~~~
x = 20
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### float 
~~~
x = 20.5
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### complex
~~~
x = 1j
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### List
~~~
x = ["apple", "banana", "cherry"]
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### Tuple
~~~
x = ("apple", "banana", "cherry")
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### Range 
~~~
x = range(6)
#display x:
print(x)
#display the data type of x:
#print(type(x)) 
~~~

### Dictionary
~~~
x = {"name" : "John", "age" : 36}
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### set 
~~~
x = {"apple", "banana", "cherry"}
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### frozenset
~~~
x = frozenset({"apple", "banana", "cherry"})
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### bool
~~~
x = True
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### byte 
~~~
x = b"Hello"
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### bytearray
~~~
x = bytearray(5)
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

### memory view
~~~
x = memoryview(bytes(5))
#display x:
print(x)
#display the data type of x:
print(type(x)) 
~~~

## Python Numbers

There are three numeric types in Python:
- int
- float
- complex
~~~
x = 1    # int
y = 2.8  # float
z = 1j   # complex
~~~

### Int

Int, or integer, is a whole number, positive or negative, 
without decimals, of unlimited length.
~~~
x = 1
y = 35656222554887711
z = -3255522
print(type(x))
print(type(y))
print(type(z))
~~~

### Float

Float, or "floating point number" is a number, 
positive or negative, containing one or more decimals
Float can also be scientific numbers with an "e" to indicate the power of 10.
~~~
x = 1.10
y = 1.0
z = -35.59
x = 35e3
y = 12E4
z = -87.7e100
~~~

### Complex

Complex numbers are written with a "j" as the imaginary part:
~~~
x = 3+5j
y = 5j
z = -5j
print(type(x))
print(type(y))
print(type(z)) 
~~~

## Type Conversion

- int() - constructs an integer number from an integer literal, a float literal (by removing all decimals), or a string literal (providing the string represents a whole number)
- float() - constructs a float number from an integer literal, a float literal or a string literal (providing the string represents a float or an integer)
- str() - constructs a string from a wide variety of data types, including strings, integer literals and float literals

You can convert from one type to another with the int(), float(), and complex() methods:
~~~
x = 1    # int
y = 2.8  # float
z = 1j   # complex

#convert from int to float:
a = float(x)

#convert from float to int:
b = int(y)

#convert from int to complex:
c = complex(x)

print(a)
print(b)
print(c)

print(type(a))
print(type(b))
print(type(c))
~~~


## Random Number
Python does not have a random() function to make a random number, 
but Python has a built-in module called random that can be used to make random numbers:
~~~
import random
print(random.randrange(1, 10))
~~~