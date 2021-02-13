Balanced Search Trees
====

**Learning Outcomes**
    - overview of balanced trees
    - AVL trees
    - 2-3 trees
    - Red-Black trees
    - m-Way trees

**Reading & Videos**
    - Carrano & Henry: Chapter 28
    - https://www.coursera.org/learn/algorithms-part1/home/week/5

**Reference**
    - https://algs4.cs.princeton.edu/33balanced/
    - https://www.geeksforgeeks.org/2-3-trees-search-and-insert/
    - https://www.geeksforgeeks.org/red-black-tree-set-1-introduction-2/
    - https://www.geeksforgeeks.org/m-way-search-trees-set-1-searching/

AVL Trees
____

A binary search tree that re-arranges its nodes during add / remove operations to maintain balance.

A node is balanced if the height of its subtrees differ by no more than one level.

Subtree nodes are **rotated** around the node that becomes the new root node.

- **left rotation** - value of node (N) is greater than its parent (P)
    - P becomes left child of N
    - existing left child of N becomes right child of P
    - existing parent of P become parent of N
- **right rotation** - value of node (N) is less than its parent (P).
    - P becomes right child of N.
    - Existing right child of N becomes left child of P
    - Existing parent of P becomes parent of N

Insertion may require **double rotation** to restore balance.

One single or double rotation during insertion of an entry will restore balance in an AVL tree.

2-3 Trees
____

A general search tree whose interior nodes must have either two or three children.
- A 2-node is like a node in a BST
- A 3-node contains two data items and has 3 children
    - data less that the node's first data item occurs in the left subtree
    - data greater than the node's 2nd data item occurs in the right subtree

A 2-3 tree is **completely balanced** with all leaves on the same level. Maintaining balance is easier than with an AVL tree.

Searching 2-nodes behaves like that for a BST.

Searching a 3-node involves checking the node's **middle** subtree if the searched value is between the node's data values.

**Adding entries**
- entries are added to existing leaf nodes to make a 3-node (2 data values)
- if adding an entry would result in 3 data values for the node, the node is split into a root & two children. The middle value moves up a level.

A **2-4 tree** is similar to 2-3 trees but internal nodes may have 3 data values and 4 children.

Red-Black Trees
____

A red-black tree is equivalent to a 2-4 tree but uses only 2-nodes so is easier to implement & can use standard BST search logic.

Each node has a boolean value indicating color (e.g. true = red, false = black)

- the tree root node is **black**
- **black** indicates the original root node
- **red** indicates the node that causes a change in tree height
- every red node has a black parent
- any children of a red node are black
- every path from the root to a leaf has the same number of black nodes
- adding an entry to a non-empty red-black tree results in a new **red** leaf
- The height of a red-blackBST with N nodes is no more than 2 lg N
- The average length of a path from the root to a node in a red-black BST with N nodes is ~1.00 lg N.
- In a red-black BST, the following operations take **logarithmic time** in the worst case: search, insertion, finding the minimum, finding the maximum, floor, ceiling, rank, select, delete the minimum, delete the maximum, delete, and range count.

AVL trees are more balanced than Red-Black Trees, but may cause more rotations during insertion and deletion. So Red-Black trees are preferrable for applications with frequent insertions and deletions.

Applications of red-black trees:
- BST map & set functions (e.g. TreeMap & TreeSet) in Java)
- MySQL table indexes
- K-means clustering in data analysis


m-Way Trees
____

A multiway search tree whose nodes have up to m children.
- k-node has k-1 data items and k children
- a binary search tree is an m-way search tree of order 2,
- not all multiway search trees are balanced
- A B-tree of order m is a balanced multiway search tree that maintains balance with these properties:
    - the root has either no children or between 2 and m children
    - interior nodes have between m/2 and m children
    - all leaves are on the same level
