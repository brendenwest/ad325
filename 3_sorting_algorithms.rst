Sorting Algorithms
====

Key Topics
----------
- Elementary sorting algorithms
- Comparable interfaces
- Advanced sorting algorithms
 
Reading & Videos
----------------
- Carron & Henry: Chapters 15 - 16, Interlude 5 Generics
- https://www.coursera.org/learn/algorithms-part1/home/week/2 - Elementary Sorts
- https://www.coursera.org/learn/algorithms-part1/home/week/3 

Reference
---------
- https://algs4.cs.princeton.edu/20sorting/
- https://www.geeksforgeeks.org/sorting-algorithms/ 
- https://www.geeksforgeeks.org/recursion/  

Key Concepts
------------
- **comparable** -  data to be sorted must be comparable - e.g. implement Java's Comparable interface
- **recursion** - The process in which a function calls itself directly or indirectly. Can achieve results similar to loop, but with different memory usage.
- **cost model** - number of compares and exchanges (or array accesses).
- **best, worst, average cases** - a sorting algorithm's performance can vary in different cases - e.g. whether input data is already sorted.
- **memory usage** - in-place sorting algorithms use constant extra space by modifying elements in the existing array or list. Others use extra memory to hold another copy of the array to be sorted.
- **stability** - output from a stable sorting algorithm has objects with equal values in the same order as in the original input. https://www.geeksforgeeks.org/stability-in-sorting-algorithms/ (Links to an external site.)Links to an external site. 
- **divide-and-conquer** - is an algorithmic paradigm that solves a problem using following three steps:

  1. Divide: Break the given problem into subproblems of same type.
  2. Conquer: Recursively solve these subproblems
  3. Combine: Appropriately combine the answers
 

Elementary Sort algorithms
---------------

**Selection sort**
Select the smallest item in the array, and exchange it with the first entry. Then, find the next smallest item and exchange it with the second entry. Continue in this way until the entire array is sorted.

- average case: uses ~N\ :sup:`2`/2 compares and N exchanges 

**Insertion sort**
consider items one at a time, swapping the current item with larger items to the left.

- average case: for randomly ordered arrays, uses ~N\ :sup:`2`/4 compares and ~N\ :sup:`2`/4 exchanges.
- worst case is ~ N\ :sup:`2`/2 compares and ~ N\ :sup:`2`/2 exchanges 
- best case is N-1 compares and 0 exchanges
- works well for certain types of non-random arrays such as partially sorted arrays

**Shell sort**
a simple extension of insertion sort that gains speed by allowing exchanges of entries that are far apart, to produce partially sorted arrays that can be efficiently sorted, eventually by insertion sort.

- The number of compares used by shellsort is ~ O(N\ :sup:`3/2`)
