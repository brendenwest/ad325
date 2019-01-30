Stacks & Queues
====

Key Topics
----------
- Linked Lists
- Stacks
- Queues
- Generics
- Iterators
 
Reading
-------
- https://www.coursera.org/learn/algorithms-part1/home/week/2  
- Sedgewick - Ch. 1.3
- https://algs4.cs.princeton.edu/13stacks/  (review)
- Lafore (optional) - Ch 4 - Stacks & Queues, Ch 5 - Linked Lists
- https://www.geeksforgeeks.org/data-structures/linked-list/
 

Watch
-----
- https://www.coursera.org/learn/algorithms-part1/home/week/2 - videos for stacks & queues
 
DS&A are frequently concerned with collections of data and related operations such as adding, 
removing, or examining objects. Collections can use fundamental abstract data types such as bag,
stack, or queue. Choice of collection structure can affect performance of required operations. 
Collections can use arrays or linked lists for their underlying data storage.

Linked Lists
------------
Linked Lists are a fundamental alternative to arrays for structuring a collection of items.

- Not native to Java
- Recursive structure that’s either null or a node w/ data & reference to a linked list
- Sequence of items, where each item links to next item in list (single linked list)
- In double linked list, items also have a link to ‘previous’ item
- Does not require contiguous memory
- Does not require advance sizing
- Can be used for any type of data,
- Items can’t be accessed by index
- Items can be added/removed more easily than for arrays but can require ‘traversing’ the list
 

Stack
-----
A data collection based on last-in-first-out (LIFO) principle.

- Stack items are iterated in reverse order of being added
- Useful for reversing items in a collection without advance knowledge of total number
- Stack operations:
  - push()
  - pop()
  - isEmpty()
  - size()
 
Queue
-----
A data collection based on first-in-first-out (FIFO) principle. Very similar methods to 
stack but:

- Data items are operated on in same order as received
- Queue operations:
  - enqueue() - add an item to end
  - dequeue() - remove oldest item
  - isEmpty()
  - size()
