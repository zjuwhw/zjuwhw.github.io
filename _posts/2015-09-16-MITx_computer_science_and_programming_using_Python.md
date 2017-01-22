---
layout: post
title: Edx-Python学习笔记
tags: [cs, mooc]
---

* TOC
{:toc}


## List of Lecture Topics

- Introduction to Python
	- Knowledge（知识）
	- Machines（机器）
	- Languages（语言）
	- Types（类型）
	- Variables（变量）
	- Operators（操作符）and Branching
- Core elements of programs
	- Bindings
	- Strings
	- Input/Output
	- IDEs
	- Control Flow
	- Iteration
	- Guess and Check
- Simple Programs
	- Approximate Soulutions
	- Bisection Search
	- Floats and Fractions
	- Newton-Raphson
- Functions
	- Decomposition and Abstraction
	- Functions and Scope
	- Keyword Arguments
	- Specifications
	- Iteration vs Recursion
	- Inductive Reasoning
	- Towers of Hanoi
	- Fibonacci
	- Reucrsion on non-numerics
	- Files
- Tuples and Lists
	- Tuples
	- Lists
	- List Operations
	- Mutation, Aliasing, Cloning
- Dictionaries
	- Functions as Objects
	- Dictionaries
	- Example with a Dictionary
	- Fibonacci and Dictionaries
	- Global Variables
- Debugging
	- Programming Challenges
	- Classes of Tests
	- Bugs
	- Debugging
	- Debugging Examples
- Assertions and Exceptions
	- Assertions
	- Exceptions
	- Exception Example
- Classes and Inheritance
	- Object Oriented Programming
	- Class Instances
	- Methods
	- Classes Examples
	- Why OOP
	- Hierarchies
	- Your Own Types
- An Extened Example
	- Building a Class
	- Viualizing the Hierarchy
	- Adding another Class
	- Using Inherited Methods
	- Gradebook Example
	- Generators
- Computational Complexity
	- Program Efficiency
	- Big Oh Notation
	- Complexity Classes
	- Analyzing Complexity
- Searching and Sorting Algorithms
	- Indirection
	- Linear Search
	- Bisection Search
	- Bogo and Bubble Sort
	- Selection Sort
	- Merge Sort
- Visualization of Data
	- Visualizing Results
	- Overlapping Displays
	- Adding More Documentation
	- Changing Data Display
	- An Example
- Summary


## 听课笔记

### Lecture 1: Introduction to python

#### Introduction

- topics:
	- represent knowledge with **data structures（数据结构）**
	- **iteration and recursion（迭代和递归）** as computational metaphors
	- **organize and modularize（组织和模块化）** systems using object classes and methods
	- different classes of **algorithms（算法）**, searching and sorting
	- **complexity（复杂性）** of algorithms

#### Basics of Computation

- What does a computer do?
	- Fundamentally a computer: (1) Performs calculations; (2) Remember the results
	- Calculation is: (1) Built-in primitives; (2) Creating our own methods of calculations
- So are ther limits?
	- Some problems still too complex
	- Some problems are fundamentally impossible to compute

#### Knowledge

- Declarative knowledge（叙述性知识）: statments of facts
- Imperative knowledge（过程式知识）: "how to" methods or recipes（菜谱）
	- sequence of simple **steps**
	- **flow of control** process that specifies when each step is executed
	- a means of determining **when to stop**

#### Machine

- Fixed Program Computers（固定程序计算机）: calculator, Alan Turing’s Bombe and etc.
- Stored Program Computers（储存程序计算机）
- What are the basic primitives（基元）?
	- Turning shows that using six primitives, can compute anything. (Truning complete)
	- Fortunately, modern programming languages have a more convenient set of primitives.
	- can **abstract（抽象）** methods to create new "primitives".
	- But anything computable in one language is computable in any other programming language

#### language

- primitive operations（操作）
- expressions（表达式）
- values（值）

##### ASPECTS OF LANGUAGES

- Primitive constructs（基元构建）:numbers, strings, simple operators 
- Syntax（语法）
- Static semantics（静态语义）
- Semantics（语义）：programming languages have only one meaning but may not be what programmer intended

##### ERRORS

- **syntatic errors（语法错误）**
- **static semantic errors（静态语义错误）**
- no semantic errors but **different meaning than what programmer intended**
	- program crashes, stops running
	- program runs forever
	- program gives an answer but different than expected

#### Types

- Options for programming languages:
	- Source code -> checker -> interpreter -> output
	- Source code -> checker -> compiler -> object code -> interpreter -> output
- Low level: Source code (low level) -> checker -> interpreter -> output
- High level (compiled language): Source code (high level) -> checker -> compiler -> object code (low level) -> interpreter -> output
- High level (interpreted language, such as Python): Source code (high level) -> checker -> interpreter -> output

#### Python objects

##### Python programs

- **Program** is a sequence of **definitions** and **commands**
- **Command** (or statement) instructs interpreter（解释器） to do something

##### Objects（对象）
- programs manipulate **data objects**
- objects have a **type** that dfeines the kind of things programs can do to it
- Objecst are: 
	- Scalar: cannot be subdivided
	- Non-scalr: have internal structure that can be accessed)

##### Scalr objects
- int
- float
- bool 
- NoneType

##### Expressions（表达式）
- Expressions: combine objects and operators
- syntax for a simple expression: <object> <operator> <object>
	- Operators on ints and floats: +, -, *, /, %, **
	- Comparison operators on ints and floats: >, >=, <, <=, ==, !=
	- Operators on bools: and, or, not
- operator precedence（优先级） without parentheses（括号）：`**`, `*`, `/`, `+ and -` executed left to right, as appear in expression 

#### 2.4 Variables and Naming

- assignment: binding variables and values

#### 2.5 Strings

- non-scalar objects
- Extracting parts of strings: indexing and slicing

#### 2.6 Simple Scripts

- statements (not expressions): *print()*, *raw_input()*
- Comments appear after #

#### 2.7 Branching Programs

- Branching programs: the simplest one is a **conditional**
- The indentation is important.
- What have we added?
	1. Branching programs allow us to make choices and do different things
	2. But still the case that at most, each statement gets executed once.
	3. So maximum time to run the program depends only on the length of the program.
	4. These programs run in constant time




Notes for the [edx](www.edx.org) course [Introduction to Computer Science and Programming Using Python](https://www.edx.org/course/introduction-computer-science-mitx-6-00-1x-5)
