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





