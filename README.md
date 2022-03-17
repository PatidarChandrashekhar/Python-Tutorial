# Python - Tutorial
This repository contains coding syntax for Python language.

- Python is a popular programming langauge.

- Python can be used on a server to create web applications.

# Syntax

**SYNTAX - A set of rules for grammar and spelling :**

***Example :***

_print("I have a car")_

_Output: I have a car_

# Indentation

**Indentation refers to the spaces at the beginning of a code line.**

- **Python uses indentation to indicate a block of code :**

***Example :*** ___ = _indent_

_if 8 > 4:_
  
___ _print("Eight is greater than four")_
  
- **Python will give you an error if you skip the indentation :**

***Example (Syntax Error) :***

_if 8 > 4:_

_print("Eight is greater than four")_

- **The number of spaces is up to you as a programmer, but it has to be at least one :**

***Example***

_if 8 > 4:_
   
___ _print("Eight is greater than four")_

_if 8 > 4:_
      
___ ___ _print("Eight is greater than four")_
      
- **You have to use the same number of spaces in the same block of code, otherwise Python will give you an error :**

***Example (Syntax Error) :***

_if 8 > 4:_
 
___ _print("Eight is greater than four")_
        
___ ___ _print("Eight is greater than four")_

# Comments

- Python code can be explained using comments.

- To make the code more readable, comments are used.

- To prevent execution when testing code, comments are used.

**Python has commenting capability for the purpose of in-code documentation.**

- **Comments start with a #, and Python will render the rest of the line as a comment (it will basically ignore them) :**

***Example #1***

_#This is a comment._

_print("I have a car!")_

***Example #2***

_print("I have a car!") #This is a comment_

- **A comment does not have to be text that explains the code, it can also be used to prevent Python from executing code :**

***Example***

_#print("I have a car!")_

_print("Howdy there!")_

**MULTI LINE COMMENTS**

- Python does not really have a syntax for multi line comments.

- **To add a multiline comment you could insert a # for each line :**

***Example***

_#This is a comment_

_#written in_

_#more than just one line_

_print("Howdy!")_

**Or, not quite as intended, you can use a multiline string.**

- **Since Python will ignore string literals that are not assigned to a variable, you can add a multiline string (triple quotes) in your code, and place your comment inside it :**

***Example***

_"""_

_This is a comment_

_written in_

_more than just one line_

_"""_

_print("Hello, World!")_

**As long as the string is not assigned to a variable, Python will read the code, but then ignore it, and you have made a multiline comment.**

# Variables

- Variables are containers for storing data values.

- **In Python, variables are created when you assign a value to it :**

***Example***

_n = 5_

_m = "Potato"_

**CREATING VARIABLES**

- Python has no command for declaring a variable

- **A variable is created the moment you first assign a value to it :**

***Example***

_n = 5_

_m = "Peppa"_

_print(n)_

_print(m)_

- **Variables do not need to be declared with any particular type, and can even change type after they have been set :**

***Example***

_n = 4       # n is of type int_

_m = "Raju"  # n is now of type str_

_print(n)_

**CASTING**

- **When you wish to specify the data type of a variable, you can use casting :**

***Example***

_m = str(9)    # m will be '9'_

_n = int(9)    # n will be 9_

_o = float(9)  # o will be 9.0_

**GET THE TYPE**

- **You can get the data type of a variable with the type() function :**

***Example***

_n = 4_

_m = "Peppa"_

_print(type(n))_

_print(type(m))_

**SINGLE VS. DOUBLE QUOTES**

- **String variables can be declared either by using single or double quotes :**

***Example***

_n = "Peppa"_

_# is the same as_

_m = 'Peppa'_

**CASE-SENSITIVE**

- **Variable names are case-sensitive :**

***Example***

- This will create two variables:

_n = 2_

_N = "Peppa"_

_#N will not overwrite n_

**VARIABLE NAMES**

***Names of Variables***

A variable can have a short name (such as x and y) or a longer name (such as age, carname, or total volume). 

***Variables in Python have the following rules :***

- _The name of a variable must begin with a letter or the underscore character_

- _A number cannot be the first character in a variable name_

- _In variable names, only alpha-numeric characters and underscores (A-z, 0-9, and_) _are permitted_

- _Case matters when it comes to variable names (age, Age and AGE are three different variables)_

_LEGAL VARIABLE NAMES :_

***Example***

_myvar = "Camille"_

_my_var = "Camille"_

_myVar = "Camille"_

_MYVAR = "Camille"_

_myvar2 = "Camille"_

_ _my_var = "Camille"_

_ILLEGAL VARIABLE NAMES :_

***Example***

_my-var = "Camille"_

_4myvar = "Camille"_

_my var = "Camille"_

**REMEMBER THAT VARIABLES ARE CASE-SENSITIVE**

***Variable Names with Multiple Words***

- _It can be difficult to comprehend variable names that contain more than one word._

- _You can use a variety of approaches to make them more readable :_ 

***CAMEL CASE***

- Except for the first, each word begins with a capital letter :

- _myVariableName = "Camille"_

***PASCAL CASE***

- The first letter of each word is capitalised :

- _MyVariableName = "Camille"_

***SNAKE CASE***

- An underscore character separates each word :

- _my_variable_name = "Camille"_

**ASSIGN VALUES TO MULTIPLE VARIABLES**

- _You can assign values to many variables in a single line in Python :_

***Example***

_r, m, a = "Raspberry", "Mango", "Apple"_

_print(r)_

_print(m)_

_print(a)_

***NOTE: If the number of variables does not match the number of values, an error will occur***

**ASSIGN ONE VALUE TO MULTIPLE VARIABLES**

- **You may also use a single line to assign the same value to many variables :**

***Example***

_r = m = a = "Raspberry"_

_print(r)_

_print(m)_

_print(a)_

**UNPACK A COLLECTION**

- **Python allows you to extract values from a list, tuple, or other collection of data into variables. This is referred to as unpacking :**

***Example***

- _Unpack a list:_

_fruits = ["raspberry", "mango", "apple"]

_r, m, a = fruits_

_print(r)_

_print(m)_

_print(a)_

**OUTPUT VARIABLES**

- **The print() function in Python is frequently used to print variables :**

***Example***

_y = "I am awesome"_

_print(y)_

- **Multiple variables are produced by the print() function, separated by a comma :**

***Example***

_a = "I"_

_b = "am"_

_c = "awesome"_

_print(a, b, c)_

- **You can also output multiple variables by using the + operator :**

***Example***

_a = "I "_

_b = "am "_

_c = "awesome "_

_print(a + b + c)_

**NOTE : The space character between "Python_" and "is_" is important; otherwise, the result would be "Pythonisawesome."

- **The + letter serves as a mathematical operator for numbers :***

***Example***

_a = 15_

_b = 5_

_print(a + b)_

- **When you use the + operator to combine a string and a number in the print() function, Python throws an error:**

***Example***

_a = 4_

_b = "Camille"_

_print(a + b)_

- **When using the print() function, the best way to output many variables is to use commas to separate them, which even supports different data types :**

***Example***

_a = 4_

_b = "Camille"_

_print(a, b)_

**GLOBAL VARIABLES**

- Global variables are variables that are created outside of a function (as in all of the examples above).

- **Everyone can utilise global variables, both inside and outside of functions :**

***Example*** _(Create a variable outside of a function and utilise it within it)_

_a = "awesome"_

_def myfunc():_
  
__ _print("I am " + a)_

_myfunc()_

- If you create a variable with the same name inside a function, it will be local, meaning it can only be used within that function. 

- **The global variable with the same name will stay global and have the same value as before :**

***Example*** _(Create a variable with the same name as the global variable inside a function)_

_a = "awesome"_

_def myfunc():_
  
__ _a = "fantastic"_
  
__ _print("I am " + a)_

_myfunc()_

_print("Python is " + a)_

**THE GLOBAL KEYWORD**

- When you create a variable inside a function, it is usually local, meaning it may only be utilised within that function.

- **The global keyword can be used to define a global variable within a function :**

***Example*** _(The variable belongs to the global scope if you use the global keyword)_

_def myfunc():_
  
__ _global a_

__ _a = "fantastic"_

_myfunc()_

_print("I am " + a)_

- **If you want to alter a global variable within a function, use the global keyword :**

***Example*** _(To update the value of a global variable inside a function, use the global keyword to refer to the variable)_

_a = "awesome"_

_def myfunc():_
  
__ _global a_

__ _a = "fantastic"_

_myfunc()_

_print("I am " + a)_

# Data Types
