# learning-python 👨🏻‍💻🐍</.>

All code learned during Udemy's "Complete Python Developer in 2020 - Zero to Mastery" course.

# Fundamental Data Types
```python

int
float
bool
str
list
tuple
set
dict

```
# Classes -> customer types

# Specialized Data Types
```python

None #used for null values

```
# Fundamental Data Types - Integers = Whole numbers
```python

print(type(2 + 4))
print(type(2 * 4))
print(type(2 - 4))

```
# To the power of
```python

print(2 ** 2)

```
# Rounds it to nearest integer
```python

print(5 // 4)

```
# Prints the remainder of the division
```python

print(6 % 4)

```
# Floating Points = Numbers with Decimal points
```python

print(type(2 / 4)) #0.5
#Integer and Floating points needs to be differentiated so that the interpreter can convert it to the binary correctly. Floating point requires more memory.

```
# Math Functions (Actions)
```python
#rounding up or down

print(round(3.9))

#absolute value of the argument (no negative numbers)

print(abs(-20))

#don't memorize all the actions - google them

```
# Operator precedence
```python

print(20 - (3 * 4))

#Use BODMAS in equations - important for operator precedence

```
# Extra data type

#only used in complex math and is not used generally
```python

complex()

```
#Binary Functions
converts int and floats to their binary values
```python

print(bin(5)) #0b101

```
# Reverse
```python

print(int('0b101', 2))

```

# Variables in Python : way to input information and assign it a name 

Variables are:

1. snake_case
2. start with lowercase or underscore
3. case sentive
4. don't overwrite keywords
```python

iq = 190
user_age = iq/4
a = user_age
print(a)

```
# Constants: best practice and shouldn't be changed
```python

PI = 3.4

```
Shorthand way to assign variables
```python

a,b,c = 1,2,3
print(a)
iq = 100
user_age = iq / 5 #RHS is "expression"
some_value = 5
some_value = 5 + 2
some_value = some_value + 2

```

Augmented assignment operator
```python

some_value += 5

```
Make sure the variable is declared beforehand using the augmented assignment operator
```python

print(some_value)

```
# Fundamental data type - String 
```python

'hi hello there'
"hi hello there"

```
Anything in quotes (single or double) will take the form of string data type
```python

print(type("he hey"))

```
How to write long string 
```python

long_string = '''
W0W
O O
---
'''
print(long_string)
first_name = "Vibhor"
last_name = "Pant"
full_name = first_name + " " + last_name
print(full_name)

```
# String concatenation
```python

print('hello' + 'Vibhor')
#can't concatenate string and int

```
Relation between str, int and type functions + Type conversion
```python

str(100)
print(type(int(str(100))))
#or
a = str(100)
b = int(a)
c = type(b)
print(c)

```
Escape Sequence - using a backslash to add quotes as a string
```python

weather_1 = "It\'s \"kind of\" sunny"
print(weather_1)

#example of adding a backslash in the string and not as an escape sequence 
weather_2 = "It\/s \"kind of\" sunny"
print(weather_2)

#tab example and next line using \t and \n
weather_3 = "\t It\'s \"kind of\" sunny \n hope you have a good day!"
print(weather_3)

```
Formatted strings
```python

#regular example

name = 'Johnny'
age = 55
print('hi ' + name + '. You are ' + str(age) + ' years old.')

#formatted example
	#this is a new feature of Python3 by adding f to the beginning 

print(f'hi {name}. You are {age} years old.')

#this can be done using .format code in Python 2 - not necessary for a new user

```
Strings are stored in a order - repetition doesn't matter, order stays. 
```python

selfish = 'me me me'
          #01234567
print(selfish[0]) #m
print(selfish[7]) #e

#string indexes examples / string slicing

#[start:stop]

selfish_1 = '01234567'
            #01234567
print(selfish_1[0:2]) #01 

#[start:stop:stepover]

print(selfish_1[0:8:2]) #0246
print(selfish_1[1:]) #1234567
print(selfish_1[:5]) #01234
print(selfish_1[::1]) #01234567
print(selfish_1[-1]) #7
print(selfish_1[::-1]) #76543210

```

# Immutability

Once strings are given a value, they cannot be changed through an action (slicing). One needs to go to the source and reassign. That is called immutability through function

# Built in functions. 
```python

print(len('heelllloooo'))

#using string indexes with len
greet = 'yyyaassss'
print(greet[0:len(greet)])

```
Built in methods
```python

#always starts with a . (dot)
#.format()
quote = 'to be or not to be'
print(quote.upper()) #capitalize everything
print(quote.capitalize()) #capitalizes only the first letter
print(quote.find('be')) #searches the index of a part of string
print(quote.replace('be', 'me')) #replaces 1st string with the second
#remember strings are immutable by functions, the above example using .replace is only creating another string without assigning it
print(quote) #this would print the original string values assigned above. 

```
# Booleans - True or False (0 and 1) - logical values. Used in conditions. 
```python 

name = 'Vibhor'
is_cool = False
is_cool = True
print(bool(1))
print(bool(0))
print(bool('True'))

#facebook data example

name = 'Vibhor Pant'
age = '36'
relationship_status = "Married"
relationship_status = 'It\'s complicated'
print(relationship_status)

#input method

birth_year = input('what year were you born?\n')

#inputs are always converted into a str so its important to convert them to int

age = 2020 - int(birth_year)
print(f'Your age is {age}')

#Exercise: Password Checker

username = input('username \n')
password = input('password \n')
passwordlength = len(password)
secret = passwordlength * '*'
print(f'{username}, your password {secret} is {passwordlength} letters long')

```

# Lists
Lists in Python are a form of array
```python

#ordered sequence

#use square brackets to activate a list

li = [1,2,3,4,5]
li2 = ['a', 'b','c']
li3 = [1,2,3, 'a', True]

```
# Data structure
```python

#organize information/data in one place

#a container of data with it pros and cons. 

amazon_cart = ['notebooks', 'sunglasses']
print(amazon_cart[1])

```

# List slicing
```python

#string slicing example
	#string = 'helllooo'
	#string[0:2:1]
amazon_cart = [
'notebooks', #0
'sunglasses', #1
'toys', #2 
'grapes' #3 
]

#example of strings being immutable but lists not

#greet = 'hello'
#greet[0] = 'z' - this won't work

#example of creating a new list out of an existing list as lists are mutable

amazon_cart[0] = 'laptop'
new_cart = amazon_cart[0:3]
new_cart[0] = 'gum'
print(new_cart)
print(amazon_cart)

#example of how this is just reassigning value to an existing list 

amazon_cart[0] = 'laptop'
new_cart = amazon_cart #this is not copying but changing/modifying. For copying, one needs to add[:]
new_cart[0] = 'gum'
print(new_cart)
print(amazon_cart)

```

# Matrix

It is a list/array within a list/array. List and array are also different in Python however, most languages means the same when they use list and/or array.  
```python

matrix = [
  [1,2,3],
  [2,4,6],
  [7,8,9],
]
print(matrix)

#how to access lists

print(matrix[0][1])

```

# List Methods
https://www.w3schools.com/python/python_ref_list.asp
```python

basket = [1,2,3,4,5]
print(len(basket))

```
Using methods
```python

#adding

basket.append(100)
new_list = basket
#print(basket)
print(new_list)

#insert 
#modifies an index within a list. Doesn't copy the list

basket.insert(4, 100)
new_list = basket
#print(basket)
print(new_list)

#extend

new_list = basket.extend([100, 101]) 
#just remember that this is only extending the basket and not really doing anything to new_list. You need to assign basket to new_list for it to read same as basket. 
print(basket)
new_list = basket
print(new_list)

#pop removes the value from the end of the list/array consecutively if no index is specified. It removes the specified index otherwise. Pop returns the value it removes from the list. 

basket.pop()
basket.pop()
basket.pop(0)

#remove would take the 'value' specified. For example, it would take out all the 4s in the list here. Remove returns none.   

basket_1 = [1,2,3,4,5]
new_list_1 = basket_1.remove(4)
print(new_list_1)
new_list_1 = basket_1.pop(3)
print(new_list_1)
print(basket_1)

#clear. This clears the list and doesn't return anything unless printed.  

basket_2 = [1,2,3,4,5]
new_list_2 = basket_2.clear()
print(basket_2)

#index. searches the index of the object specified in the index range

basket = ['a', 'b', 'c', 'd', 'e']
print(basket.index('d'))
print(basket.index('d', 0, 4))

#using 'in' for searching a list. Returns a boolean value

print('d' in basket)

#count. Counts occurrences

print(basket.count('d'))

#sort. Sorts the list as per the underlying order. Example: alphabetical order. 

basket = ['a', 'b', 'c', 'd', 'e', 'd']
basket.sort()
print(basket)

#sorted.
#This creates a new array unlike 'sort' which produces none. Note below how 'basket_1' is not modified but a new array/list was created. 

basket_1 = ['a', 'x', 'b', 'c', 'd', 'e', 'd']
print(sorted(basket_1)) 
  #['a', 'b', 'c', 'd', 'd', 'e', 'x']
print(basket_1)
  #['a', 'x', 'b', 'c', 'd', 'e', 'd']

#reverse. Just reverses the index and no sorting occurs

basket_1.reverse()
print(basket_1)
  #['d', 'e', 'd', 'c', 'b', 'x', 'a']

```
# Common list patterns
These tricks are used along with splicing when dealing with lists
```python

basket_1 = ['a', 'x', 'b', 'c', 'd', 'e', 'd']
basket_1.sort()
basket_1.reverse()
print(basket_1[::-1])
  #this creates a new   list
print(basket_1[:])
  #this creates a copy of the list
print(basket_1)

#range 
  #can be used to create a numbered list

print(list(range(1,101))) 
  #range uses 'index' and not absolute numbers for ranging

#.join

sentence = ' '
new_sentence = sentence.join(['hi', 'my', 'name', 'is', 'Frank'])
print(new_sentence)
  #this creates a new variable and joins the list objects with the variable that is '.join' is applied open

new_sentence_1 = ' '.join(['hi', 'my', 'name', 'is', 'Frank'])
print(new_sentence_1)
  #a shorthand way of doing the same

#this is a way to assign variables to each item in a list
a,b,c = [1,2,3]

print(a)
print(b)
print(c)

#list unpacking
  #more power when assigning variables. Allows for grouping items within a list and assigning it a variable

a,b,c, *other, d = [1,2,3,4,5,6,7,8,9]

print(a)
print(b)
print(c)
print(other)
print(d)

```


