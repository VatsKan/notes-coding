# Python Basics

## Other resources

Project Euler (for problems)

## Basic Syntax

```
# this is a comment
```
```
helloStr = "hello"  # variable assignment
```
```
name = input("enter name: ") # add user input
```

* mathematics:
    ```
    3 // 4  # integer division
    3 ** 4  # exponentiation
    ``` 
    - order of ops standard maths and other math ops are as usual.
    - comparison ops are the usual (e.g. ==, <=, etc.)
    - assignment shorthand ops ```+= -= *= /=``` are usual.

* string manipulation
print(2 * "hi") # "hihi"

* type conversion: 
```
# type_name(expression)
str(2)    # "2"
int("3")  # 3
int(3.7)  # 3 
float("2.6") # 2.6
int("hi") # will crash
```

* conditionals
```
if condition_is_true:
  execute_this_code
elif condition_2:
  execute_this
else:
  this_code_is_executed_otherwise
```
: stands for "then"

* indentation is used for all the statments in a particular block (e.g. if statement above)
(rather than curly braces like in JS)

* logic keywords:
and, or, not

* loops
    - while loop:
    ```
    i = 1
    sum = 0
    while i <= 7:
        sum += i
        i += 1 # increment
    print(sum)
    ```

## Basic in-built functions

print("Hello world")

```
number = 10
print(number, end=" ") # This will print " " after number. instead of on a new line.
```

string concatonation: "hi" + "john"

## Data structures

* lists 
    - (seems equivalent of JS array, in terms of accessing, declaring)
    - can get length of list using 
    ```len(my_list)```, which returns an int. 
    - ```my_list.append("hi")``` adds "hi" to end of list. 

## Functionality Notes

- variables must be initilised with a value in python
-- variable names can start with underscore or with a-z A-Z, or theoretically any unicode character
-- key words (cannot be used as variable names):
False	await	else	import	pass
None	break	except	in	raise
True	class	finally	is	return
and	continue	for	lambda	try
as	def	from	nonlocal	while
assert	del	global	not	with
async	elif	if	or	yield


- 