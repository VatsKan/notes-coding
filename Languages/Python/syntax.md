# Python Basics

## Other resources

Project Euler (for problems)

## Basic Syntax

```python
# this is a comment
```
```python
helloStr = "hello"  # variable assignment
```
```python
name = input("enter name: ") # add user input
```

* mathematics:
    ```python
    3 // 4  # integer division
    3 ** 4  # exponentiation
    ``` 
    - order of ops standard maths and other math ops are as usual.
    - comparison ops are the usual (e.g. ```==```, ```<=```, etc.), apart from ```!=```
    - assignment shorthand ops ```+= -= *= /=``` are usual.

* string manipulation
  ```python
  print(2 * "hi") # "hihi"
  ```

* type conversion: 
  ```python
  # type_name(expression)
  str(2)    # "2"
  int("3")  # 3
  int(3.7)  # 3 
  float("2.6") # 2.6
  int("hi") # will crash
  ```

* conditionals
  ```python
  if condition_is_true:
    execute_this_code
  elif condition_2:
    execute_this
  else:
    this_code_is_executed_otherwise
  ```


* ```:``` indicates an indented block will follow. Indentation is used for all the statments in a particular block (e.g. if statement above)
(rather than curly braces like in JS)

* logic keywords:
  ```and, or, not```

* loops
    - while loop:
      ```python
      i = 1
      sum = 0
      while i <= 7:
          sum += i
          i += 1 # increment
      print(sum)
      ```

    - for loop:
      ```python 
      # (define integers a and b)
      for i in range(a, b):
        print(i)
        # iterates through a to b-1
      ```
      ```python 
      # (define list called my_list)
      for item in my_list:
        print(item)
        # iterates through list
      ```
      ```python
      # (define a dictionary d={...})
      for key in dictionary:
          print(dictionary[key])
          # iterates through dictionary, printing values of the keys.
      ```

* functions
    - e.g.
      ```python
      def funcName(arg1, arg2):
        return arg1 * arg2
      ```

    -  A function that doesn't end up calling `return` automatically returns `None` which is a special value with type `NoneType`. [LOOK UP WHAT THIS MEANS]

    - LOOK UP RECURSION IN PYTHON

## Basic in-built functions

* ```print("Hello world")```
 
  ```python
  number = 10
  print(number, end=" ") # This will print " " after number. instead of on a new line.
  ```

* LOOK UP ```range(10)``` (does it give an array [1, ..., 10]?) and ```range(1, 5)```

## Data structures

* dictionaries
  - seems equivalent to javascript objects. (same syntax, but using bracket notation to access values of keys)

* lists 
    - (seems equivalent of JS array, in terms of accessing, declaring)
    - can get length of list using 
    ```len(my_list)```, which returns an int. 
    - ```my_list.append("hi")``` adds "hi" to end of list. 
    - ```del my_list[4]``` deletes 4th item from list 
    - ```my_list.remove("mayo")```  searches through list for mayo and deletes it, less efficient than ```del``` if you know where it is as search required.
    - join two lists:
    ```
    my_list1 = ["hi", "hello"]
    my_list2 = ["jim", "jack"]
    my_list = my_list1 + my_list2   # ["hi", "hello", "jim", "jack"]
    ```
    - ```sorted(my_list)``` arranges my_list in alphabetical order, or numerical order.

* strings 
  - concatonation: ```"hi" + "john"```
  - get part of a string
    ```
    str = "hello"
    print(str[0]) # "h"
    ```
  - compare order of characters
    ```
    "a" <= "b" # true
    "a" >= "z" # false
    ```
  - ```str.islower()``` returns true if
  all the letters in the string is lowercase.
  Similar ```str.isupper()```.
  

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


- when getting errors Python gives us a very convenient call stack - basically a list of all the functions that were called but haven't ended when we get the error. This makes tracking down bugs far easier.