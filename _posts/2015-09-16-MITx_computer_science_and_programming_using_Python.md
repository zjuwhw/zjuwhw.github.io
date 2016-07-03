---
layout: post
title: Edx-Python学习笔记
tags: [cs, mooc]
---

# Lecture 1: Introduction to computation

## 1.1 Introduction

## 1.2 Basics of Computation

- What does a computer do?
1. Fundamentally a computer: (1) Performs calculations; (2) Remember the results
2. Calculation is: (1) Built in primitives; (2) Creating our own methods of calculations

- So are ther limits?
1. Some problems still too complex
2. Some problems are fundamentally impossible to compute

## 1.3 Types of Knowledge

- Declarative knowledge: statments of facts

- Imperative knowledge: "how to" methods or recipes

## 1.4 Basic Machine Architecture

- Fixed Program Computers

- Stored Program Computers

- What are the basic primitives?
1. Turning shows that using six primitives, can compute anything. (Truning complete)
2. Fortunately, modern programming languages have a more convenient set of primitives.
3. Also have ways to abstract methods to create new "primitives".
4. But anything computable in one language is computable in any other programming language

## 1.5 Programming language characteristics

- Primitive constructs

- Syntax

- Static semantics

- Semantics

# Lecture 2: Core Elements of Programs

## 2.1 Introduction

## 2.2 Types of Programming languages

- Options for programming languages:
1. Source code -> checker -> interpreter -> output
2. Source code -> checker -> compiler -> object code -> interpreter -> output

- Low level: Source code (low level) -> checker -> interpreter -> output

- High level (compiled language): Source code (high level) -> checker -> compiler -> object code (low level) -> interpreter -> output

- High level (interpreted language, such as Python): Source code (high level) -> checker -> interpreter -> output

## 2.3 Python objects

- Python programs
1. Program (or script) is a sequence of definitions and commands
2. Command (or statement) instructs interpreter to do something

- Objects
1. Each object has a **type** that dfeines the kind of things programs can do to it
2. Objecst are: (1) Scalar (*i.e.* cannot be subdivided); (2) Non-scalr (*i.e.* have internal structure that can be accessed)

- Scalr objects
1. int
2. float
3. bool - Boolean values

- Expressions: [object] [operator] [object]

- Operators on ints and floats: +, -, *, /, %, **

- Comparison operators on ints and floats: >, >=, <, <=, ==, !=

- Operators on bools: and, or, not

- Type conversions (type casting): float(3), int(3.9)

## 2.4 Variables and Naming

- assignment: binding variables and values

## 2.5 Strings

- non-scalar objects

- Extracting parts of strings: indexing and slicing

## 2.6 Simple Scripts

- statements (not expressions): *print()*, *raw_input()*

- Comments appear after #

## 2.7 Branching Programs

- Branching programs: the simplest one is a **conditional**

- The indentation is important.

- What have we added?
1. Branching programs allow us to make choices and do different things
2. But still the case that at most, each statement gets executed once.
3. So maximum time to run the program depends only on the length of the program.
4. These programs run in constant time

# Lecture 3: Simple Algorithms

## 3.1 Introduction

## 3.2 Iteration

## 3.3 Guess and check algorithm

## 3.4 Loop mechanisms

## 3.5 Floating point accuracy

## 3.6 Approximate methods

## 3.7 Bisection search

## 3.8 Newton-Paphson root finding



Notes for the [edx](www.edx.org) course [Introduction to Computer Science and Programming Using Python](https://www.edx.org/course/introduction-computer-science-mitx-6-00-1x-5)
