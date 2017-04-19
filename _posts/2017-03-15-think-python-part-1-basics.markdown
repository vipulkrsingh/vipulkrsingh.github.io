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

.. To be continued...