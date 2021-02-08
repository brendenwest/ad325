Trees, Heaps, Priority Queues
====

**Learning Outcomes**
 - Tree structures
 - Binary trees
 - Heaps
 - Priority queues


**Reading & Videos**
 - Carrano & Henry: Chapters 8.34, 24, 25, 27
 - https://www.coursera.org/learn/algorithms-part1/home/week/4

**Reference**
 - https://algs4.cs.princeton.edu/24pq/
 - https://www.geeksforgeeks.org/heap-data-structure/
 - https://www.geeksforgeeks.org/binary-tree-data-structure/ (Sets 1-3)
 

Trees
----

A **tree** is a set of **nodes** connected by **edges** that indicate the relationships between the nodes. The nodes are arranged in **levels** that indicate the hierarchy. The top level has a single node called the **root**.

Nodes at each successive level are **children** of related nodes at the previous level. A node that has children is their **parent**. Nodes that are children of the same parent are **siblings**.

A **leaf** node has no children.

Trees whose nodes are constrained to some number (n) of children are called **n-ary trees**. In a **binary tree*, nodes may have at most two children. 

Tree **height** is the number of levels in the tree. An empty tree has height = 0.

Nodes in a tree are accessed by a **path** starting at the root and following the connected nodes. The number of edges in a path are its **length**.

Binary Trees
----

Each node in a binary tree has at most two children, called the **left child** and **right child**.

**Properties of a binary tree**
 - The maximum number of nodes at level 'l' of a binary tree is 2\ :sup:`l`
 - The Maximum number of nodes in a binary tree of height ‘h’ is 2\ :sup:`h` – 1
 - In a binary Tree with N nodes, minimum height is - Log\ :sub:`2` (N+1) 

**Types of binary trees**
 - **Full** - A binary tree is full if every node has 0 or 2 children.
 - **Complete** - A binary tree is complete  if all the levels are completely filled except possibly the last level, and the last level has all keys to the left as much as possible,
 - **Perfect** - A binary tree is a perfect of all the internal nodes have two children and all leaf nodes are at the same level. A perfect binary tree of height h has 2\ :sup:`h+1` – 1 nodes. 
 - **Balanced** - A binary tree is balanced if the height of the tree is O(Log n), where n is the number of nodes.

Binary trees can be traversed (each node visited), usually through recursive methods that take one of these approaches:
 - **pre-order** - visit all nodes in tree order (starting from root):
    - visit the root,
    - traverse the left sub-tree
    - traverse the right sub-tree
 - **in-order** - visit all the nodes ascending order, based on their key values:
    - traverse the left sub-tree,
    - visit the root,
    - traverse the right sub-tree.
 - **post-order** - useful for deleting a tree or getting 'postfix' expression:
    - traverse the left sub-tree
    - traverse the right sub-tree
    - visit the root


Binary Heap
----

A Binary Heap is a **complete binary tree** structure that can efficiently support priority-queue operations. 

A Binary Heap is either a Min Heap or a Max Heap. In a Min Binary Heap, the root node must have the minimum value among all nodes in the tree. The tree is **heap-ordered**, meaning all nodes in the tree are less than or equal to their children. 

A Max Heap is similar, but with the maximum value at the root and each node larger than or equal to it's children.


Heap operations involve making a simple change that could violate the heap condition, then modifying the heap (**reheapifying**)as needed to restore that heap order. 

 - A **sink** operation is performed when a node becomes larger than it's parent node. The node is exchanged with it's parent, until heap order is restored
 - A **swim** operation is performed when a node becomes smaller than one or both of it's child nodes. The node is exchanged with the larger child until heap order is restored.

- Binary heaps stored in arrays can be traversed through simple arithmetic on array indices,

 Priority Queues
----

Unlike regular FIFO queues, priority queues support removing the item with largest (or smallest) value.

 - Priority queue data can be stored in an array or a linked list
 - Data can be unordered - priority item is identified at 'remove' time
 - Data can be ordered - priority item is moved to correct position when inserted
 - Operations to insert or remove a priority item operation should take linear time in the worst case

 - binary heaps support efficient priority queue operations:
  - Insert. Add the new item at the end of the array, increment the size of the heap, and then swim up through the heap with that item to restore the heap condition.
  - Remove the maximum. We take the largest item off the top, put the item from the end of the heap at the top, decrement the size of the heap, and then sink down through the heap with that item to restore the heap condition.
- In an n-item priority queue, the heap algorithms require no more than 1 + lg n compares for insert and no more than 2 lg n compares for remove the maximum.
