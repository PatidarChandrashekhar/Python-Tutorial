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

**BUILT-IN DATA TYPES**

- Data type is a crucial concept in programming.

- Variables can store a variety of data, and different types can perform different tasks.

- **Python comes with the following data types pre-installed in these categories :**

***Text Type*** :	_str_

***Numeric Types*** : _int, float, complex_

***Sequence Types*** :	_list, tuple, range_

***Mapping Type*** :	_dict_

***Set Types*** : _set, frozenset_

***Boolean Type*** :	_bool_

***Binary Types*** : _bytes, bytearray, memoryview_

**GETTING THE DATA TYPE**

- **The type() function can be used to determine the data type of any object :**

***Example*** _(Print the variable a's data type)_

_a = 5_

_print(type(a))_

**SETTING THE DATA TYPE**

**When you assign a value to a variable in Python, the data type is set :**

_a = "Hello World"_	***string (str)***

_a = 20_	***integer (int)***	

_a = 20.5_	***float***

_a = 1j_	***complex***

_a = ["apple", "banana", "cherry"]_	***list***	

_a = ("apple", "banana", "cherry")_	***tuple***	

_a = range(6)_	***range***	

_a = {"name" : "John", "age" : 36}_	***dict***

_a = {"apple", "banana", "cherry"}_	***set***	

_a = frozenset({"apple", "banana", "cherry"})_	***frozenset***	

_a = True_	***boolean (bool)***

_a = b"Hello"_	***bytes***	

_a = bytearray(5)_	***bytearray***	

_a = memoryview(bytes(5))	memoryview

**SETTING THE SPECIFIC DATA TYPE**

- **The constructor functions listed below can be used to specify the data type :**

_a = str("Hello World")_	***string (str)***

_a = int(20)_	***integer (int)***

_a = float(20.5)_	***float***	

_a = complex(1j)_	***complex***	

_a = list(("apple", "banana", "cherry"))_	***list***	

_a = tuple(("apple", "banana", "cherry"))_	***tuple***	

_a = range(6)_	***range***	

_a = dict(name="John", age=36)_	***dict***	

_a = set(("apple", "banana", "cherry"))_	***set***	

_a = frozenset(("apple", "banana", "cherry"))_	***frozenset***	

_a = bool(5)_	***boolean (bool)***	

_a = bytes(5)_	***bytes***	

_a = bytearray(5)_	***bytearray***	

_a = memoryview(bytes(5))_	***memoryview***

# Numbers

**Python has three different numeric types :**

- int

- float 

- complex

**When you add a value to a numeric type variable, it is created :**

***Example***

_a = 3    # int_

_b = 8.5  # float_

_c = 4x   # complex_

**You can use the type() function in Python to determine the type of any object :**

***Example***

_print(type(a))_

_print(type(b))_

_print(type(c))_

**INT**

- **An int, or integer is a whole number that can be positive or negative, has no digits, and can be any length :**

***Example***

_a = 4_

_b = 134912741298298_

_c = -2419342_

_print(type(a))_

_print(type(b))_

_print(type(c))_

**FLOAT**

- **A float, also known as a "floating point number," is a positive or negative number with one or more decimals :**

***Example***

_a = 2.25_

_b = 4.0_

_c = -72.56_

_print(type(a))_

_print(type(b))_

_print(type(c))_

- **Scientific numbers with a "e", to signify the power of ten, can also be used as floats :**

***Example***

_a = 45e2_

_b = 18E7_

_c = -90.2e505_

_print(type(a))_

_print(type(b))_

_print(type(c))_

**COMPLEX**

- **The imaginary portion of complex numbers is written with a "j" :**

***Example***

_a = 2+4j_

_b = 4j_

_c = -4j_

_print(type(a))_

_print(type(b))_

_print(type(c))_

**TYPE CONVERSION**

- **The int(), float(), and complex() functions can be used to convert between types :**

***Example***

_a = 4    # int_

_b = 4.5  # float_

_c = 2j   # complex_

_#convert from int to float :_

_x = float(a)_

_#convert from float to int :_

_y = int(b)_

_#convert from int to complex :_

_z = complex(a)_

_print(x)_

_print(y)_

_print(z)_

_print(type(x))_

_print(type(y))_

_print(type(z))_

**NOTE : Complex numbers cannot be converted to another number type**

**RANDOM NUMBER**

- **Although Python does not have a random() function, it does have a built-in module named random that can be used to generate random numbers :**

***Example** _(Import the random module and display a number between 1 and 9 as follows :)_

_import random_

_print(random.randrange(1, 10))_

# Casting

**SPECIFY A VARIABLE TYPE**

- It's possible that you'll wish to assign a type to a variable at some point. This can be accomplished through casting. Python is an object-oriented language, therefore data types, including primitive kinds, are defined using classes.

- **Constructor functions are used to cast objects in Python :**

- _int() creates an integer number from an integer, a float (by deleting all decimals), or a text literal (providing the string represents a whole number)_

- _float() is a function that creates a float number from an integer, a float, or a string literal (providing the string represents a float or an integer)_

- _str() - creates a string from a number of different data types, including strings, integer literals, and float literals_

***Example*** _(int)_

_a = int(4)   # a will be 4_

_b = int(3.6) # b will be 3_

_c = int("7") # c will be 7_

***Example*** _(float)_

_a = float(4)     # a will be 4.0_

_b = float(3.9)   # b will be 3.9_

_c = float("2")   # c will be 2.0_

_d = float("1.7") # d will be 1.7_

***Example*** _(str)_

_x = str("s3") # x will be 's3'_

_y = str(4)    # y will be '4'_

_z = str(1.0)  # z will be '1.0'_

# Strings

- Single quotation marks or double quotation marks are used to surround strings in Python.

- 'world' and "world" are the same.

- **The print() function can be used to display a string literal :**

***Example***

_print("World")_

_print('World')_

**ASSIGN STRING TO A VARIABLE**

- **When you assign a string to a variable, you use the variable name, an equal sign, and the string :**

***Example***

_x = "World"_

_print(x)_

**MULTILINE STRINGS**

- **Using three quotation marks, you can assign a multiline string to a variable :**

***Example***

_x = """Life is like riding a bicycle. 

To keep your balance, 

you must keep moving."""_

_print(x)_

***Example*** _OR 3 SINGLE QUOTES_

_x = '''Life is like riding a bicycle. 

To keep your balance, 

you must keep moving.'''_

_print(x)_

**NOTE : As a result, line breaks are added in the same place as they were in the code**

**STRINGS ARE ARRAYS**

- Strings in Python, like many other popular programming languages, are arrays of bytes that represent unicode characters.

- However, because Python lacks a character data type, a single character is merely a one-length string.

- **Square brackets can be used to access the string's elements :**

***Example*** _(Get the character to position 1 (remember, the first character has the position 0))_

_x = "Hello, World!"_

_print(x[1])_

**LOOPING THROUGH A STRING**

- **We can use a for loop to loop through the characters in a string since strings are arrays :**

***Example***

_for x in "apple":_
  
___ _print(x)_

**STRING LENGTH**

- **Use the len() function to find out how long a string is :**

***Example***

_x = "Hello, World!"_

_print(len(x))_

**CHECK STRING**

- **The keyword : in, can be used to see if a phrase or character is contained in a string :**

***Example***

_txt = "May the Force be with you."_

_print("you" in txt)_

***Example*** _(Use it in an if statement)_

_txt = "May the Force be with you."_

_if "you" in txt:_
  
___ _print("Yes, 'you' is present.")_

**CHECK IF NOT**

- **The keyword : not in, can be used to see if a phrase or character is not contained in a string :**

***Example***

_txt = "May the Force be with you."_

_print("me" not in txt)_

***Example*** _(Use it in an if statement)_

_txt = "May the Force be with you."_

_if "me" not in txt:_
  
___ _print("No, 'me' is NOT present.")_
