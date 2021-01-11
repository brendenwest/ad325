Stacks & Queues
====

Key Topics
----------
- Stacks
- Queues
- Iterators
 
Reading
-------
- https://www.coursera.org/learn/algorithms-part1/home/week/2  
- Carron & Henry: Chapters 5 - 8, Interlude 4 Iterators
- https://algs4.cs.princeton.edu/13stacks/  (review)
- https://www.geeksforgeeks.org/stack-data-structure/ (review)
- https://www.geeksforgeeks.org/queue-data-structure/ (review)
 

Watch
-----
- https://www.coursera.org/learn/algorithms-part1/home/week/2 - videos for stacks & queues

Stack
-----
A data collection based on last-in, first-out (LIFO) principle.

- Stack items are accessed in reverse order of being added
- Useful for reversing items in a collection without knowing  total count
- Common stack operations:
  - push - add an item to top of the stack
  - pop - remove top item from the stack
  - peek - retrieve top item without removing from the stack
  - isEmpty - True if the stack has no items
  - size - number of items on the stack
- Common uses of stacks:
  - browser history
  - mobile application screens
  - evaluating arithmetic expressions
- Stacks can use a linked-list or an array for data storage
  - for linked-list implementation, it's most efficient to treat first node as 'top' of stack. Stack operations for linked-list implementation are O(1).
  - for array implementation, it's most efficient to treat last occupied element as top of stack. Stack operations for array implementation are O(1), except for resizing the array when full.

Queue
-----
A data collection based on first-in, first-out (FIFO) principle. Similar to stack, but operations happen at both ends of the collection.

- Data items are organized in the order received - earliest item is at the front and most recently added item is at the back
- Common Queue operations:
  - enqueue - add an item to end of queue
  - dequeue - remove item from front of queue
  - isEmpty
  - size
- Double-ended queue (Deque) is similar to a queue, but items can be added/removed from either end
- Priority queue orders items by importance rather than arrival time. Requires that items be **Comparable**