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


