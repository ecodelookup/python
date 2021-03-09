# SET

- Sets are used to store multiple items in a single variable.
- A set is a collection which is both unordered and unindexed.
- Sets are written with curly brackets.
- Sets are unchangeable, meaning that we cannot change the items after the set has been created.
- Sets cannot have two items with the same value.Duplicate values will be ignored.
- From Python's perspective, sets are defined as objects with the data type 'set'.<br> **\<class 'set'\>**

~~~
thisset = {"apple", "banana", "cherry"}
print(thisset) 
~~~

Set items can be of any data type:
~~~
set1 = {"apple", "banana", "cherry"}
set2 = {1, 5, 7, 9, 3}
set3 = {True, False, False} 
~~~

## length of set
~~~
thisset = {"apple", "banana", "cherry"}
print(len(thisset)) 
~~~

## set() Constructor

~~~
thisset = set(("apple", "banana", "cherry")) # note the double round-brackets
print(thisset) 
~~~

## Accessing the set items

You cannot access items in a set by referring to an index or a key.
But you can loop through the set items using a for loop, 
or ask if a specified value is present in a set, by using the in keyword.
~~~
thisset = {"apple", "banana", "cherry"}
for x in thisset:
  print(x) 
~~~

Check if "banana" is present in the set:
~~~
thisset = {"apple", "banana", "cherry"}
print("banana" in thisset) 
~~~

## Change Items
Once a set is created, you cannot change its items, but you can add new items.

## Add Items
To add one item to a set use the add() method.
~~~
thisset = {"apple", "banana", "cherry"}
thisset.add("orange")
print(thisset) 
~~~

## Add Sets
To add items from another set into the current set, use the update() method.
~~~
thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}
thisset.update(tropical)
print(thisset) 
~~~

## Add Any Iterable
The object in the update() method does not have be a set, 
it can be any iterable object (tuples, lists, dictionaries etc.).
~~~
thisset = {"apple", "banana", "cherry"}
mylist = ["kiwi", "orange"]
thisset.update(mylist)
print(thisset) 
~~~

## Remove items
To remove an item in a set, use the remove(), or the discard() method.
If the item to remove does not exist, remove() will raise an error.
If the item to remove does not exist, discard() will NOT raise an error.
~~~
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana")
print(thisset)

thisset1 = {"apple", "banana", "cherry"}
thisset1.discard("banana")
print(thisset1) 
~~~

You can also use the pop() method to remove an item,
but this method will remove the last item. 
Remember that sets are unordered, so you will not know what item that gets removed.
The return value of the pop() method is the removed item.
~~~
thisset = {"apple", "banana", "cherry"}
x = thisset.pop()
print(x)
print(thisset)
~~~

### clear()

The clear() method empties the set:
~~~
thisset = {"apple", "banana", "cherry"}
thisset.clear()
print(thisset) 
~~~

### The del keyword will delete the set completely:
The del keyword will delete the set completely:
~~~
thisset = {"apple", "banana", "cherry"}
del thisset
print(thisset) 
~~~

## Loop Items

~~~
thisset = {"apple", "banana", "cherry"}
for x in thisset:
  print(x) 
~~~

## Join Sets

### Join Two Sets
You can use the union() method that returns a new set containing 
all items from both sets, or the update() method that inserts all
the items from one set into another:
~~~
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}
set3 = set1.union(set2)
print(set3) 
~~~

The update() method inserts the items in set2 into set1:
~~~
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}
set1.update(set2)
print(set1) 
~~~

=> Both union() and update() will exclude any duplicate items

### Keep ONLY the Duplicates

The intersection_update() method will keep only the items that are present in both sets.
~~~
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
x.intersection_update(y)  => {'apple'} 
print(x) 
~~~


The intersection() method will return a new set, that only contains the 
items that are present in both sets.
Return a set that contains the items that exist in both set x, and set y:

~~~
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
z = x.intersection(y)
print(z) 
~~~


### Keep All, But NOT the Duplicates

The symmetric_difference_update() method will keep only the 
elements that are NOT present in both sets.
~~~
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
x.symmetric_difference_update(y)
print(x) => {'google', 'banana', 'microsoft', 'cherry'} 
~~~

The symmetric_difference() method will return a new set, 
that contains only the elements that are NOT present in both sets.
~~~
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
z = x.symmetric_difference(y)
print(z) 
~~~



