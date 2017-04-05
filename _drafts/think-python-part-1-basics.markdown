---
layout: post
title:  "Think Python - Part 1 - Basics"
subtitle: "from zero to hero"
date: 2017-03-13 01:00:00
categories: [tech]
---

Problem Solving = Ability  to formulate problem + think creatively about soultions + expess solution clearly and accurately

### They way of the program


> Tip : While writing python code working in interactive mode is convenient for 
> testing small pieces of code because you can type and execute them immediately.
>  But for anything more than a few lines, you should save your code as a script so 
> you can modify and execute it in the future.


### What is a Program 

All programs are built of following building blocks

<div class="mermaid">
  graph TD
    A[input]
    B[output]
    C[math]
    D[contitionals]
    E[repetation]
</div>

Believe it or not, that’s pretty much all there is to it. Every program you’ve ever used, no matter how complicated, is made up of instructions that look pretty much like these. So you can think of programming as the process of breaking a large, complex task into smaller and smaller subtasks until the subtasks are simple enough to be performed with one of these basic instructions

Programming is error-prone. For whimsical reasons, programming errors are called bugs and the process of tracking them down is called debugging.
Three kinds of errors can occur in a program:
  - Syntax errors : These occuer if you do not follow the rules of programming language.
  - Runtime errors : These errors are also called exceptions because they usually indicate that something exceptional (and bad) has happened.
  - Semantic errors : Program will execute withour throwing errors, but the results/output will not be as expected. It can become tricky to find the cause of a semantic error.

You will need to do debugging to get rid of these errors/bugs
> Tip : One of the most important skills you will acquire is 
> debugging. Although it can be frustrating, debugging is one of 
> the most intellectually rich, challenging, and interesting parts of 
> programming. In some ways, debugging is like detective work. 
> You are confronted with clues, and you have to infer the 
> processes and events that led to the results you see.


Programming languages are formal languages that have been designed to express computations.

 - Tokens : Elements that makes a  language e.g words, symbols..
 - Syntax rules : Ways in which tokens are allowed to be arranged

Parsing is the method of bredking down tokens and structures to make sense of it all

### Variables, expressions and statements

**Values and types** : These are basic things that programs work with, eg number, letter. e.g 2 is a number and  "This is a string", anythying inside double qoutes is  treated as string. 1.5 is called a floating-point number.

**Variables** : Variables are like named things, you can give an name to a value, variables can be changed and modified e.g
n = 17
message = "this is a message"
Type of a variable is the type of value it refers to.

Its a good idea to choose a meaningfull name for a variable. We need to keep following in mind while naming variabled
 - They can be arbitrarily long
 - Can contain both lettters and numbers
 - HAVE to begin with a letter
 - Its a GOOD idea to begin a variable name with lowercase letter
 - "_" underscore character can come in name, it is often used in names with multiple words.
 - Key words e.g "class" cannot be used as variable names

**Operators** are special symbols that represent computations like addition and multiplication. The values the operator is applied to are called operands. The operators + , - , * , / and ** perform addition, subtraction, multiplication, division and exponentiation.

 In Python 3, the result of this division is a float . The new operator // performs floor division.

 An **Expression** comprises of values, variables and operators.
 A **statement** is a unit of code that python interpreter can execute. 

 > TIP : Technically an expression is also a statement, but it is probably simpler to 
 > think of them as different things. The important difference is that an 
 > expression has a value; a statement does not.
 
 #### Order of operations

 When more than one operator appears in an expression, the order of evaluation depends on the rules of precedence. For mathematical operators, Python follows mathematical convention. The acronym PEMDAS is a useful way to remember the rules:

  - **P**arentheses
  - **E**xponentiation
  - **M**ultiplication and **D**ivision
  - **A**ddition and **S**ubtraction


Operators with the same precedence are evaluated from left to right (except exponen-tiation).

 #### String Operations

Performing mathematical operations on strings is illegal. "+" and "*" can be performed in strings.
 - operator + means concatenation =>  "a" + "b" = "ab"
 - operator * means repetation =>  "a"*3 = "aaa"


 ### Functions ###

A bunch of statements can be given a name, these named buch are called functions. It is common to say that a function “takes” an argument and “returns” a result. The result is called the return value.

 - Type conversion functions: These functions help in conveting argements to requried type.
   - int('32')  # output: 32
   - int(3.99)  # output: 3
 - Math functions: Python has a math module that provides most of the familiar mathematical functions. A module is a file that contains a collection of related functions. Before we can use the module, we have to import it `import math`
  - math.sqrt(2)
  - math.pi

### functions
##### Funtion and arguments
 Argument is evaluated before function is called
### Flow of execution
What’s the moral of this sordid tale? When you read a program, you don’t always want to read from top to bottom. Sometimes it makes more sense if you follow the flow of execution.

#### Stack diagrams
To keep track of which variables can be used where, it is sometimes useful to draw a stack diagram.
 - Each function is represented by a frame, a frame box with the name of a function beside it
 - 


 Importing with from
Python provides two ways to import modules
 - import math
   - Math module is imported all functions can be called using
   - math.sin()
 - from math import pi
   - pi variable is imported inside program and can be accessed without math. prefix

#### Questions

 - [Arguments are computed before call] Pass espression to function, change variable used in expression inside functions
 - [] Function defination with expression as arguments
 - Flow of executions  defP, defC , call vs defC, defP , call vs defP, call, defC
 - difference between `from math import *` vs `import math`
 - 1 line ->  70 characters padding
 

#### Conditionals and recursion

1. Modulus operator (%)
   - Returns remainder  e.g 7%3 = 1
   - Surprisingly usefull, can be used to get right most digit e.g x%10 will give right most digit

2. Boolean expressions
  - Its an expression that is either True or False
  - type(True) , type(False)  ---> Bool
  - ==, !=, >, <, >=, <=
  - =>,=< Does not exist!

3. Logical operators
  - and, or, not
  - non-zero "numbers" are true

4. Conditional Execution
  - pass is for convinience != break

5. Alternative Execution
  - True, fasle branches based on conditionals

6. Chained conditionals

7. Recursion
  - The function that calls itself is recursive and process is called recursion
  - Many recurstions are easy to write using for loops, but there are many that are easier to write as recursion than for loop.
  -

8. Infinite Recursion
  - 

9. Keyboard Inputs 
  - raw_input vs input

### Fruitful function
1. dead code
  - dead code - Code that cannot be reached
  - try not to have deadcode

2. Incremental development with scaffolding
  - moving from a working version to another
  - Steps
    - Small working program, make small changes
    - Use temp variables 
    - Once program is working, remove scaffolding / consolidate 
       - But do not make program difficult to read

3. Composition
  - function inside functions

4. Boolean function
  - that returns either true or false
  - good idea to name them so that they sound like yes / no function

5. Guardians
  - Code at the beginning of a program to protect from incorrect inputs / preconditions

### Iteration
1. Multiple assignment
2. Updating variables
3. While statement
4. break
- Stop when this happens vs keep going unitil that happens


### Strings
1. Sequest of characters, starts at 0 .. index can be expressions but should return integer
2. len  - returns number of characters in a string

### String slices
1. s[n:m]  string frm nth to mth, including n excluding m

Strings are immutable


#### Questions
  - type(True) vs 
  - type("True")
  - 3 <= 4 vs 3 => 4 output?
  - Logical operators
    -  0.5 and True
    - -0.5 and True
    -     0 and True
    -      not 0
    - False and True
  - Conditional
    if x > 0:
    print("hello")
    pass
    print("hello")
  - Chained conditionals
    - x =100
    - if x > 200
       print(200)
      elif x > 40
        print(40)
      elif x > 20
        print(20)
      elif
        print("all")
    - * execute first matching branch and break
  - Nested conditions
  - print_n stack digram
      - <module>  [  ]
      - print_n  [s --> "hello", n --> 2]
      - print_n  [s --> "hello", n --> 1]
      - print_n  [s --> "hello", n --> 0]
  - Infinite recursion -- finite recurssion with 1000 depth
  - Input
      print("Enter your name")
      name = input()
      vs
      name = input("Enter your name")

  - Multiple assignment, pass by value
    - a =5
    - b = a
    - a = 3
  - Updating same variable
    - x = 0
    - x + 1 = 2
    - x = x + 3
    - print(x)
  - Think of q question using epsilon
  - str = "epsilon"
      - print(str[1])
      - print(str[0])
      - print(str[1.5])
      - print(str[-0])
      - print(str[-1])
  - string range
    - str[1:5],
    - str[5:1]
    - str[-1:-3]
    - str[-3:-1]
    - str[1:100]
    - str[-100:2]
  - 


- Amusing quotes

"Error message tells where the problem was discovered"

"An endless source of amusement for computer scientists is the observation that the directions on shampoo, “Lather, rinse, repeat,” are an infinite loop"

Program testing can be used to show the presence of bugs, but never to show their absence!
— Edsger W. Dijkstra

- Review of bigger things to come
  - State diagrams
  - Hurestic for writing code


  ###Lists

  - Sequece of values of anytype
  - Lists are mutable
  - "in" operrator works
  - +,* concatenates, repeates the lists
  - List methods
    - Append addes a new element to end of list
    - extend appends a list to another
    - sort arranges the list
    - All list methods modify the list and return void
    - sum() sums up the elements in list
    - 
  - Map, filter built in
  - Deleting 
    - pop returns
    - del del doesnt returns
    - remove by value
  - list() can be used to convert string to a list of character
  - delimiter.join()
  - a is b for comparing strings

### Dictionaries
  - dictionaries have methods called get

### Tuples


#### Questions

   - Strings vs lists imutable
   - pop edge case
   - pop vs del vs remove
   - delete with a range
   - search in list vs search in dictonaries
   - global variables vs list / dics


  ### Classes and Objects

This header indicates that the new class is a Point , which is a kind of Object, which is a built-in type. ???

class Point(object):

The class object is like a factory for creating objects. To create a Point, you call Point as if it were a function.

hasattr can be used to check if class has attribute