Binary Search Trees (BST)
====

**Learning Outcomes**
    - Elementary Symbol Tables
    - Searching a BST
    - Balanced Search Trees

**Reading & Videos**
    - https://www.coursera.org/learn/algorithms-part1/home/week/4  (Elementary Symbol Tables)
    - https://www.coursera.org/learn/algorithms-part1/home/week/5

**Reference**
    - https://algs4.cs.princeton.edu/30searching/ (3.1 - 3.3)
    - https://www.geeksforgeeks.org/binary-search-tree-data-structure/


Symbol Tables
----
A symbol table associates a value with a key, to enable later searches for the value associated with a given key. Table entries are **key-value pairs**.

Symbol tables are sometimes referred to as 'associative arrays' or 'dictionaries'.

.. code-block::

    courses = [
        "ad320": {"instructor": "mchenry", "credits": 5},
        "ad325": {"instructor": "west", "credits": 5},
    ]

Symbol tables typically support basic **insert**, **find**, **get**, and **delete** operations.

Some design considerations for symbol tables:
    - **No duplicate keys**. Inserting a key-value pair where the key already exists, over-writes the existing value
    - **No null values** - keys cannot have 'null' values because null is used for deletion
    - **Deletion** - Keys can be removed immediately (eager deletion) or set to 'null' for later bulk (lazy) deletion
    - **Interation** - clients can iterate through the collection of keys
    - **Key equality** - Objects stored as keys must be comparable.

**Ordered symbol tables** allow key comparison for efficient insert & get operations and keep the table entries in order. This ordering enables a larger set of operations, such as:
    - **min** & **max** - smallest or largest key
    - **floor** & **ceiling** - smallest or largest key relative to a given key
    - **rank** - number of keys less than a given key
    - **range** - number or collection of keys between high and low values

Searching Trees
----
