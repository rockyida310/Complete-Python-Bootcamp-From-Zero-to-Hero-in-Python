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








