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
#None
```python

weapons = None
print(weapons)

```
# Dictionary
#dict is a data type and a data structure. It is an unordered key values 
```python

#example 1
dictionary = {
  'a': 1,
  'b': 2,
  'x': 3
}

print(dictionary)
print(dictionary['x'])

#example 2
dictionary_1 = {
  'a': [1,2,3],
  'b': 'hello',
  'x': True
}

print(dictionary_1)

#example 3
my_list = [{
  'a': [1,2,3],
  'b': 'hello',
  'x': True
},
{
  'a': [4,5,6,],
  'b': 'hello',
  'x': True
},
{
  'a': [7,8,9],
  'b': 'hello',
  'x': True
}]

print(my_list[0]['a'][2])
print(my_list[2]['a'][1])

#example :
  #Dict keys are immutable, therefore, lists can't be used as keys. Keys have to be unique, they can be overwrited.

dictionary = {
  123: [1,2,3],
  'greeting': 'hello',
  'is_Magic': True,
  True: 'yes',
  #[100]: 'wrong' 
    #this would fail
}

print(dictionary)

#Dictionary Methods

user = {
  'basket': [1,2,3],
  'greet': 'hello',
}

#print(user['age']) 
  #this would fail

#.get

user_1 = {
  'basket': [1,2,3],
  'greet': 'hello',
}

print(user_1.get('age', 55))
  #.get assigns the value to the key if it is missing. If the value is there then it would default to that and ignore the value placeholder.  

#example of using dict
user_2 = dict(name = 'John')
print(user_2)

#another example of calling values in dictionaries
print('basket' in user_1)

#example of checking keys, values, clear, and items(list of total). Copy, update, pop and popitem works in the same way and as in lists. 

print('age' in user_1.keys())
print('hello' in user_1.values())
print(user.items())
print(user.clear())

```
# Tuple
They work like a list but are immutable like variables.  
```python 

my_tuple = (1,2,3,4,5)
print(my_tuple[0])
print(5 in my_tuple)

```
Tuples are less flexible. They don't reverse, replace or sort. 
```python

user = {
  (1,2): [1,2,3],
  'greet': 'hello',
  'age': '20'
}
print(user['greet'])

new_tuple = my_tuple[1:2]
print(new_tuple)

x,y,z, *other = (1,2,3,4,5)
print(other)

```
Tuple methods
```python

print(my_tuple.count(5))
print(my_tuple.index(5))
print(len(my_tuple))

```
# Set
Unordered collection of unique objects.  
```python

my_set = {1,2,3,4,5,5}

print(my_set)
  #only returns the 'unique' objects. The extra 5 will be omitted.  

my_set.add(100)
my_set.add(2)
print(my_set)

my_list = [1,2,3,4,5,5]

print(set(my_list))
  #Useful when one needs to omit duplicates such as e-mails or usernames.  

print(1 in my_set)

print(len(my_set))

print(list(my_set))

new_set = my_set.copy()
my_set.clear()

print(new_set)
print(my_set)

```
Set methods - https://www.w3schools.com/python/python_ref_set.asp
```python

my_set_1 = {1,2,3,4,5}
your_set = {4,5,6,7,8,9,10}

print(my_set_1.difference(your_set))

print(my_set_1.discard(5))
print(my_set_1)

print(my_set_1.difference_update(your_set))
print(my_set_1)

print(my_set_1.intersection(your_set))
  #print(my_set_1 & your_set) works same as above

print(my_set_1.isdisjoint(your_set))

print(my_set_1.issubset(your_set))

print(my_set_1.issuperset(your_set))

print(my_set_1.union(your_set))
  #print(my_set_1 | your_set) works same as above. 

```
# Conditional Logic
```python

is_old = False
is_licensed = True

if is_old and is_licensed:
    print('you are old enough to drive and you have a license!')
#elif is_licensed:
    #print('you can drive now!')
else:
    print('you are not old enough to drive.')

print('ook')

```
Indentation creates nested code

Truthy Falsy: https://stackoverflow.com/questions/39983695/what-is-truthy-and-falsy-how-is-it-different-from-true-and-false
```python

print(True == 1) #True
print('1' == 1) #False
print([] == 1) #False
print(10 == 10.0) #True
print([] == []) #True

# == checks for the inherent Value. 
# 'is' checks for what is stored in the memory. 

```
Ternary Operator or Conditional Expressions
These are shortcuts
```python

#condition_if_true if condition else condition_if_false

is_friend = True
can_message = "message allowed" if is_friend else "not allowed to message"

print(can_message)

```
Short Circuiting
```python

is_Friend = True
is_User = True

if is_Friend and is_User:
  print('best friends forever')

```
Logical operator examples
```python

print(4 == 5)
print(4 < 5)
print('a' < 'b')
print('a' < 'A')
print(1 < 2 < 3 < 4)
print(1 >= 0)
print(0 != 0)
  #not equal to  
print(not(True))
print(not(1 == 1))

```
# For Loops
String
```python

for variable in 'Zero to Mastery':
    print(variable)

```
List
```python

for variable_1 in [1, 2, 3, 4, 5]:
    print(variable_1)

```
Set
```python

for variable_2 in {1, 2, 3, 4, 5}:
    print(variable_2)
    
```
Tuple
```python

for variable_3 in (1, 2, 3, 4, 5):
    print(variable_3)

```
Dictionaries
```python

user = {
  'name': 'Golem', 
  'age': 5006, 
  'can_swim': False
  }

for i in user:
    print(i)

for i in user.items():
    print(i)

for i in user.values():
    print(i)

for i in user.keys():
    print(i)

for key, value in user.items():
    print(key, value)

```
Example
```python

for item in ('a', 'c', 'f', 'b'):
    print(item)
    print(item)
    print(item)
    print(item)
    print(item)
print(item)

```
Example of nested loops
```python

for item_1 in (1, 2, 3, 4, 5):
    for x in ['a', 'b', 'c']:
        print(item_1, x)
	
```
Iterable(noun): object or collection that can be iterated over - list, dictionary, tuple, set, string

Iterate(verb): means that we can go one by one check each item in the collection.

# 

Using range with loops

A range is a collection of objects or an iterable in this context

Examples:
```python

for _ in range(2):
  print(_)

for _ in range(1, 11):
  print(_)

for _ in range(1, 11, 2):
  print(_)

for _ in range(11, 0, -1):
  print(_)

for _ in range(11, 0, -2):
  print(_)

for _ in range(2):
  print(list(range(10)))
  #note how this prints out a list ranging from 0 to 9 (index 10) twice as the iterable is a range of 2

```
# Enumerate
Used like range but its not common. It results in an index, value pair which can be sliced and manipulated. 
```python

for i,char in enumerate('Hellooo'):
  print(i, char)
  #note how this spits out the index of the objects. 

```
Example:
```python

user_input = int(input('Which index?\n'))
for i,char in enumerate(list(range(100))):
  if char == user_input:
    print(f'index of {char} is: {i}')

```
# While Loops
Remember to add a break or a condition to break the loop or avoid the infinite loops 
```python

#while condition:
  #do something

# i = 0
# while i < 51:
#   print(i)
#   i += 1
# else:
#   print('done with all the work')

```
For and While loop comparison. Results the same
```python

my_list = [1,2,3]
for item in my_list:
  print(item)

a = 0
while a < len(my_list):
  print(my_list[a])
  a += 1

```
For simple loops - 'for' loops are great. 

If you're not sure how long the loop is going to be, use while. 

Common while loop usage
```python

# while True:
#   input('say something: ')
#   break

while True:
  response = input('say something: ')
  if (response == 'bye') or (response == 'see ya'):
    break

```
Continue and Pass:

Continue: continues the loop until the loop ends and the next in line code never runs. 

Pass: does nothing, just lets the code move ahead. Used as a placeholder during developement but not in production code. Useful in place of comments sometime to allow for the code to run at the current iteration.  


# What is good code?
Clean, readable, predictable and DRY (Don't Repeat Yourself: no repetition, code should be reusable).  

Example of a code:
```python

picture = [
  [0, 0, 0, 1, 0, 0, 0], 
  [0, 0, 1, 1, 1, 0, 0], 
  [0, 1, 1, 1, 1, 1, 0],
  [1, 1, 1, 1, 1, 1, 1], 
  [0, 0, 0, 1, 0, 0, 0], 
  [0, 0, 0, 1, 0, 0, 0]
  ]

for row in picture:
    for pixel in row:
        if (pixel == 1):
            print('*', end='')
        else:
            print(' ', end='')
    print('')

```
Better version of the code above: 
```python

fill = '.'
empty = ' '

for row in picture:
  for pixel in row:
    if(pixel):
      print(fill, end= '')
    else:
      print(empty, end= '')
  print('')

```
Another example:

Original version
```python

def is_even_1(num_1):
  if num_1 % 2 == 0:
    return True
  elif num_1 % 2 != 2:
    return False

```
Cleaner version
```python

def is_even(num):
  return num % 2 == 0

print(is_even(51))

```
# Functions

'def' is used to define your own functions which can be then run later on 

() brackets indicate it to the interpreter that some action will be taken on this function. 

Functions come in handy to keep the code DRY and also for ease of usage of complex loops etc.  

If a function is run above the line where it is declared then it will results in an error.  

Example:
```python

def say_hello():
  print('hello!')

say_hello()

```
Function parameters: creating variables within a function

Function arguments: calling or invoking the function by assigning arguments(value) for the parameters(variables)

Example:
```python

def say_hello_again(name, emoji):
  print(f'hello {name} {emoji} !')

say_hello_again('Poopy', '💩')

```
# 
Positional arguments:

Arguments require to be in the right position. They are locked to the position of the variable and one comes after the first.  

Keyword arguments:

Arguments that are given with the keyword (variable) and don't need to be positioned as per the defined function. However, this is considered as a negative practice because it creates unnecessary confusion for the reader of the code. As much as possible, right order must be followed.
```python

say_hello_again(emoji='😛', name='Tangy')

```
Default parameters:

These are parameters(variables) within a function that work as a default or a placeholder when no argument is given.
```python

def say_hello_now(name='Boring', emoji='😒'):
  print(f'hello {name} {emoji} !')
say_hello_now()

```
# 
Return:

Functions always should return something otherwise once ran they will result in 'None'

Function either modifies something or returns something. 

Function should do one thing really well and usually should return something. 

Return would always exit the function. 

Example of return:
```python

def sum(num1, num2):
  return num1 + num2

total = sum(5, 10)

print(sum(5, total))

```
Complicated example of return:
```python

def sum_1(n_1, n_2):
  def sum_2(s1, s2):
    return s1 + s2
  return sum_2(n_1, n_2)

total_1 = sum_1(10, 10)

print(sum_1(10, total_1))

```
# Methods vs Functions

Both are actions - the difference is how you use them. 

Functions are called by using brackets. They are either pre-defined within Python or can be defined by the coder using 'def'

print()
list()

Methods are used by using a '.' and data types can use certain methods to action 

print('hellooo'.capitalize())

Whatever is to the left to the dot (.) owns the method. They are owned by the object or the data type. 

Methods can be learned about from Python 3 documentation. Googling it would work too. 
# 
Docstrings

It allows us to comment inside of the function (within the IDE or the editor program and not just using #). It helps with code collaboration. 

Example:
```python

def test(a):
  '''
  Info: This function prints the parameter a
  '''
  print(a)

#Calling the info:

help(test)

#or

print(test.__doc__)

```
# *args and **kwargs

These are used to give multiple arguments to a defined function

*args would grab the positional argumetns

**kwargs would grab the keyword arguments (here the position doesn't matter)

kwargs return in to a dictionary with key/value pairs

Example:
```python

def super_func(*args, **kwargs):
  total = 0
  for item in kwargs.values():
    total += item
  return sum(args) + total

print(super_func(1,2,3,4,5, num1=5, num2=10))

```
Ordering rule when writing parameters in a function: params, *args, default parameters, **kwargs

Exercise:
```python

def highest_even(li):
  li_1 = []
  for item in li:
    if item % 2 == 0:
      li_1.append(item)
  return max(li_1)
  
print(highest_even([10,2,3,4,8,11,200]))

```
# Scope in coding

Scope defines: What variables do I have access to?

Scope in python has 'functional scope' or 'global scope'

Function scope refers to the variable that are assigned inside of a defined fuction

Scope rules hierarchy:

#1 - Starts with local scope or functional scope

#2 - Goes to the parent local if there is one

#3 - Goes to global 

#4 - built in python functions. 
# 
Global keyword

Example of how a global variable can be called within a defined function. 
```python

total = 0

def count():
  global total
  total += 1
  return total

print(count())

```
Another way of doing the above:
```python

total_1 = 0

def count_1(total_1):
  total_1 += 1
  return total_1

print(count_1(count_1(count_1(total_1))))

```
Non-local keyword: This is used to refer to the parent variable

Example of non local
```python

def outer():
  x = 'local'
  def inner():
    nonlocal x
    x = 'nonlocal'
    print('inner: ', x)

  inner() 
  print("outer: ", x)

```
Why do we need scope?

Due to the limitations of the machines. When scopes are managed locally, non-locally (parent) and/or globally, memory resources are used efficiently.  

Python empties the memory taken by local and non-local(parent) variables. 

# Object Oriented Programming (OOP)
Examples of built in classes (or data types and structures in Python)
```python

print(type(None))
print(type(True))
print(type(5))
print(type(5.5))
print(type('hi'))
print(type([]))
print(type(()))
print(type({}))

```
Class names are capitalized and camel case is used
```python

class BigObject:
    pass


obj1 = BigObject()  # double-bracket means that you are instantiating the class.
obj2 = BigObject()
obj3 = BigObject()

print(type(obj1))


class PlayerCharacter:
    def __init__(self, name):
        self.name = name

    def run(self):
        print('run')


player1 = PlayerCharacter('Cindy')

print(player1)
print(player1.name)

```
#
OOP Exercise
```python

class Cat:
    species = 'mammal'
    def __init__(self, name, age):
        self.name = name
        self.age = age
  

cat1 = Cat('Minty', 5)
cat2 = Cat('Pinky', 12)
cat3 = Cat('Sally', 15)

def oldest_cat(*args):
    return max(args)

print(f"The oldest cat is {oldest_cat(cat1.age, cat2.age, cat3.age)} years old")

```
Methods within class

❗️🔆 Within classes, you can use certain in built methods by invoking 'self'. However, the more important and powerful ability is to create your own methods by building functions within classes. This is done by using 'def' and whatever done within those functions, can be used as a class attribute. 

Also, one can create a class OBJECT attribute, which applies to all instantiated objects. 
```python

class PlayerCharacter:
    membership = True # This is a class object attribute
    def __init__(self, name, age):
        self.name = name
        self.age = age
        if (int(age) > 18):
            print("You can play this game, what is your name and age?")
        else:
            print("You cannot play this game")
    
    def shout(self):
        print(f'Your name is {self.name} and age is {self.age}')

# Example of class method

    @classmethod
    def adding(cls, num1, num2): #cls stands for class
        return cls('Teddy', num1 + num2)
    
#Example of static method
    
    @staticmethod
    def adding_1(num_1, num_2):
        return num_1 + num_2
    
print(PlayerCharacter.adding(10, 10))

```
# Four pillars of OOP
```python

'''
1. Encapsulation : ability to call actions (functions and methods) from within a code

2. Abstraction: ability to rely more on the utility and application of code rather than nitty-gritty
    a. There isn't any privacy in Python code - a convention is used where underscore (_) denotes private code

4. Inheritance: parent classes can have children classes (see example below)

5. Polymorphism: methods can be bound to objects rather than classes. This means that methods with same name will get 
over-ridden by the method created within the object. However, polymorphism also allows a code to access both the 
parent and child attributes if needed. 

'''


class User():
    def sign_in(self):  # When there is no variable assigned to the class, no need to use __init__
        print('logged in')


class Wizard(User):
    def __init__(self, name, power):
        self.name = name
        self.power = power

    def attack(self):
        print(f'Attacking with power of {self.power}')


class Archer(User):
    def __init__(self, name, num_arrows):
        self.name = name
        self.num_arrows = num_arrows

    def attack(self):
        print(f'Attacking with arrows. Remaining arrows: {self.num_arrows}')


wizard1 = Wizard('Merlin', 50)
archer1 = Archer('Robin', 100)

# Example of polymorphism
wizard1.attack()
archer1.attack()

print(isinstance(wizard1, Wizard))


def player_attack(char):
    char.attack()


player_attack(wizard1)
player_attack(archer1)

# or

for char in [wizard1, archer1]:
    char.attack()

char.attack()

```
Class, objects, and four pillars of OOP - An exercise
```python

class Pets:
    animals = []

    def __init__(self, animals):
        self.animals = animals

    def walk(self):
        for animal in self.animals:
            print(animal.walk())


class Cat:
    is_lazy = True

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def walk(self):
        return f'{self.name} is just walking around'


class Simon(Cat):
    @staticmethod
    def sing(sounds):
        return f'{sounds}'


class Sally(Cat):
    @staticmethod
    def sing(self, sounds):
        return f'{sounds}'


class Mango(Cat):
    @staticmethod
    def sing(self, sounds):
        return f'{sounds}'


simon = Simon('Simon', 6)
sally = Sally('Sally', 10)
mango = Mango('Mango', 14)

my_cats = [simon, sally, mango]

my_pets = Pets(my_cats)

my_pets.walk()

```
Example of how the parent class methods/attributes can be accessed from within the sub-classes by using 'super'
```python

class User:
    def __init__(self, email):
        self.email = email
        
    @staticmethod
    def sign_in(self):
        print('logged in')


class Wizard(User):
    def __init__(self, name, power, email):
        # old method: User.__init__(self, email)
        super().__init__(email)  # New addition of 'super' that eliminates the need of passing 'self'
        self.name = name
        self.power = power

    def attack(self):
        print(f'Attacking with power of {self.power}')


wizard1 = Wizard('Merlin', 50, 'merlin@gmail.com')

print(wizard1.email)

```
Example of how to call a dir of methods/functions available within an object:
```python

print(dir(wizard1))

```
