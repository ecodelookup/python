# Lists

- Lists are used to store multiple items in a single variable.
- List items are ordered, changeable, and allow duplicate values.
- List items are indexed, the first item has index [0], the second item has index [1] etc.
- When we say that lists are ordered, it means that the items have a defined order, and that order will not change.If you add new items to a list, the new items will be placed at the end of the list.
- The list is changeable, meaning that we can change, add, and remove items in a list after it has been created.
- Since lists are indexed, lists can have items with the same value:
~~~
thislist = ["apple", "banana", "cherry", "apple", "cherry"]
print(thislist)
print(thislist[1])
print(type(mylist))
~~~

- To determine how many items a list has, use the len() function:
~~~
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
~~~

- List items can be of any data type and A list can contain different data types:
~~~
list1 = ["apple", "banana", "cherry"]
list2 = [1, 5, 7, 9, 3]
list3 = [True, False, False]
list4 = ["abc", 34, True, 40, "male"]
~~~

## list() Constructor
it is also possible to use the list() constructor when creating a new list.
~~~
thislist = list(("apple", "banana", "cherry")) # note the double round-brackets
print(thislist)
~~~

## Access Items
List items are indexed and you can access them by referring to the index number.
- The first item has index 0.
- Negative indexing means start from the end , -1 refers to the last item, -2 refers to the second last item etc.
- You can specify a range of indexes by specifying where to start and where to end the range. 
When specifying a range, the return value will be a new list with the specified items.

~~~
thislist = ["apple", "banana", "cherry"]
print(thislist[1])
print(thislist[-1])

thislist1 = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist1[2:5])
#The search will start at index 2 (included) and end at index 5 (not included).
print(thislist[:4]) # start to 3rd value 
print(thislist[2:]) # second to last value
print(thislist[-4:-1]) # 4th last to end
~~~

## Check if Item Exists
To determine if a specified item is present in a list use the in keyword:
~~~
thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list") 
~~~
## Change Item Value

To change the value of a specific item, refer to the index number:
~~~
thislist = ["apple", "banana", "cherry"]
thislist[0] = "blackcurrant"
thislist[1:3] = ["blackcurrant", "watermelon"]
print(thislist)
~~~

- If you insert more items than you replace, the new items will be inserted where you specified, 
and the remaining items will move accordingly:
~~~
thislist = ["apple", "banana", "cherry"]
thislist[1:2] = ["blackcurrant", "watermelon"]
print(thislist) => ['apple', 'blackcurrant', 'watermelon', 'cherry']
~~~

- If you insert less items than you replace,
the new items will be inserted where you specified, 
and the remaining items will move accordingly:
~~~
thislist = ["apple", "banana", "cherry"]
thislist[1:3] = ["watermelon"]
print(thislist)
~~~

## Insert Items
To insert a new list item, without replacing any of the existing values, 
we can use the insert() method.
the insert() method inserts an item at the specified index:
~~~
thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist) => ['apple', 'banana', 'watermelon', 'cherry']
~~~

## Append Items
To add an item to the end of the list, use the append() method:
~~~
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist) => ['apple', 'banana', 'cherry', 'orange']
~~~

## Extend List
To append elements from another list to the current list, use the extend() method. <br>
The extend() method does not have to append lists, you can add any iterable object (tuples, sets, dictionaries etc.).
~~~
thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]
thislist.extend(tropical)
print(thislist)

thislist1 = ["apple", "banana", "cherry"]
thistuple = ("kiwi", "orange")
thislist1.extend(thistuple)
print(thislist1)
~~~

## Remove List Items

### Remove Specified Item
~~~
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)
~~~

### Remove Specified Index
~~~
thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)
~~~
- If you do not specify the index, the pop() method removes the last item.
~~~
thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)
~~~

- The **del** keyword also removes the specified index:
~~~
thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)
~~~

- the del keyword can also delete the list completely.
~~~
thislist = ["apple", "banana", "cherry"]
del thislist 
~~~

## Clear the List

The clear() method empties the list.
~~~
thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)
~~~


## Loop Through a List

- You can loop through the list items by using a for loop:
~~~
thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x) 
~~~

- Use the range() and len() functions to create a suitable iterable.
~~~
thislist = ["apple", "banana", "cherry"]
for i in range(len(thislist)):
  print(thislist[i]) 
~~~

- using a while loop to go through all the index numbers
~~~
thislist = ["apple", "banana", "cherry"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1
~~~

- List Comprehension offers the shortest syntax for looping through lists:
~~~
thislist = ["apple", "banana", "cherry"]
[print(x) for x in thislist] 
~~~

## List Comprehension
List comprehension offers a shorter syntax when you want to create a new list 
based on the values of an existing list.<br>
Based on a list of fruits, you want a new list, containing only the fruits 
with the letter "a" in the name.Without list comprehension you will have 
to write a for statement with a conditional test inside:
~~~
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []
for x in fruits:
  if "a" in x:
    newlist.append(x)
print(newlist) 
~~~

With list comprehension you can do all that with only one line of code:
~~~
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits if "a" in x]
print(newlist) 
~~~

###  Syntax

newlist = [expression for item in iterable if condition == True]<br>
**Condition** => The condition is like a filter that only accepts the items that valuate to True.<br>
**Iterable**  => The iterable can be any iterable object, like a list, tuple, set etc.<br>
**Expression** => The expression is the current item in the iteration, but it is also the outcome, 
 which you can manipulate before it ends up like a list item in the new list<br>
 
 
 ## Sort Lists
 
List objects have a sort() method that will sort the list alphanumerically, ascending, by default:
~~~
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort()
print(thislist)

thislist1 = [100, 50, 65, 82, 23]
thislist1.sort()
print(thislist1)
~~~

### Sort Descending
~~~
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort(reverse = True)
print(thislist)
~~~

### Customize Sort Function
You can also customize your own function by using the keyword argument key = function.
~~~
def myfunc(n):
  return abs(n - 50)
thislist = [100, 50, 65, 82, 23]
thislist.sort(key = myfunc)
print(thislist)
~~~

### Case Insensitive Sort
~~~
thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.sort(key = str.lower)
print(thislist)
~~~

### Reverse Order
~~~
thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.reverse()
print(thislist)
~~~

## Copy a List
You cannot copy a list simply by typing list2 = list1, 
because: list2 will only be a reference to list1, 
and changes made in list1 will automatically also be made in list2.
There are ways to make a copy, one way is to use the built-in List method copy().
~~~
thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)
~~~

Another way to make a copy is to use the built-in method list().
~~~
thislist = ["apple", "banana", "cherry"]
mylist = list(thislist)
print(mylist)
~~~

## Join Lists
There are several ways to join, or concatenate, two or more lists in Python.
One of the easiest ways are by using the + operator.
~~~
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]
list3 = list1 + list2
print(list3)
~~~

Another way to join two lists are by appending all the items from list2 into list1, one by one:
~~~
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]
for x in list2:
  list1.append(x)
print(list1)
~~~

you can use the extend() method, which purpose is to add elements from one list to another list:
~~~
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]
list1.extend(list2)
print(list1) 
~~~

## List Methods

### count()
Return the number of times the value "cherry" appears in the fruits list:
~~~
fruits = ['apple', 'banana', 'cherry']
x = fruits.count("cherry") => 1
~~~

### index()
What is the position of the value "cherry":
~~~
fruits = ['apple', 'banana', 'cherry']
x = fruits.index("cherry")  => 2 
~~~





