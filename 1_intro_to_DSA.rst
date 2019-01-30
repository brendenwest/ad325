Intro to Data Structures & Algorithms
====
**Summary**
  - Class overview
  - Java programming overview
  - Data Structures
  - Algorithmic Analysis

**Reading**
  - https://www.coursera.org/learn/algorithms-part1/home/week/1  
  - Sedgewick - Ch. 1.1, 1.2, & 1.4
  - (optional) Lafore - Ch 1 - Overview, Ch 2 - Basics of Arrays, Classes, Logarithms, Big O Notation
  - https://www.geeksforgeeks.org/assertions-in-java/  
 
**Watch**
  - https://www.coursera.org/learn/algorithms-part1/home/week/1 - week 1 videos
  - https://techdevguide.withgoogle.com/paths/foundational/riffing-unit-test-importance/#! 
 
**Practice**
  - Students can practice their understanding of Java programming basics through the BJP4 exercises for chapters 1 - 8, at https://practiceit.cs.washington.edu/problem/list 
  - BJP4 Ch. 13 - bigOh 1 -5
 
**Java Programming**

DS&A concepts are independent of any specific programming language. But this class teaches them via Java, which students should know from their previous class.

Sedgewick Ch. 1.1 covers basics of Java programming as a refresher.

Students can practice their understanding of Java basics through the BJP4 exercises for chapters 1 - 8, at https://practiceit.cs.washington.edu/problem/list. 

Sedgewick Ch. 1.2 covers abstraction and object-oriented programming in the context of Java.

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
