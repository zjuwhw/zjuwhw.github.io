---
layout: post
title: Edx-Python学习笔记
tags: [cs, mooc, python]
---

* TOC
{:toc}


## 听课笔记

### Lecture 1: Introduction to python

#### Introduction（简介）

- topics:
	- represent knowledge with **data structures（数据结构）**
	- **iteration and recursion（迭代和递归）** as computational metaphors
	- **organize and modularize（组织和模块化）** systems using object classes and methods
	- different classes of **algorithms（算法）**, searching and sorting
	- **complexity（复杂性）** of algorithms

#### Basics of Computation（计算的基础）

- What does a computer do?
	- Fundamentally a computer: (1) Performs calculations; (2) Remember the results
	- Calculation is: (1) Built-in primitives; (2) Creating our own methods of calculations
- So are ther limits?
	- Some problems still too complex
	- Some problems are fundamentally impossible to compute

#### Knowledge（知识）

- Declarative knowledge（叙述性知识）: statments of facts
- Imperative knowledge（过程式知识）: "how to" methods or recipes（菜谱）
	- sequence of simple **steps**
	- **flow of control** process that specifies when each step is executed
	- a means of determining **when to stop**

#### Machine（机器）

- Fixed Program Computers（固定程序计算机）: calculator, Alan Turing’s Bombe and etc.
- Stored Program Computers（储存程序计算机）
- What are the basic primitives（基元）?
	- Turning shows that using six primitives, can compute anything. (Truning complete)
	- Fortunately, modern programming languages have a more convenient set of primitives.
	- can **abstract（抽象）** methods to create new "primitives".
	- But anything computable in one language is computable in any other programming language

#### language（语言）

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

#### Types（类型）

- Options for programming languages:
	- Source code -> checker -> interpreter -> output
	- Source code -> checker -> compiler -> object code -> interpreter -> output
- Low level: Source code (low level) -> checker -> interpreter -> output
- High level (compiled language): Source code (high level) -> checker -> compiler -> object code (low level) -> interpreter -> output
- High level (interpreted language, such as Python): Source code (high level) -> checker -> interpreter -> output

#### Python objects（对象）

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

#### Operators（操作符） and Branching（Flow of Control）

- Branching programs（程序分块）: the simplest one is a **conditional**
	- a test expression
	- true bblock
	- false block (optional)
- NESTED（嵌套） CONDITIONALS
- Indentation（缩进） is important
- `=` vs `==`
- Priority order of Boolean opersations: `parentheses`, `not` statements, `and` statements, `or` statements

### Lecture 2: Core elements of programs

#### Bindings（复制）

- right hand side --> value
- left hand side --> variable
- left hand side will be replaced with new value
- `=` is called assignment

#### Strings（字符串）

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

#### Input/Output（输入/输出）

- `print`
- `input("")`, return a string

#### IDEs（集成开发环境）

- IDE: integrated development environment
	- text editor
	- shell
	- integrated debugger

#### Control Flow（控制流）

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

#### Iteration（循环）

- some properties of iteration loops:
	- need to set an iteration variable outside the loop
	- need to test variable to determine when done
	- need to change variable within the loop, in addition to other work

#### Guess and Check（猜测和检查）

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

##### strings

- slice: `[start:stop:step]`
- immutable: cannot be modified

#### Approximate Solutions（近似解）

- start with exhaustive enumeration
	- task small steps to generate guesses in order
	- check to see if close enough
- **good enough** solution
- start with a guess and increment by some **small value**
- `|guess ** 3| - cube <= epsilon` for some **small epsilon**

##### some observations

- Step could be any small number
	- If too small, takes a long time to find square root
	- If too large, might skip over answer without getting close enough
- In general, will task x/step times through code to find solution
- Need a more efficient way do do this

#### Bisection Search（二分查找）

EXAMPLE OF SQUARE ROOT

```python
x = 25
epsilon = 0.01
numGuesses = 0
low = 1.0
high = x
ans = (high + low)/2.0
while abs(ans**2 - x) >= epsilon:
	print('low = ' + str(low) + ' high = ' + str(high) + ' ans = ' + str(ans)) 
	numGuesses += 1
	if ans**2 < x:
		low = ans
	else:
		high = ans
	ans = (high + low)/2.0
print('numGuesses = ' + str(numGuesses))
print(str(ans) + ' is close to square root of ' + str(x))
```

Some obersvation

- Bisection search radically reduces computation time – being smart about generating guesses is important
- Should work well on problems with “ordering” property


#### Floats and Fractions（浮点型和分数）

- Decimal number: `302 = 3*10^2 + 0*10^1 + 2*10^0`
- Binary number: `10011 = 1*2^4 + 0*2^3 + 0*2^2 + 1*2^1 + 1*2^0`

convert decimal number to binary number

```python
if num < 0:
    isNeg = True
    num = abs(num)
else:
	isNeg = False 
result = ‘‘
if num == 0:
    result = ‘0’
while num > 0:
	result = str(num%2) + result
	num = num//2
if isNeg:
	result = ‘-’ + result
```

FRACTIONS

- Decimal number: 0.375 = 3 * 10<sup>-1</sup> + 7 * 10<sup>-2</sup> + 5 * 10<sup>-3</sup>
- Binary number: 0.375 = 0* 2<sup>-1</sup> + 1 * 2<sup>-2</sup> + 1 * 2<sup>-3</sup>

- So if we multiply by a power of 2 big enough to convert into a whole number, can then convert to binary, and then divide by the same power of 2

SOME IMPLICATIONS

- If there is no integer p such that `x*(2**p)` is a whole number, then internal representation is always an approximation
- Use `abs(x-y)` < some small number, rather than `x == y`

#### Newton-Raphson（Newton-Raphson迭代法）

General approximation algorithm to find roots of a polynomial in one variable：
p(x) = a<sub>n</sub>x<sup>n</sup> + a<sub>n-1</sub>x<sup>n-1</sup> + ... + a<sub>1</sub>x + a<sub>0</sub>

Newton showed that if g is an approximation to the root, then `g – p(g)/p’(g)` is a better approximation; where p’ is derivative of p.

```python
epsilon = 0.01
y = 24.0
guess = y/2.0
numGuesses = 0
while abs(guess*guess - y) >= epsilon:
	numGuesses += 1
	guess = guess - (((guess**2) - y)/(2*guess))
	print(‘numGuesses = ‘ + str(numGuesses))
	print('Square root of ' + str(y) + ' is about ' + str(guess))
```

##### Iterative algorithms

- Guess and check methods build on reusing same code 
	- Use a looping construct to generate guesses, then check and continue
- Generating guesses
	- Exhaustive enumeration
	- Bisection search
	- Newton-Raphson (for root finding)

### Lecture 4: Functions

#### Decomposition and Abstraction（分解和抽象）

GOOD PROGRAMMING

- more code not necessarily a good thing
- measure good programmers by the amount of functionality
- introduce **functions**
- mechanism to achieve **decomposition** and **abstraction**

DECOMPOSITION and ABSTRACTION

- Decomposition: Break problem into different, self-contained, pieces
- Abstraction: Suppress details of method to compute something from use of that computation
- Powerful together

DECOMPOSITION

- in programming, divide code into **modules**
	- are *self-contained*
	- used to *break up* code
	- intended to be *reusable*
	- keep code *organized*
	- *keep code coherent*
- achieve decomposition with **functions** and **classes**

ABSTRACTION

- in programming, think of a piece of code as a **block box**
	- cannot see details
	- do not need to see details
	- do not want to see details
	- hide tedious coding details
- achieve abstraction with **function specifications** or **docstrings**

#### Functions and Scope（函数和作用域）

FUNCTIONS

- **functions**: write reusable piece/chunks of code
- "**called**" or "**invoked**": functions are not run in a program until they are "called" or "invoked" in a program
- function characteristics:
	- has a **name**
	- has **parameters** (0 or more)
	- has a **docstring** (optional but recommended)
	- haas a **body**

```python
def is_even(i):             # def是keyword；is_even是函数名，i是参数（parameters or arguments）
	"""                
	Input: i, a positive int
	Returns True if i is even, otherwise False
	"""                 # specification, docstring
	print("hi")         # body
	return i % 2 == 0   # return是keyword

is_even(3)	            # later in the code, you call the function using its name and values for parameters
```

VARIABLE SCOPE

- **formal parameter** gets bound to the value of **actual parameter** when function is called
- new **score/frame/environment** created when enter a funcion
- **scope** is mapping of names to objects
- Python returns the value **None, if no return given**

|return|print|
|:--|:--|
|return only has meaning **inside** a function|print can be used **outside** functions|
|only **one** return executed inside a function|can execute **many** print statements inside a function|
|code inside function but after return statement not executed| code inside function can be executed after a print statement|
|has a value associated with it, **given to function caller**|has a value associated with is, **outputed** to the console|

FUNCTIONS AS ARGUMENTS

- arguments can take on any type, even functions

SCOPE EXAMPLE

- inside a function, **can access** a variable defined outside
- inside a function, **cannot modify** a variable defined outside

#### Keyword Arguments（关键字参数）

Can specify that some arguments have default values, so if no value supplied, just use that value

#### Specifications（说明书）

- a **contract** between the implementer of a function and the clients who will use it
	- **Assumptions**: conditions that must be met by clients of the function; typically constraints on values of parameters
	- **Guarantees**: conditions that must be met by function, providing it has been called in manner consistent with assumptions

#### Iteration vs Recursion（迭代 vs 递归）

WHAT IS RECURSION

- a way to design solutions to problems by **divide-and-conquer or decrease-and-conquer**
- a programming technique where a **function calls itself**
- in programming, goal is to NOT have infinite recursion
	- must have **1 or more base cases** that are easy to solve
	- must solve the same problem on **some other input** with the goal of simplifying the larger problem input

ITERATIVE ALGORITHMS SO FAR

- looping constructs (while and for loops) lead to **iterative** algorithms
- can capture computation in a set of **state variables** that update on each iteration through loop

MULTIPLICATION - ITERATIVE SOLUTION

- "multiply a*b" is equivalent to "add a to itself b times"
- capture **state** by:
	- an **iteration number**
	- a current **value of compustation** (result)

```python
def mult_iter(a, b):
	result = 0
	while b > 0:
		result += a    # value of computation
		b -= 1         # iteration variable
	return result
```

MULTIPLICATION – RECURSIVE SOLUTION

- recursive step
- base case

```python
def mult(a, b):
	if b == 1:                          # base case
		return a
	else:
		return a + mult(a, b-1)         # recursive step
```

SOME OBSERVATIONS

- each recursive call to a function creates its **own scope/environment**
- **bindings of variables** in a scope is not changed by recursive call
- flow of control passes back to **previous scope** once function call returns value

ITERATION vs. RECURSION

```python
def factorial_iter(n):
	prod = 1
	for i in range(1, n+1)
		prod *= i
	return prod
```

```python
def factorial(n):
	if n == 1:
		return 1
	else:
		return n*factorial(n-1)
```

- recursion may be simmpler, more intuitive
- recursion may be efficient from programmer POV (point of view)
- recursion may not be efficient from computer POV

#### Inductive Reasoning（归纳推理）

To prove a statement indexed on integers is true for all values of n:

- Prove it is true when n is smallest value (e.g. n = 0 or n = 1)
- Then prove that if it is true for an arbitrary value of n, one can show that it must be true for n+1

#### Towers of Hanoi（汉诺塔）

```python
def printMove(fr, to):
	print("Move from " + str(fr) + " to " + str(to))
def Towers(n, fr, to, spare):
	if n == 1:
		printMove(fr, to)
	else:
		Towers(n-1, fr, spare, to)
		Towers(1, fr, to, spare)
		Towers(n-1, spare, to, fr)	
```

#### Fibonacci（斐波那契数列）

FIBONACCI

- Base case
	- Females(0) = 1
	- Females(1) = 1
- Recursive case
	- Females(n) = Females(n-1) + Females(n-2)

```python
def fib(x):
	"""
	Input: x, an int >= 0
	Return: Fibonacci of x
	"""
	if x == 0 or x == 1:
		return 1
	else:
		return fib(x-1) + fib(x-2)
```
#### Recursion on non-numerics（非数字递归）

- check if a string of characters is a palindrome(回文)
- Base case
	- a string of length 0 or 1 is a palindrome
- Recursive case
	- If first character matches last character, then is a palindrome if middle section is a palindrome

```python
def isPalindrome(s):
	def toChars(s):
		s = s.lower()
		ans = ''
		for c in s:
			if c in 'abcdefghijklmnopqrstuvwxyz':
				ans = ans + c
		return c
	def isPal(s):
		if len(s) <= 1:
			return True
		else:
			return s[0] == s[-1] and isPal(s[1:-1])
	return isPal(toChars(s))
```

##### Divid and Conquer（分治算法）

- an example of a "divide and conquer" algorithm
- solve a hard problem by breaking it into a set of sub-problems such that:
	- sub-problems are eaiser to solve than the original
	- solutions of the sub-problems can be combined to solve the original

#### Files（文件）

##### MODULES AND FILES（模块和文件）

a module is a .py file containing a collection Python definitions and statements

circle.py

```python
pi = 3.14159

def area(radius):
	return pi * (radius**2)
	
def circumference(radius):
	return 2 * pi * radius	
```

import and use circle module

```python
import circle

pi = 3
print(pi)                       # 3
print(circle.pi)                # 3.14159
print(circle.area(3))           # 28.27431
print(circle.circumference(3))  # 18.849539999999998

```

OTHER IMPORTING

- if we don’t want to refer to functions and variables by their module, and the names don’t collide with other bindings, then we can use:

```
from circle import *
print(pi)
print(area(3))
```
-  this has the effect of creating bindings within the current scope for all objects defined within circle
-  statements within a module are executed only the first time a module is imported

FILES

file handle:

```
nameHandle = open(‘kids’, ‘w’)
```
creates a file named kids and returns file handle which we can name and thus reference. The w indicates that the file is to opened for writing into.

### Lecture 5: Tuples and Lists

#### Tuples（元组）

#### Lists（列表）

#### List Operations（列表操作）

#### Mutation, Aliasing, Cloning（对象改变，对象别名，对象拷贝）

### Lecture 6: Dictionaries

#### Functions as Objects（函数作为对象）

#### Dictionaries（字典）

#### Example with a Dictionary（字典的例子）

#### Fibonacci and Dictionaries（菲波那切数列和字典）

#### Global Variables（全局变量）

### Lecture 7: Debugging

#### Programming Challenges

#### Classes of Tests

#### Bugs

#### Debugging

#### Debugging Examples

### Lecture 8: Exceptions and Assertions

### Lecture 9: Classes and Inheritance

#### Object Oriented Programming（面向对象编程）

#### Class instances（类示例）

#### Methods（方法）

#### Classes Examples（举例）

#### Why OOP（为什么OOP）

#### Hierarchies（层级结构）

#### Class Variables（类变量）

### Lecture 10: An Extended Example

#### Building a Class（创建一个类）

#### Visualizing the Hierarchy（可视化层级结构）

#### Adding another class

#### Using inherited methods

#### Gradebook example

#### Generators

Notes for the [edx](www.edx.org) course [Introduction to Computer Science and Programming Using Python](https://www.edx.org/course/introduction-computer-science-mitx-6-00-1x-5)
