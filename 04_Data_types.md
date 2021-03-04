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