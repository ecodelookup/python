# Strings 

Strings in python are surrounded by either single quotation marks, or double quotation marks.
'hello' is the same as "hello".
You can display a string literal with the print() function:
~~~
print("Hello")
print('Hello')
a = "Hello"
print(a)
~~~

You can assign a multiline string to a variable by using three quotes:
~~~
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a) 
~~~

Python does not have a character data type, 
a single character is simply a string with a length of 1.
Square brackets can be used to access elements of the string.

~~~
a = "Hello, World!"
print(a[1])
~~~

## Looping Through a String

~~~
for x in "banana":
  print(x)
~~~

## String Length

To get the length of a string, use the len() function.
~~~
a = "Hello, World!"
print(len(a))
~~~

## Check String
To check if a certain phrase or character is present in a string, we can use the keyword in.
~~~
txt = "The best things in life are free!"
print("free" in txt)

txt = "The best things in life are free!"
if "free" in txt:
  print("Yes, 'free' is present.")
~~~

To check if a certain phrase or character is NOT present in a string, 
we can use the keyword not in.
~~~
txt = "The best things in life are free!"
print("expensive" not in txt)
txt = "The best things in life are free!"
if "expensive" not in txt:
  print("Yes, 'expensive' is NOT present.")
~~~

## String Slicing

Specify the start index and the end index, separated by a colon, to return a part of the string.
counting starts from 0 to last-1 
~~~
b = "Hello, World!"
print(b[2:5]) => llo  
~~~

y leaving out the start index, the range will start at the first character:
~~~
b = "Hello, World!"
print(b[:5]) => Hello
~~~

By leaving out the end index, the range will go to the end:
~~~
b = "Hello, World!"
print(b[2:]) => llo, World! 
~~~

Use negative indexes to start the slice from the end of the string: 
Get the characters:
From: "o" in "World!" (position -5)
To, but not included: "d" in "World!" (position -2):
~~~
b = "Hello, World!"
print(b[-5:-2])  => orl
~~~

## MODIFY STRING 

### Upper Case
The upper() method returns the string in upper case:
~~~
a = "Hello, World!"
print(a.upper())  => a = "Hello, World!"
print(a.upper()) => HELLO, WORLD!
~~~

### Lower Case
The lower() method returns the string in lower case:
~~~
a = "Hello, World!"
print(a.lower())
~~~

### Remove Whitespace
Whitespace is the space before and/or after the actual text, 
and very often you want to remove this space.
The strip() method removes any whitespace from the beginning or the end:

~~~
a = " Hello, World! "
print(a.strip()) # returns "Hello, World!" 
~~~

### Replace String
The replace() method replaces a string with another string:
~~~
a = "Hello, World!"
print(a.replace("He", "Ji")) => Jillo, World!
~~~

### Split String
The split() method returns a list where the text between 
the specified separator becomes the list items.
~~~
a = "Hello, World!"
print(a.split(",")) # returns ['Hello', ' World!'] 
~~~

## String Concatenation
To concatenate, or combine, two strings you can use the + operator.
~~~
a = "Hello"
b = "World"
c = a + b
print(c)

a = "Hello"
b = "World"
c = a + " " + b
print(c)
~~~

## String Format

we cannot combine strings and numbers like this:<br>
  a ="hello" +5 <br> 
But we can combine strings and numbers by using the format() method!
The format() method takes the passed arguments, formats them, 
and places them in the string where the placeholders {} are:
~~~
age = 36
txt = "My name is John, and I am {}"
print(txt.format(age))
~~~
The format() method takes unlimited number of arguments, 
and are placed into the respective placeholders:
~~~
quantity = 3
itemno = 567
price = 49.95
myorder = "I want {} pieces of item {} for {} dollars."
print(myorder.format(quantity, itemno, price))
~~~
You can use index numbers {0} to be sure the arguments are placed in the correct placeholders:
~~~
quantity = 3
itemno = 567
price = 49.95
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemno, price))
~~~

## Escape Character

To insert characters that are illegal in a string, use an escape character.
An escape character is a backslash \ followed by the character you want to insert.
An example of an illegal character is a double quote inside 
a string that is surrounded by double quotes:<br>

txt = "We are the so-called "Vikings" from the north."<br>

To fix this problem, use the escape character \":
~~~
txt = "We are the so-called \"Vikings\" from the north."
~~~

|Code 	|Result 	
|-------|-----------------|
|\' 	|Single Quote 	  |
|\\ 	|Backslash 	      |
|\n 	|New Line 	      |
|\r 	|Carriage Return  |	
|\t 	|Tab 	          |
|\b 	|Backspace 	      |
|\f 	|Form Feed 	      |
|\ooo 	|Octal value 	  |
|\xhh 	|Hex value        |    