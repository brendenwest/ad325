Binary Search Trees (BST)
====

**Learning Outcomes**
    - Elementary Symbol Tables
    - Binary Search Trees
    - Searching a BST
    - Balanced Search Trees

**Reading & Videos**
    - Carrano & Henry: Chapters 20, 21, 26
    - https://www.coursera.org/learn/algorithms-part1/home/week/4  (Elementary Symbol Tables)
    - https://www.coursera.org/learn/algorithms-part1/home/week/5

**Reference**
    - https://algs4.cs.princeton.edu/30searching/ (3.1 - 3.3)
    - https://www.geeksforgeeks.org/binary-search-tree-data-structure/


Symbol Tables
----
A symbol table associates a value with a key to enable later searches for the value associated with a given key. Table entries are **key-value pairs**.

Symbol tables are sometimes referred to as 'associative arrays' or 'dictionaries'.

.. code-block::

    words = [
        {"the": 25},
        {"house": 2},
        {"tv": 1}
    ]

Dictionaries typically support basic **insert**, **find**, **get**, and **delete** operations.

Some design considerations for symbol tables:
    - **No duplicate keys**. Inserting a key-value pair where the key already exists, over-writes the existing value
    - **No null values** - keys cannot have 'null' values because null is used for deletion
    - **Deletion** - Keys can be removed immediately (eager deletion) or set to 'null' for later bulk (lazy) deletion
    - **Interation** - clients can iterate through the collection of keys
    - **Key equality** - Objects stored as keys must be comparable.

Dictionaries can be implemented using arrays or linked lists. Array implementation may use a single array, where each **entry** is an object containing key-value pair, or use two synchronized arrays - one for keys and one for values.

Worst-case performance is generally O(n) for operations in both sorted and unsorted dictionaries, whether using an array or linked list, except retrieval from a sorted array-based dictionary is O(log n) at worst.

**Ordered symbol tables** allow key comparison for efficient insert & get operations and keep the table entries in order. This ordering enables a larger set of operations, such as:
    - **min** & **max** - smallest or largest key
    - **floor** & **ceiling** - smallest or largest key relative to a given key
    - **rank** - number of keys less than a given key
    - **range** - number or collection of keys between high and low values

BST Operations
----

A BST is a binary tree that meets these conditions:
    - each node contains a **comparable** object
    - a node's data is greater than any data in the node's left subtree
    - a node's data is less than any data in the node's right subtree (for unique values)
    - a node's data is less than or equal to any data in the node's right subtree (for duplicate values)

The tree's largest value will be the right-most node and its smallest value will be the left-most node.

BST's support basic **database** operations through recursive methods:

**Add** - adds an entry to the tree. In case of unique values, overwrites any existing value.

**Search** - returns boolean indicating whether requested entry is in the tree

**Retrieve** - returns the requested entry, or entries in case of duplicate values.

**Remove** - removes and returns the requested entry, or entries in case of duplicate values. Code needs to account for scenarios where removed node has a) one child or b) two children.

**Traverse** - as with binary trees, BST's can be traversed **in-order** to visit entries in ascending order.

Where a tree supports duplicate entries, class designer needs to determine if retrieve and remove operations should affect the first occurence of an entry or all occurences.

Searches begin at the root and the max number of comparisons for each operation is directly proportional to tree height - add, remove, and retrieve are O(h).

Worst case for an unbalanced tree is O(n) and for a **height-balanced** tree is O(log n).

Adding items to an empty tree in random order will result in a tree that is approximately balanced.
