# Dictionaries

- Dictionaries are used to store data values in key:value pairs.
- A dictionary is a collection which is ordered*, changeable and does not allow duplicates.
- Dictionaries are written with curly brackets, and have keys and values:
- Dictionary items are ordered, changeable, and does not allow duplicates.
- Dictionary items are presented in key:value pairs, and can be referred to by using the key name.
- Dictionaries are changeable, meaning that we can change, add or remove items after the dictionary has been created.
- the values in dictionary items can be of any data type:
- From Python's perspective, dictionaries are defined as objects with the data type 'dict':<br>*<class 'dict'>*
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
~~~

Duplicate values will overwrite existing values:
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "year": 2020
}
print(thisdict) => {'brand': 'Ford', 'model': 'Mustang', 'year': 2020} 
~~~

## Dictionary Length
To determine how many items a dictionary has, use the len() function:
print(len(thisdict))

## Access Dictionary Items
You can access the items of a dictionary by referring to its key name, inside square brackets:
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]
~~~

There is also a method called get() that will give you the same result:
~~~
x = thisdict.get("model")
~~~

## Get Keys
The keys() method will return a list of all the keys in the dictionary.
~~~
x = thisdict.keys() 
~~~

Add a new item to the original dictionary, and see that the keys list gets updated as well:
~~~
car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}
x = car.keys()
print(x) #before the change
car["color"] = "white"
print(x) #after the change 
~~~

## Get Values

The values() method will return a list of all the values in the dictionary.
~~~
x = thisdict.values() 
~~~

Make a change in the original dictionary, and see that the values list gets updated as well:
~~~
car = {
		"brand": "Ford",
		"model": "Mustang",
		"year": 1964
	  }
x = car.values()
print(x) #before the change
car["year"] = 2020
print(x) #after the change 
~~~

## Get Items
The items() method will return each item in a dictionary, as tuples in a list.
~~~
x = thisdict.items() 
~~~

Make a change in the original dictionary, and see that the items list gets updated as well:

~~~
car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}
x = car.items()
print(x) #before the change
car["year"] = 2020
print(x) #after the change 
~~~