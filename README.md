# Complete-Python-Bootcamp-From-Zero-to-Hero-in-Python

to open a jupter notebook inside a folder 
> open cmd on folder
> jupyter notebook

python official documentation ---> https://docs.python.org/3/ <br>

### command line basics

to list contents of current directory
> dir

to go inside a subfolder
> cd directoryName

to move back up a directory 
> cd ..

to get options
> cd D{TAB}  

to clear screen
> cls

### jupyter notebook

to run a cell
> shift + enter

to see all the keyboard shortcuts
> help > keyboard shortcuts

to write notes instead of code
we can change in jupyer notebook  code to markdown


FAQ
1. What's the difference between floating point and an integer?

An integer has no decimals in it, a floating point number can display digits past the decimal point.

2. Why doesn't 0.1+0.2-0.3 equal 0.0 ?

This has to do with floating point accuracy and computer's abilities to represent numbers in memory. For a full breakdown, check out: https://docs.python.org/2/tutorial/floatingpoint.html

---

python uses dynamic typing , this means we can reassign a variable to different data types

to know the type of data type a
> type(a)

string slicing
[start:stop:step]   ---> s[start,stop)  with step

---
print fromatting with strings

.format() method

example 1
> print('This is a string {}'.format('Inserted'))

output

> This is a string Inserted

<br>

example 2
> print('The {} {} {}'.format('fox','brown','quick'))

output

> The fox brown quick

<br>

example 3
> print('The {2} {1} {0}'.format('fox','brown','quick'))

output

> The quick brown fox

<br>


example 4
> print('The {q} {b} {f}'.format(f='fox',b='brown',q='quick'))

output

> The quick brown fox

<br>

---
float formatting follows "{value:width:precision f}"

> result = 100/777
> result
```
0.1287001287001287
```
> print("The result was {r}".format(r=result))

```
The result was 0.1287001287001287
```

> print("The result was {r:10.3f}".format(r=result))
```
The result was      0.129
```
> print("The result was {r:1.5f}".format(r=result))

```
The result was 0.12870
```

---
f strings
example 1
> name = 'Aditya'
> print(f'Hello, his name is {name}')
```
Hello, his name is Aditya
```
<br>

example 2
> name = 'Aditya'
> age = 22
> print(f'{name} is {age} years old.')
```
Aditya is 22 years old.
```

---
HERE IS AN AWESOME SOURCE FOR PRINT FORMATTING:

https://pyformat.info/

---
List

to append a element
```py
l.append(x)
````

to pop an element from last
```py
l.pop()
```

to pop an element at a given index
```py
l.pop(2)
# here popping element at index 2
```

to sort a list inplace
```py
l.sort()
```

to reverse a list
```py
l.reverse()
```

---

1. Do dictionaries keep an order? How do I print the values of the dictionary in order?

Dictionaries are mappings and do not retain order! If you do want the capabilities of a dictionary but you would like ordering as well, check out the ordereddict object 

---
tuple

to count a element in tuple
```py
t.count(x)
```

to finde index of
```py
t.index(x)
```

---
Writing and reading from a file in jupyter notebook

```py
%%writefile myfile.txt
Hello this is a text file
this is the second line
this is the third line
```

opening a file
```py
myfile = open('myfile.txt')
```

to know the working directory in jupyter notebook
```py
 pwd
```


reading a file
```py
myfile.read()
```

to move cursor back to start
```py
myfile.seek(0)
```

to close a file
```py
myfile.close()
```

---
opening  file new way

```py
with open('myfile.txt') as my_new_file:
    contents = my_new_file.read()  
```

on jupyter notebook on typing 'shift+tab' just near a function it will provide 
documentation


---
Resources for More Basic Practice

http://codingbat.com/python<br>
https://projecteuler.net/archives<br>
http://www.codeabbey.com/index/task_list<br>
https://www.reddit.com/r/dailyprogrammer<br>
http://www.pythonchallenge.com/<br>

---


tuple unpacking

```py
mylist = [(1,2),(3,4),(5,6),(7,8)]
for a,b in mylist:
    print(a)
    print(b)
```

iterating dictionary

will print only key
```py
d = {'k1':1,'k2':2,'k3':3}
for item in d:
    print(item)
```

to only print values
```py
d = {'k1':1,'k2':2,'k3':3}
for item in d.values():
    print(item)
```

will print (key,values)
```py
d = {'k1':1,'k2':2,'k3':3}
for item in d.items():
    print(item)
```

```py
d = {'k1':1,'k2':2,'k3':3}
for key,value in d.items():
    print(f'{key} contains value {value}')
```

---

we can use pass keyword to put something into indentation

```py

x = [1,2,3]
for item in x:
    pass

```

---
range()

```py
for num in range(0,11,2):
    print(num)
```

output
```
0
2
4
6
8
10
```

---
enumerate

normal method
```py
index_count = 0

for letter in 'abcde':
    print('At index {} the letter is {}'.format(index_count,letter))
    index_count += 1
```

using enumerate
```py
word = 'abcde'
for item in enumerate(word):
    print(item)
```

```py
word = 'abcde'
for index,letter in enumerate(word):
     print('At index {} the letter is {}'.format(index,letter))
```

---
zip function

```py
mylist1 = [1,2,3]
mylist2 = ['a','b','c']

for item in zip(mylist1,mylist2):
    print(item)

```

```py
mylist1 = [1,2,3,4,5,6,7,8]
mylist2 = ['a','b','c']
mylist3 = [100,200,300]

for item in zip(mylist1,mylist2,mylist3):
    print(item)

```

casting it to a list
```py
list(zip(mylist1,mylist2))
```

tuple unpacking
```py
for a,b,c in zip(mylist1,mylist2,mylist3):
    print(b)
```

in operator
```py
x in ['x','y','z']  #true
'mykey' in {'mykey':345}  #true
d = {'mykey':345}
345 in d.values() #true
345 in d.keys() #false
```

---
min max

```py
mylist = [10,20,30,40,100]
min(mylist)
# 10

max(mylist)
# 100
```

---
random library

shuffle
```py
from random import random shuffle
mylist = [1,2,3,4,5,6,7,8,9,10]
shuffle(mylist)
```

random integer
```py
from random import randint
mynum = randint(0,100)
```

---

input in python

```py
result = input('Enter a number here: ')
```

casting into float or int
```py
float(result)
int(result)
```

---

list comprehensions

normal way
```py
mystring = 'hello'
mylist = []
for letter in mystring:
    mylist.append(letter)
```

using list comprehensions
```py
mylist = [letter for letter in mystring]
```

we can also perform operations on first variable name
```py
mylist = [num**2 for num in range(0,11)]
```

we can also add if statements to it
```py
mylist = [x**2 for x in range(0,11) if x%2==0]
```

another example
```py
celcius = [0,10,20,34.5]
fahrenheit = [( (9/5)*temp + 32 ) for temp in celcius]
```

if else statement in one line not recommended for redability
```py
results = [x if x%2==0 else 'ODD' for x in range(0,11)]
```

nested loops in list comprehensions


normal way
```py
mylist = []

for x in [2,4,6]:
    for y in [100,200,300]:
        mylist.append(x*y)

```

using list comprehensions
```py
mylist = [x*y for x in [2,4,6] for y in [100,200,300]]
```

---

to convert to lowercase
```py
word = 'Sam'
print(word[0].lower())
```
> s

---

in fizzbuzz problem be careful to check first multiple of both 3 and 5 , then 3 ,then 5

---

methods

```py
list.append(x)
list.pop()

```

to know about a method or a function
```py
help(mylist.insert)
```

---
 functions

providing default values to functions parameter
 ```py
def say_hello(name='Default'):
    print(f'Hello {name}')

say_hello('Aditya')

 ```

 ---

 functions and tuple unpacking
 ```py
stock_prices = [('Apple',200),('Google',400),('Microsoft',100)]
for item in stock_prices:
    print(item)

for ticker,price in stock_prices:
    print(ticker)
 ```

with functions and tuple unpacking
```py
work_hours = [('Abby',200),('Babby',400),('Cabby',100)]

def employee_check(work_hours):
    current_max = 0
    employee_of_the_month = ''

    for employee,hours in work_hours:
        if hours > current_max:
            current_max = hours
            employee_of_the_month = employee

    return (employee_of_the_month,current_max)

name,hours = employee_check(work_hours) 
```

---

interaction between python functions

```py
example = [1,2,3,4,5,6,7]
from random import shuffle
shuffle(example)

```

guessing game
```py
from random import shuffle

def shuffle_list(mylist):
    shuffle(mylist)
    return mylist

def player_guess():
    guess = ''

    while guess not in ['0','1','2']:
        guess = input("Pick a number : 0,1 or 2 : ")
    
    return int(guess)

def check_guess(mylist,guess):
    if mylist[guess] == 'O':
        print('Correct!')
    else:
        print('Wrong guess !')
        print(mylist)


# Initial_list
mylist = [' ','O',' ']

# shuffled list
mixedUp_list = shuffle_list(mylist)

# user guess
guess = player_guess()

#check guess
check_guess(mixedUp_list,guess)

```

---

*args and **kwargs

for two parameters
```py
def myfunc(a,b):
    return sum((a,b)) * 0.05

myfunc(40,60)
```

```py
def myfunc(*args):
    return sum(args) * 0.05

# now we can give any number of parameters we want
myfunc(40,50,67,89)
```

args is just a name we can name it different

<br>

using **kwargs
```py
def myfunc(**kwargs):
    print(kwargs)
    if 'fruit' in kwargs:
        print('My fruit of choice is {}'.format(kwargs['fruit']))
    else:
        print('I did not find any fruit here')

myfunc(fruit='apple',veggie='lettuce')
```

using both *args and **kwargs together
```py
def myfunc(*args,**kwargs):
    print(args)
    print(kwargs)
    print('I would like {} {}'.format(args[0],kwargs['food']))

myfunc(10,20,30,fruit='orange',food='eggs',animal='dog')
```


---

capitalize()  capitalizes the first letter of string 

creating a string from list

```py
mylist = ['a','b','c']
mystr = ''.join(mylist)
```
> abc

```py
mylist = ['a','b','c']
mystr = '@'.join(mylist)
```
>a@b@c


---

summer_69 problem

dont add values in between 6...9

```py
def summer_69(arr):

    total = 0
    add = True

    for num in arr:
        while add:
            if num!=6:
                total+=num
                break
            else:
                add=false
        while not add:
            if num != 9:
                break
            else:
                add=True
                break
    return total                

```

---

#### lambda expressions map and filter

```py
def square(num):
    return num**2

my_nums = [1,2,3,4,5]

for item in map(square,my_nums):
    print(item)

list(map(square,my_nums))

```

```py 
def splicer(mystring):
    if len(mystring) % 2 == 0:
        return 'Even'
    else:
        return mystring[0]

names = ['Andy','Eve','Sally']

list(map(splicer,names))
```

<br>


filter

```py
def check_even(num):
    return num%2 == 0

mynums = [1,2,3,4,5,6]

list(filter(check_even,mynums))

for n in filter(check_even,mynums):
    print(n)

```

<br>

lambda expression (also known as anonymous function)

normal way
```py
def square(num):
    return num**2
```

```py
sqaure = lambda num: num ** 2
square(5)
```

<br>

using lambda function in conjunction with map
```py
list(map(lambda num: num**2,mynums))
```

using lambda function in conjunction with filter
```py
list(filter(lambda num: num%2 == 0 ,mynums))
```

```py
names = ['Andy','Eve','Sally']
list(map(lambda name: name[0] , names))
```

reversing names
```py
names = ['Andy','Eve','Sally']
list(map(lambda name: name[::-1] , names))
```










