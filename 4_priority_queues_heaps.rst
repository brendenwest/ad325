Priority Queues & Heaps
====

**Learning Outcomes**
 - Priority queues
 - Tree structures
 - Binary trees
 - Heaps


**Reading & Videos**
 - Carrano & Henry: Chapters 8.34, 24, 27
 - https://www.coursera.org/learn/algorithms-part1/home/week/4

**Reference**
 - https://algs4.cs.princeton.edu/24pq/


Priority Queues
----

Unlike regular FIFO queues, priority queues support removing the item with largest (or smallest) value.

 - Priority queue data can be stored in an array or a linked list
 - Data can be unordered - priority item is identified at 'remove' time
 - Data can be ordered - priority item is moved to correct position when inserted
 - Operations to insert or remove a priority item operation should take linear time in the worst case

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

The binary heap is a data structure that can efficiently support the basic priority-queue operations. In a binary heap, the items are stored in an array such that each key is guaranteed to be larger than (or equal to) the keys at two other specific positions.

 - A binary tree is heap-ordered if the key in each node is larger than (or equal to) the keys in that node's two children (if any).
 - The largest key in a heap-ordered binary tree is found at the root.
 - Binary heaps can be traversed through simple arithmetic on array indices
 - Heap operations involve making a simple change that could violate the heap condition, then traveling through the heap, modifying the heap as required to ensure that the heap condition is satisfied everywhere. We refer to this process as *reheapifying* - restoring heap order.
 - binary heaps support efficient priority queue operations:
  - Insert. Add the new item at the end of the array, increment the size of the heap, and then swim up through the heap with that item to restore the heap condition.
  - Remove the maximum. We take the largest item off the top, put the item from the end of the heap at the top, decrement the size of the heap, and then sink down through the heap with that item to restore the heap condition.
- A **sink** operation is performed when a node becomes larger than it's parent node. The node is exchanged with it's parent, until heap order is restored
- A **swim** operation is performed when a node becomes smaller than one or both of it's child nodes. The node is exchanged with the larger child until heap order is restored.
- In an n-item priority queue, the heap algorithms require no more than 1 + lg n compares for insert and no more than 2 lg n compares for remove the maximum.
