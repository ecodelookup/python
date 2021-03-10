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


## Check if Key Exists

To determine if a specified key is present in a dictionary use the in keyword:

~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
if "model" in thisdict:
  print("Yes, 'model' is one of the keys in the thisdict dictionary") 
~~~

## Change Dictionary Items
You can change the value of a specific item by referring to its key name:
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["year"] = 2018
~~~

### Update()
the update() method will update the dictionary with the items from the given argument.
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})
~~~

### Adding items
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["sdf"]="dsaff"
print(thisdict)
~~~

## Removing Items

### pop()
The pop() method removes the item with the specified key name:
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model")
print(thisdict) 
~~~
### popitem()

The popitem() method removes the last inserted item 
(in versions before 3.7, a random item is removed instead):
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.popitem()
print(thisdict) 
~~~

### del

The del keyword removes the item with the specified key name:
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict["model"]
print(thisdict) 
~~~

The del keyword can also delete the dictionary completely:
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict
print(thisdict) #this will cause an error because "thisdict" no longer exists. 
~~~
### clear()

the clear() method empties the dictionary:
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.clear()
print(thisdict) 
~~~


## Loop Dictionaries
You can loop through a dictionary by using a for loop.
When looping through a dictionary, 
the return value are the keys of the dictionary, 
but there are methods to return the values as well.
~~~
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

# for keys in the dictionaries
for x in thisdict:
  print(x) 
  
# for values in the dictionaries
for x in thisdict:
  print(thisdict[x]) 
 
# for values
for x in thisdict.values():
  print(x) 
  
# for keys 
for x in thisdict.keys():
  print(x) 
  
# Loop through both keys and values, by using the items() method:
for x, y in thisdict.items():
  print(x, y) 
  
~~~


