# Python-Tutorial
This repository contains coding syntax for Python language.

- Python is a popular programming langauge.

- Python can be used on a server to create web applications.

# Python Syntax

**Syntax - A set of rules for grammar and spelling :**

***Example :***

_print("Hello World")_

_Output: Hello World_

# Python Indentation

**Indentation refers to the spaces at the beginning of a code line.**

- **Python uses indentation to indicate a block of code :**

***Example :*** ___ = _tab_

_if 5 > 2:_
  
___ _print("Five is greater than two!")_
  
- **Python will give you an error if you skip the indentation :**

***Example (Syntax Error) :***

_if 5 > 2:_

_print("Five is greater than two!")_

- **The number of spaces is up to you as a programmer, but it has to be at least one :**

***Example***

_if 5 > 2:_
   
___ _print("Five is greater than two!")_

_if 5 > 2:_
      
___ ___ _print("Five is greater than two!")_
      
- **You have to use the same number of spaces in the same block of code, otherwise Python will give you an error :**

***Example (Syntax Error) :***

_if 5 > 2:_
 
___ _print("Five is greater than two!")_
        
___ ___ _print("Five is greater than two!")_
          
# Python Variables

**In Python, variables are created when you assign a value to it :**

***Example***

_x = 5_

_y = "Hello, World!"_

**Python has no command for declaring a variable**

# Comments

- Comments can be used to explain Python code.

- Comments can be used to make the code more readable.

- Comments can be used to prevent execution when testing code.

**Python has commenting capability for the purpose of in-code documentation.**

**Comments start with a #, and Python will render the rest of the line as a comment (it will basically ignore them) :**

***Example #1***

_#This is a comment._

_print("Hello, World!")_

***Example #2***

_print("Hello, World!") #This is a comment_

**A comment does not have to be text that explains the code, it can also be used to prevent Python from executing code :**

***Example***

_#print("Hello, World!")_

_print("Cheers, Mate!")_

**Multi Line Comments**

- Python does not really have a syntax for multi line comments.

**To add a multiline comment you could insert a # for each line :**

***Example***

_#This is a comment_

_#written in_

_#more than just one line_

_print("Hello, World!")_

**Or, not quite as intended, you can use a multiline string.**

**Since Python will ignore string literals that are not assigned to a variable, you can add a multiline string (triple quotes) in your code, and place your comment inside it :**

***Example***

_"""_

_This is a comment_

_written in_

_more than just one line_

_"""_

_print("Hello, World!")_

**As long as the string is not assigned to a variable, Python will read the code, but then ignore it, and you have made a multiline comment.**

# Python Variables

