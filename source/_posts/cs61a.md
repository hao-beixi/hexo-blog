---
title: cs61a
date: 2021-10-27 15:20:36
tags:
---
# Lectures
## 1 Functions
## 2 Names
- Names
- Assignments
- User-defined functions
### Types of Expressions
**Primitive Expressions**
- Number or Numeral
- Name
- String
**Call Expressions**
- Operator
- Operand
- ### Environment Diagrams
  
## 3 Control
## 4 Higher-Order Functions
## 5 Environments
## 6 Iteration
## 7 Design
## 8 Function Examples
## Midterm
## 9 Recursion
## 10 Tree Recursion
## 11 Containers
## 12 Data Abstraction
## 13 Trees
## 14 Mutable Values
## 15 Mutable Functions
## 16 Iterators
## 17 Objects
## 18 Inheritance
## 19 Representation
## 20 Composition
## 21 Efficiency[]
## 22 Decomposition
## 23 Data Examples
## Midterm 2
## 24 Users
## 25 Scheme
## 26 Exceptions[]
## 27 Calculators
## 28 Intepreters
## 29 Declarative Programming
## 30 Tables
## 31 Aggregation
## 32 Final Examples
## 33 Databases[]
## 34 Distributed Data[]
## 35 Natural Language[]
## Practice Exam
## Exam 1 - L 1-12 & 14 - 15
## Exam 2 - L 1 - 23
## Exam 3 - L 1 - 31
## 36 Tail Calls
## 37 Macros[]
## 38 Streams[]
---
# Lab
## Lab00: Getting Started
## Lab01: Variables & Functions, Control
## Lab02: Higher-Order Functions, Lambda Expressions, Self Reference
## Lab 03: Midterm Review (Optional) 
## Lab 04: Recusion, Tree Recursion
## Lab 05: Python Lists, Data Abstraction, Trees 
## Lab 06: Nonlocal, Iterators & Generators
## Lab 07: Linked Lists, Mutable Trees, Object-Oriented Programming
## Lab 08: Midterm Review
## Lab 09: Scheme, Scheme Lists
## Lab 10: Interpreters
## Lab 11: SQL  
## Lab 12: Final Review 
---
# Discussion
## Disc 00: Getting Started
## Disc 01: Control, Environment Diagrams
## Disc 02: Highrt-Order Functions, Self Reference
## Disc 03: Recursion
## Disc 04: Python lists, Tree Recursion
## Disc 05: Data Abstraction, Trees, Mutability
## Disc 06: Nonlocal, Iterators & Generators
## Disc 07: Object-Oriented Programming, Linked Lists
## 	Supplemental Disc 08: Efficiency
## 	Disc 09: Scheme
## Disc 10: Interpreters
## Disc 11: SQL
## Disc 12: Final Review
---
# HW
## HW 01
## HW 02
## HW 03
## HW 04
## HW 05
## HW 06
## HW 07
## HW 08
## HW 09
## HW 10
---
# Projects
## Hog
## Hog Contest
## Cats
## Ants
## Scheme
## Scheme Contest
---
# Guerrilla
## Guerrilla 00: Higher-Order Functions, Environment Diagrams, Control
## Guerrilla 01: Python Lists, Recursion, Tree Recursion
## Guerrilla 02: Data Abstraction, Trees, Nonlocal, Iterators & Generators 
## Guerrilla 03: Linked Lists, Object-Oriented Programming
## 	Guerrilla 04: Scheme, Interpreters
## Guerrilla 05: SQL
---
# Textbook
## Chapter 1: Building Abstractions with Functions
### 1.1 Getting Started
All computing begins with representing information, specifying logic to process it, and designing abstractions that manage the complexity of that logic. Mastering these fundamentals will require us to understand precisely how computers interpret computer programs and carry out computational processes.

Structure and Interpretation of Computer Programs (SICP) by Harold Abelson and Gerald Jay Sussman with Julie Sussman
#### 1.1.1 Programming in Python
The language was conceived and first implemented by Guido van Rossum in the late 1980's. The first chapter of his Python 3 Tutorial explains why Python is so popular

python3 tutorial
https://docs.python.org/3/tutorial/appetite.html

zen of python
https://www.python.org/dev/peps/pep-0020/

on-going projects
https://pypi.org/
#### 1.1.2 Installing Python 3
#### 1.1.3 Interactive Sessions
Interactive controls. Each session keeps a history of what you have typed. To access that history, press <Control>-P (previous) and <Control>-N (next). <Control>-D exits a session, which discards this history. Up and down arrows also cycle through history on some systems.
#### 1.1.4 First Examples
**Statements & Expressions**. Python code consists of expressions and statements. Broadly, computer programs consist of instructions to either

Compute some value
Carry out some action
Statements typically describe actions. When the Python interpreter executes a statement, it carries out the corresponding action. On the other hand, expressions typically describe computations. When Python evaluates an expression, it computes the value of that expression. This chapter introduces several types of statements and expressions.

**Functions.** Functions encapsulate logic that manipulates data.

**Objects** An object seamlessly bundles together data and the logic that manipulates that data, in a way that manages the complexity of both


**Interpreters.**Evaluating compound expressions requires a precise procedure that interprets code in a predictable way. A program that implements such a procedure, evaluating compound expressions, is called an interpreter. 

 functions are objects, objects are functions, and interpreters are instances of both.
#### 1.1.5 Errors
Learning to interpret errors and diagnose the cause of unexpected errors is called debugging. Some guiding principles of debugging are:

1. Test incrementally: Every well-written program is composed of small, modular components that can be tested individually. Try out everything you write as soon as possible to identify problems early and gain confidence in your components.
2. Isolate errors: An error in the output of a statement can typically be attributed to a particular modular component. When trying to diagnose a problem, trace the error to the smallest fragment of code you can before trying to correct it.
3. Check your assumptions: Interpreters do carry out your instructions to the letter — no more and no less. Their output is unexpected when the behavior of some code does not match what the programmer believes (or assumes) that behavior to be. Know your assumptions, then focus your debugging effort on verifying that your assumptions actually hold.
4. Consult others: You are not alone! If you don't understand an error message, ask a friend, instructor, or search engine. If you have isolated an error, but can't figure out how to correct it, ask someone else to take a look. A lot of valuable programming knowledge is shared in the process of group problem solving.
Incremental testing, modular design, precise assumptions, and teamwork are themes that persist throughout this te  xt. Hopefully, they will also persist throughout your computer science career.

### 1.2 Elements of Programming
The language also serves as a framework within which we organize our ideas about computational processes.

programs must be written for people to read, and only incidentally for machines to execute.

the means that the language provides for combining simple ideas to form more complex ideas. Every powerful language has three such mechanisms:

- **primitive expressions and statements**, which represent the simplest building blocks that the language provides,
- **means of combination**, by which compound elements are built from simpler ones, and
- **means of abstraction**, by which compound elements can be named and manipulated as units.


In programming, we deal with two kinds of elements: functions and data.

Informally, data is stuff that we want to manipulate, and functions describe the rules for manipulating the data. Thus, any powerful programming language should be able to describe primitive data and primitive functions, as well as have some methods for combining and abstracting both functions and data.

#### 1.2.1  Expressions
 *infix notation*, where the operator (e.g., +, -, *, or /) appears in between the operands (numbers)
#### 1.2.2 Call Expressions
*call expression*, which applies a function to some arguments.

This call expression has subexpressions: the operator is an expression that precedes parentheses, which enclose a comma-delimited list of operand expressions.

The operator specifies a function. 

Function notation has three principal advantages over the mathematical convention of infix notation. First, functions may take an arbitrary number of arguments:No ambiguity can arise, because the function name always precedes its arguments.

Second, function notation extends in a straightforward way to *nested expressions*, where the elements are themselves compound expressions. In nested call expressions, unlike compound infix expressions, the structure of the nesting is entirely explicit in the parentheses.

Third, mathematical notation has a great variety of forms: multiplication appears between terms, exponents appear as superscripts, division as a horizontal bar, and a square root as a roof with slanted siding. Some of this notation is very hard to type! However, all of this complexity can be unified via the notation of call expressions. While Python supports common mathematical operators using infix notation (like + and -), any operator can be expressed as a function with a name.

The order of the arguments in a call expression matters.

#### 1.2.3 Importing Library Functions
Python defines a very large number of functions, including the operator functions mentioned in the preceding section, but does not make all of their names available by default. Instead, it organizes the functions and other quantities that it knows about into modules, which together comprise the Python Library. To use these elements, one imports them.

An import statement designates a module name (e.g., operator or math), and then lists the named attributes of that module to import (e.g., sqrt). Once a function is imported, it can be called multiple times.

The Python 3 Library Docs list the functions defined by each module
http://docs.python.org/py3k/library/index.html

#### 1.2.4 Names and the Environment

If a value has been given a name, we say that the name binds to the value.

In Python, we can establish new bindings using the assignment statement, which contains a name to the left of = and a value to the right

Names are also bound via import statements.

The = symbol is called the assignment operator in Python (and many other languages). Assignment is our simplest means of abstraction, for it allows us to use simple names to refer to the results of compound operations

The possibility of binding names to values and later retrieving those values by name means that the interpreter must maintain some sort of memory that keeps track of the names, values, and bindings. This memory is called an environment.

Names can also be bound to functions.

In Python, names are often called variable names or variables because they can be bound to different values in the course of executing a program. When a name is bound to a new value through assignment, it is no longer bound to any previous value. One can even bind built-in names to new values.

#### 1.2.5 Evaluating Nested Expressions
#### 1.2.6 The Non-Pure Print Function
**Pure Function**
**Non-Pure Function**
### 1.3 Defining New Functions
### 1.4 Designing Functions
### 1.5 Control
### 1.6 Higher-Order Functions
### 1.7 Recursive Functions
## Chapter 2: Building Abstractions with Data
### 2.1 Introduction
### 2.2 Data Abstraction
### 2.3 Sequences
### 2.4 Mutable Data
### 2.5 Object-Oriented Programming
### 2.6 Implementing Classes and Objects
### 2.7 Object Abstraction
### 2.8 Efficiency
### 2.9 Recursive Objects
## Chapter 3: Interpreting Computer Programs
### 3.1 Introduction
### 3.2 Functional Programming
### 3.3 Exceptions
### 3.4 Interpreters for Languages with Combination
### 3.5 Interpreters for Languages with Abstraction
## Chapter 4: Data Processing
### 4.1 Introduction
### 4.2 Implicit Sequences
### 4.3 Declarative Programming
### 4.4 Logic Programming
### 4.5 Unification
### 4.6 Distributed Computing
### 4.7 Distributed Data Processing
### 4.8 Parallel Computing