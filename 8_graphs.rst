Graphs
====

**Learning Outcomes**
    - overview of graphs
    - undirected graphs
    - directed graphs
    - graph traversal

**Reading & Videos**
    - Carrano & Henry: Chapter 29, 30
    - https://www.coursera.org/learn/algorithms-part2/home/week/1

**Reference**
    - https://algs4.cs.princeton.edu/41graph/
    - https://algs4.cs.princeton.edu/42digraph/
    - https://www.geeksforgeeks.org/graph-data-structure-and-algorithms/

Overview
----

In computer science, a **Graph** is a non-linear data structure consisting of **nodes** (**vertices**) and **edges**. Nodes are a data structure representing each entity. Edges are the lines that connect any two nodes.

Graphs are useful for solving real-world **network** problems. For example:

    - road maps (nodes = towns)
    - social network (nodes = people)
    - Internet (nodes = pages)

Edges
++++

An edge may be **undirected** if there is a two-way relationship between the nodes it connects, or **directed** if the relationship is one-way (e.g. one-way streets).

A graph with directed edges is called a directed graph or **digraph**.

Edges may have an associated **weight** or **cost** (e.g. road distance, driving time, etc.).

Paths
++++

A **path** between two nodes in a graph is a sequence of edges, where path length is the number of edges.

A **cycle** is a path that begins and ends at the same node and a **simple cycle** passed through other nodes ony once each.

The weight of a path in **weighted graph** is the sum of its edge weights. Algorithms can use weights to choose from among multiple valid paths (e.g. to minimize cost).

Connected Graphs
++++

A **connected** graph has a path between every pair of nodes and is **complete** if every node is connected to every other node. A **disconnected** graph has some nodes that can't be reached from all other nodes.
