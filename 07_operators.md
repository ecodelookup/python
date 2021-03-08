# OPERATORS

Python divides the operators in the following groups:

- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Identity operators
- Membership operators
- Bitwise operators

##  Arithmetic Operators

### Addition 
~~~
x = 5
y = 3
print(x + y) => 8
~~~

### Subtraction
~~~
x = 5
y = 3
print(x - y) => 2
~~~

### MULTIPLICATION 
~~~
x=5;
y=3
print(x*y) => 15
~~~

### DIVISION 
~~~
x = 12
y = 3
print(x / y) =>4 
~~~

### MODULUS
~~~
x = 5
y = 2
print(x % y) => 1
~~~

### Exponentiation
~~~
x = 2
y = 5
print(x ** y) #same as 2*2*2*2*2 => 32
~~~

### Floor division
~~~
x = 15
y = 2
print(x // y) =>7
#the floor division // rounds the result down to the nearest whole number
~~~

## Assignment Operators

| Operator | Example | Same As    |
|----------|---------|------------|
|   = 	   | x = 5 	 | x = 5 	  |
|   +=     | x += 3  | x = x + 3  |
|   -=     | x -= 3  | x = x - 3  |
|   *=     | x *= 3  | x = x * 3  |
|   /=     | x /= 3  | x = x / 3  |
|   %=     | x %= 3  | x = x % 3  |
|   //=    | x //= 3 | x = x // 3 |
|   **=    | x **= 3 | x = x ** 3 |
|   &=     | x &= 3  | x = x & 3  |
|   \|=    | x \|= 3 | x = x \| 3 |
|   ^=     | x ^= 3  | x = x ^ 3  |
|   >>=    | x >>= 3 | x = x >> 3 |
|   <<=    | x <<= 3 | x = x << 3 |

## Comparison Operators
Comparison operators are used to compare two values:

### Equal 
~~~
x = 5
y = 3
print(x == y)
# returns False because 5 is not equal to 3
~~~

### Not equal
~~~
x = 5
y = 3
print(x != y)
# returns True because 5 is not equal to 3
~~~

### Greater than
~~~
x = 5
y = 3
print(x > y)
# returns True because 5 is greater than 3
~~~

### Less than
~~~
x = 5
y = 3
print(x < y)
# returns False because 5 is not less than 3
~~~

### Greater than or equal to
~~~
x = 5
y = 3
print(x >= y)
# returns True because five is greater, or equal, to 3
~~~

### Less than or equal to
~~~
x = 5
y = 3
print(x <= y)
# returns False because 5 is neither less than or equal to 3
~~~

## Logical Operators
Logical operators are used to combine conditional statements:

| Operator 	| Description                                            |        Example        |
|-----------|--------------------------------------------------------|-----------------------|
| and  	    |Returns True if both statements are true 	             | x < 5 and  x < 10 	 |
| or 	    |Returns True if one of the statements is true 	         | x < 5 or x < 4 		 |
| not 	    |Reverse the result, returns False if the result is true | not(x < 5 and x < 10) |	


## Identity Operators

Identity operators are used to compare the objects, 
not if they are equal, but if they are actually the same object, 
with the same memory location:

| Operator | Description 	                                       | Example    |
|----------|-------------------------------------------------------|------------|
|is  	   | Returns True if both variables are the same object    |  x is y    |
|is not    | Returns True if both variables are not the same object| x is not y |

## Membership Operators
Membership operators are used to test if a sequence is presented in an object:
| Operator | Description 	                                                                | Example 	|
|----------|--------------------------------------------------------------------------------|-----------|
|in  	   |Returns True if a sequence with the specified value is present in the object 	| x in y 	|
|not in    |Returns True if a sequence with the specified value is not present in the object| x not in y|

## Bitwise Operators

|Operator 	| Name 				| Description                                       |
|-----------|-------------------|---------------------------------------------------|
| &  	    | AND   			| Sets each bit to 1 if both bits are 1             |
| \| 	    | OR    			| Sets each bit to 1 if one of two bits is 1        |
| ^ 	    | XOR   			| Sets each bit to 1 if only one of two bits is 1   |
| ~  	    | NOT   			| Inverts all the bits                              |
| << 	    | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off |
| >> 	    | Signed right shift| Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |
