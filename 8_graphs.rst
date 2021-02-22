Graphs
====

**Learning Outcomes**
    - overview of graphs
    - directed & undirected graphs
    - graph traversal
    - graph implementation

**Reading & Videos**
    - Carrano & Henry: Chapter 29, 30
    - https://www.coursera.org/learn/algorithms-part2/home/week/1

**Reference**
    - https://algs4.cs.princeton.edu/41graph/
    - https://algs4.cs.princeton.edu/42digraph/
    - https://www.geeksforgeeks.org/graph-data-structure-and-algorithms/

Overview
----

In computer science, a **Graph** is a non-linear data structure consisting of **vertices** (**nodes**) and **edges**. Vertices are a data structure representing each entity. Edges are the lines that connect any two vertices.

Graphs are useful for solving real-world **network** problems. Some examples, with vertices in parens:
    - road maps (towns)
    - social network (people)
    - airline routes (airports)
    - mazes (corners & ends)
    - college degree programs (courses)

Unlike other data structures, graphs are not modified after being created. Instead they are used to answer questions about how vertices are related.

All trees are connected graphs with hierarchical order and without cycles.

Edges
++++

An edge may be **undirected** if there is a two-way relationship between the vertices it connects, or **directed** if the relationship is one-way (e.g. one-way streets).

A graph with directed edges is called a directed graph or **digraph**.

Edges may have an associated **weight** or **cost** (e.g. road distance, driving time, etc.).

Paths
++++

A **path** between two vertices in a graph is a sequence of edges, where path length is the number of edges.

A **cycle** is a path that begins and ends at the same vertex and a **simple cycle** passed through other vertices ony once each.

The weight of a path in **weighted graph** is the sum of its edge weights. Algorithms can use weights to choose from among multiple valid paths (e.g. to minimize cost).

A **connected** graph has a path between every pair of vertices and is **complete** if every vertex is connected to every other vertex. A **disconnected** graph has some vertices that can't be reached from all other vertices.

Adjacency
++++

Two vertices in an undirected graph are **adjacent** (aka **neighbors**) if joined by an edge.

In a directed graph, the vertex at the end of the directed edge is adjacent to the vertex at the beginning.

Traversal
____

Graph applications focus on the connections between vertices, rather than the contents of vertices.

A graph traversal can begin from any vertex (**origin vertex**) and visits only vertices it can reach.

Visited vertices are marked to avoid repeated visits.

The order in which neighbors are visited can vary according a graph's implementation.

Breadth-first Search (BFS)
++++

A **breadth-first** search visits each of a vertex's neighbors before visiting neighbors of neighbors and so on. Level-order tree traversal is an example of BFS.

BFS uses a queue to hold the visited vertices and traversal order is the order that vertices are added to the queue.

Depth-first Search (DFS)
++++

A **depth-first** search follows a single path as deeply as possible before following other paths. Inorder, preorder, and postorder traversal are examples of DFS.

DFS traversal can be recursive and uses a stack to track visited vertices. The traversal order is the order in which vertices are added to the stack.

DFS is useful to determine the path between two vertices.

Topological Order
++++

Vertices in a directed graph without cycles can be placed in **topological order** (in order of their precedence).

Such a graph may have more than one valid topological order.

Graphs with a cycle cannot have a topological order because this would result in circular logic.

**Topological sort** is the process for discovering the topological order for vertices in a graph. It uses a stack to hold vertices that have no successor or whose neighbors have been visited.

Graph Implementation
----

Data about graph edges can be stored either in an **adjacency matrix** or an **adjacency list**.

Adjacency Matrix
++++

This is a two-dimensional array of size V rows and V columns, where V is the number of vertices in the graph.

For an unweighted graph, the adjacency matrix would have boolean values for each edge. For a weighted graph, the matrix value would be the edge weight or infinity if no edge exists.

Determining if an edge exists for two vertices is a O(1) operation, but finding all the neighbors of a vertex is O(V).

The adjacency matrix requires fixed space for all possible edges, even though graphs are usually sparse. It can be a good choice for a dense graph.

Adjacency List
++++

An adjacency list maintains a vertex-indexed array of lists. For each vertex, the array contains a list of its neighbors and represents the edges that originate from this vertex.

Space is reserved only for edges that exist, so this approach uses less memory.

Determining if an edge exists between two vertices, or finding all the neighbors of a vertex, is O(n) at worst but faster on average.

Vertices & Edges
++++
Graph implementations typically include:

- A **Vertex** object that is similar to a tree node. The object has attributes for vertex data, whether the vertex is visited, and the vertex's edges.
- An **Edge** object that includes weight (if any) and a reference to the vertex that ends the edge.
