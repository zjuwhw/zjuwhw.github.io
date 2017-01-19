---
layout: post
title: Edx-Python学习笔记
tags: [cs, mooc]
---

## 听课笔记

### Lecture 1: Introduction to computation

#### 1.1 Introduction

#### 1.2 Basics of Computation

- What does a computer do?
	- Fundamentally a computer: (1) Performs calculations; (2) Remember the results
	- Calculation is: (1) Built in primitives; (2) Creating our own methods of calculations
- So are ther limits?
	- Some problems still too complex
	- Some problems are fundamentally impossible to compute

#### 1.3 Types of Knowledge

- Declarative knowledge: statments of facts
- Imperative knowledge: "how to" methods or recipes

#### 1.4 Basic Machine Architecture

- Fixed Program Computers
- Stored Program Computers
- What are the basic primitives?
	- Turning shows that using six primitives, can compute anything. (Truning complete)
	- Fortunately, modern programming languages have a more convenient set of primitives.
	- Also have ways to abstract methods to create new "primitives".
	- But anything computable in one language is computable in any other programming language

#### 1.5 Programming language characteristics

- Primitive constructs
- Syntax
- Static semantics
- Semantics

### Lecture 2: Core Elements of Programs

#### 2.1 Introduction

#### 2.2 Types of Programming languages

- Options for programming languages:
	- Source code -> checker -> interpreter -> output
	- Source code -> checker -> compiler -> object code -> interpreter -> output
- Low level: Source code (low level) -> checker -> interpreter -> output
- High level (compiled language): Source code (high level) -> checker -> compiler -> object code (low level) -> interpreter -> output
- High level (interpreted language, such as Python): Source code (high level) -> checker -> interpreter -> output

#### 2.3 Python objects

- Python programs
	- Program (or script) is a sequence of definitions and commands
	- Command (or statement) instructs interpreter to do something
- Objects
	- Each object has a **type** that dfeines the kind of things programs can do to it
	- Objecst are: (1) Scalar (*i.e.* cannot be subdivided); (2) Non-scalr (*i.e.* have internal structure that can be accessed)
- Scalr objects
	- int
	- float
	- bool - Boolean values
- Expressions: [object] [operator] [object]
- Operators on ints and floats: +, -, *, /, %, **
- Comparison operators on ints and floats: >, >=, <, <=, ==, !=
- Operators on bools: and, or, not
- Type conversions (type casting): float(3), int(3.9)

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

## List of Lecture Topics

- Introduction to Python
	- Knowledge
	- Machines
	- Languages
	- Types
	- Variables
	- Operators and Branching
- Core elements of programs
	- Bindings
	- Strings
	- Input/Output
	- IDEs
	- Control Flow
	- Iteration
	- Guess and Check
- Simpel Programs
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





Notes for the [edx](www.edx.org) course [Introduction to Computer Science and Programming Using Python](https://www.edx.org/course/introduction-computer-science-mitx-6-00-1x-5)
