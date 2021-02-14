Hashing
====

**Learning Outcomes**
    - overview of hashing
    - hash functions
    - index hashing
    - collision handling

**Reading & Videos**
    - Carrano & Henry: Chapter 22, 23
    - https://www.coursera.org/learn/algorithms-part1/home/week/6

**Reference**
    - https://algs4.cs.princeton.edu/34hash/
    - https://www.geeksforgeeks.org/hashing-data-structure/

Overview
----

**Hashing** is a technique for implementing a dictionary that can ideally result in O(1) (constant) search times.

Hashing determines the array **index** of an entry based on its search key. Entries can then be accessed directly according to their index.

Arrays constructed through hashing are called **hash tables**. In most cases, hash tables are **sparse*, with only a few elements used.

While useful for searching, hashing cannot provide traversal of search keys in sorted order.

Hash Functions
----
A **hash function** produces an integer (**hash index**) based on search key to determine the entry's array index position.

Typical (index) hashing involves:
    1 - Converting the search key to an integer (**hash code**)
    2 - Compressing the hash code into the range of indices for the hash table

Basic indexing can result in **collisions**, where  different search keys map to the same index.

**Perfect** hash functions should produce a unique index for each unique search key.

**Good** hash functions should:
    - minimize collisions
    - be fast to compute

A hash function can reduce the chance of collision by distributing entries uniformly throughout the hash table.

Hash code computation should always return the same code for the same input data.

Some common approaches for hashing:
    - Use all or part of the data for each key (e.g. part of a phone number)
    - **modular hashing** - choose a prime number M for array size. For any **positive integer** k, compute the remainder (modulus) when dividing k by M. For **floating-point numbers**, use binary representation of the key.
    - **Strings** - compute a modular hash value based on value & position of each character:

.. code-block::

    int hash = 0;
    for (int i = 0; i < s.length(); i++)
        hash = (R * hash + s.charAt(i)) % M;


Collision Handling
----

**Open Addressing**

**Linear Probing**

**Separate Chaining**