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
	- Operators（操作符）and Branching（FLow of Control）
- Core elements of programs
	- Bindings（赋值）
	- Strings（字符串）
	- Input/Output（输入/输出）
	- IDEs（集成开发环境）
	- Control Flow（控制流）
	- Iteration（循环）
	- Guess and Check（猜测和检查）
- Simple Programs
	- Approximate Solutions（近似）
	- Bisection Search（二分查找）
	- Floats and Fractions（浮点型和分数）
	- Newton-Raphson（Newton-Raphson迭代法）
- Functions
	- Decomposition and Abstraction（分解和抽象）
	- Functions and Scope（函数和作用域）
	- Keyword Arguments（关键字参数）
	- Specifications（说明书）
	- Iteration vs Recursion（迭代 vs 递归）
	- Inductive Reasoning
	- Towers of Hanoi
	- Fibonacci
	- Recursion on non-numerics
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
- syntax for a simple expression: `<object> <operator> <object>`
	- Operators on ints and floats: `+`,` -`, `*`, `/`, `%`, `**`
	- Comparison operators on ints and floats: `>`, `>=`, `<`, `<=`, `==`, `!=`
	- Operators on bools: and, or, not
- operator precedence（优先级） without parentheses（括号）：`**`, `*`, `/`, `+ and -` executed left to right, as appear in expression 

#### Variables（变量）

- **assignment**: binding **variables** and **values**
- BINDING VARIABLES AND VALUES
	- **reuse names** instead of values
	- **easier to change** code later
- value on the right and name on the left

#### Operators and Branching

- Branching programs（程序分块）: the simplest one is a **conditional**
	- a test expression
	- true bblock
	- false block (optional)
- NESTED（嵌套） CONDITIONALS
- Indentation（缩进） is important
- `=` vs `==`
- Priority order of Boolean opersations: `parentheses`, `not` statements, `and` statements, `or` statements

### Lecture 2: Core elements of programs

#### Bindings

- right hand side --> value
- left hand side --> variable
- left hand side will be replaced with new value
- `=` is called assignment

#### [Strings](https://docs.python.org/3/tutorial/introduction.html#strings)

- quotation marks or single quotes

##### operations on stings

- concatenation（连接）: ‘ab’ + 'cd'
- successive concatenation: 3* 'eric'
- the length: len('eric')
- indexing（索引）: 'eric'[1]
- slicing（切片）: 'eric'[1:3]
	- extracts sequence starting at first index, and ending before second index
	- if no value before `:`, start at 0
	- if no value after `:`, end at length
	- if just `:`, make a copy of entire sequence

#### Input/Output

- `print`
- `input("")`, return a string

#### IDEs

- IDE: integrated development environment
	- text editor
	- shell
	- integrated debugger

#### Control Flow

- comparison operators on int and float: 
	- `>`
	- `<`
	- `>=`
	- `<=`
	- `==`
	- `!=`
- logic operators on bools: 
	- `not a`
	- `a and b`
	- `a or b`
- `if ... elif ... else ...`

##### Control FLow: `while` loops

```
while <condition>:
	<expression>
	<expression>
```

repeat until <contidtion> is False

##### Control FLow: `for` loops

```
for <variable> in range(<some_num>):
	<expression>
	<expression>
```

##### range function

`range(start, stop, step)`

##### break statement

- immediately exits whatever loop it is in（直接跳出）
- skips remaining expressions in code block（跳过该块其他表达式）
- exits only innermost loop（只跳出最里一层）

##### for vs while loops

|for loops|while loops|
|:--|:--|
|know number of iterations|unbounded number of iterations|
|can end early via break| can end early via break |
|uses a counter|can use a counter but must initialize before loop and increment it inside loop|
|can rewrite a for loop using a while loop|may not be able to rewrite a while loop using a for loop|

#### Iteration

- some properties of iteration loops:
	- need to set an iteration variable outside the loop
	- need to test variable to determine when done
	- need to change variable within the loop, in addition to other work

#### Guess and Check

- loop characterristics
	- need a loop variable
		- initialized outside loop
		- changes within loop
		- test for termination depends on variable
	- a decrementing function
- GUESS-AND-CHECK
	- guess a value
	- check if the solution is correct
- exhaustive enumeration（枚举）
	- guess and check methods can work on problems with a finite number of possibilities
	- exhaustive enumeration is a good way to generate guesses in an organized manner


### Lecture 3: Simple Algorithms

#### So Far...


Notes for the [edx](www.edx.org) course [Introduction to Computer Science and Programming Using Python](https://www.edx.org/course/introduction-computer-science-mitx-6-00-1x-5)
