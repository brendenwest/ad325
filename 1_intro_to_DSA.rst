Intro to Data Structures & Algorithms
====
**Summary**
  - Class overview
  - Java programming overview
  - Recursion
  - Data Structures
  - Algorithmic Analysis

**Reading**
  - https://www.coursera.org/learn/algorithms-part1/home/week/1  
  - https://algs4.cs.princeton.edu/10fundamentals/ - Ch. 1.1, 1.2, & 1.4
  - https://www.geeksforgeeks.org/recursion/
  - https://www.geeksforgeeks.org/assertions-in-java/  
 
**Watch**
  - https://www.coursera.org/learn/algorithms-part1/home/week/1 - week 1 videos
  - https://techdevguide.withgoogle.com/paths/foundational/riffing-unit-test-importance/#! 
 
**Practice**
  - Java programming basics - https://practiceit.cs.washington.edu/problem/list (BJP4 chapters 1 - 8)
  - BJP4 Ch. 13 - bigOh 1 -5
 
**Java Programming**

DS&A concepts are language independent, but this class teaches them via Java which students should know from previous classes.

The readings & practice links above provide a recap of Java language features.

This course will make use of several Java features that may be new to students.

- *Generics* - A Java mechanism that allows a class to work for any data type. Classes are defined with a symbolic placeholder for some concrete type to be used in practice.
- *Autoboxing* - Java automatically converts (*casts*) between a primitive type (e.g. *int*) and the corresponding wrapper type (*Integer*).  Automatically casting a wrapper type to a primitive type is known as *unboxing*.
- *Assertions* - Java uses the *assert* command to test if a boolean expression is *true*. Such assertions test the correctness of program assumptions and are the basis of *unit testing*.

**Data Structures & Algorithms**

Data structures & Algorithms (DS&A) describes the concepts around solving programming problems efficiently. As we’ll cover a bit later, ‘correct’ solutions can differ by orders of magnitude in terms of speed & memory usage.

Solutions typically involve questions of how to store & represent data, esp. collections of data. Data structures are ways in which data is arranged in your computer’s memory (or stored on disk).

Data structures have different capabilities that can simplify or complicate common operations such as - search, add, update, delete, count, and sort.

Data structures also vary in terms of computer memory requirements.
 

**Abstract Data Types (ADT’s)**
Programmers commonly use ADT’s to hide implementation details from clients and provide a stable public interface to the data and methods.

Using an ADT allows the programmer to change the underlying algorithm or data storage without affecting clients.

ADT’s typically store data in arrays, which are native to most languages, or in a linked list.

ADT’s can be a composed of arrays, linked lists, and other ADT’s.

**Algorithmic Analysis**
Algorithms are methods for operating on data. Efficient algorithms can greatly speed calculations & even solve previously unsolvable problems.

The study of efficient algorithms is hard to separate from data structures, so these are usually taught together.

Algorithmic analysis uses the scientific method to answer two key questions:
  - How long will a program run?
  - How much memory will a program consume?

Programmers can observe program running time using ‘timer’ commands.

Programmers can also build a mathematical model for total running time based on:
  - Cost of execution of each statement
  - Frequency of execution of each statement

These cost models are functions that describe the program’s ‘order of growth’.

Models are usually simplified by ignoring low-order mathematical terms, to better represent program behavior at extreme scale.

Models allow the evaluation of program efficiency separate from the programming language or run-time environment.

Program run time is typically referred to by the model’s order of growth - e.g. constant, logarithmic, linear, linearithmic, etc.
