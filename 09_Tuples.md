# Tuples

- Tuples are used to store multiple items in a single variable.
- A tuple is a collection which is ordered and unchangeable.
- Tuples are written with round brackets.

~~~
thistuple = ("apple", "banana", "cherry")
print(thistuple)
~~~

## Tuple Items

- Tuple items are ordered, unchangeable, and allow duplicate values.
- Tuple items are indexed, the first item has index [0], the second item has index [1] etc.

~~~
thistuple = ("apple", "banana", "cherry", "apple", "cherry")
print(thistuple)
~~~

## Tuple Length
~~~
thistuple = ("apple", "banana", "cherry")
print(len(thistuple))
~~~


## Create Tuple With One Item

To create a tuple with only one item, you have to add a comma after the item, 
otherwise Python will not recognize it as a tuple.
~~~
thistuple = ("apple",)
print(type(thistuple))

#NOT a tuple
thistuple = ("apple")
print(type(thistuple)) 
~~~


## Tuple Items - Data Types 
~~~
tuple1 = ("apple", "banana", "cherry")
tuple2 = (1, 5, 7, 9, 3)
tuple3 = (True, False, False)
~~~

A tuple can contain different data types
~~~
tuple1 = ("abc", 34, True, 40, "male")
~~~


##  tuple() Constructor
~~~
thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets
print(thistuple)
~~~


## Python - Access Tuple Items
### indexing 
You can access tuple items by referring to the index number, inside square brackets:
the first item has index 0
~~~
thistuple = ("apple", "banana", "cherry")
print(thistuple[1])
~~~

### Negative Indexing

Negative indexing means start from the end.
-1 refers to the last item, -2 refers to the second last item etc.
~~~
thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])
~~~

### Range of Indexes

You can specify a range of indexes by specifying where to start and where to end the range.
When specifying a range, the return value will be a new tuple with the specified items.

~~~
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])
# return the third fourth fifth element
# The search will start at index 2 (included) and end at index 5 (not included).

thistuple1 = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple1[2:])
#This example returns the items from "cherry" and to the end:
~~~


### Range of Negative Indexes

~~~
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[-4:-1])
This example returns the items from index -4 (included) to index -1 (excluded)
~~~


### Check if Item Exists
~~~
thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
  print("Yes, 'apple' is in the fruits tuple") 
~~~

## Change Tuple Values
Once a tuple is created, you cannot change its values. 
Tuples are unchangeable, or immutable as it also is called.
But there is a workaround. You can convert the tuple into a list, change the list,
and convert the list back into a tuple.
~~~
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)
print(x)
~~~

### Add Items
~~~
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.append("orange")
thistuple = tuple(y)
~~~

### Remove items
~~~
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.remove("apple")
thistuple = tuple(y)
~~~


## Unpack Tuples
When we create a tuple, we normally assign values to it. This is called "packing" a tuple:
But, in Python, we are also allowed to extract the values back into variables. 
This is called "unpacking":
~~~
fruits = ("apple", "banana", "cherry")
(green, yellow, red) = fruits
print(green)
print(yellow)
print(red)
~~~

### Using the *

If the number of variables is less than the number of values, 
you can add an * to the variable name and the values will be assigned to the variable
as a list:

~~~
fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")
(green, yellow, *red) = fruits
print(green)
print(yellow)
print(red)
~~~

If the asterix is added to another variable name than the last, Python will assign values to the variable 
until the number of values left matches the number of variables left.

~~~
fruits = ("apple", "mango", "papaya", "pineapple", "cherry")
(green, *tropic, red) = fruits
print(green)
print(tropic) => ['mango', 'papaya', 'pineapple']
print(red)
~~~

## Loop Through a Tuple
~~~
thistuple = ("apple", "banana", "cherry")
for x in thistuple:
  print(x)
  
thistuple1 = ("apple", "banana", "cherry")
for i in range(len(thistuple1)):
  print(thistuple[i])   
  
thistuple2 = ("apple", "banana", "cherry")
i = 0
while i < len(thistuple2):
  print(thistuple2[i])
  i = i + 1 
~~~

## Join Tuples
~~~
tuple1 = ("a", "b" , "c")
tuple2 = (1, 2, 3)
tuple3 = tuple1 + tuple2
print(tuple3)
~~~

## Multiply Tuples
~~~
fruits = ("apple", "banana", "cherry")
mytuple = fruits * 2
print(mytuple) => ('apple', 'banana', 'cherry', 'apple', 'banana', 'cherry')
~~~

## Tuple Methods

| Method |	Description |
|--------|--------------|
|count() |	Returns the number of times a specified value occurs in a tuple |
|index() |	Searches the tuple for a specified value and returns the position of where it was found|

