## Graphs 

A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

Here is some common terminology used when working with Graphs:

1- Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
2- Edge - An edge is a connection between two nodes.
3- Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
4-Degree - The degree of a vertex is the number of edges connected to that vertex.


* Undirected Graphs

An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

For example, in the graph below, Node C is connected to Node A, Node E and Node B. There are no “directions” given to point to specific vertices. The connection is bi-directional.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)


The undirected graph we are looking at has 6 vertices and 7 undirected edges.

Vertices/Nodes = {a,b,c,d,e,f}

Edges = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}


* Directed Graphs (Digraph)

A Directed Graph also called a Digraph is a graph where every edge is directed.


Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

Compare the visual below with the undirected graph above. Can you see the difference? The Digraph has arrows pointing to specific nodes.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)


he directed graph above has six vertices and eight directed edges

Vertices = {a,b,c,d,e,f}

Edges = {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}

## Complete vs Connected vs Disconnected
There are many different types of graphs. This depends on how connected the graphs are to other node/vertices.

The three different types are completed, connected, and disconnected.


 * Complete Graphs
A complete graph is when all nodes are connected to all other nodes.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/CompleteGraph.PNG)

 * Connected
A connected graph is graph that has all of vertices/nodes have at least one edge. 
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/ConnectedGraph.PNG)

 * Disconnected 
A disconnected graph is a graph where some vertices may not have edges.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DisconnectedGraph.PNG)



## Acyclic vs Cyclic 

### Acyclic Graph
An acyclic graph is a directed graph without cycles.

A cycle is when a node can be traversed through and potentially end up back at itself.

Here is an example of 3 acyclic graphs:

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/threeAcyclic.png)


### Cyclic Graphs
A Cyclic graph is a graph that has cycles.

A cycle is defined as a path of a positive length that starts and ends at the same vertex.

Here is an example of a two different cyclic graph:

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/cyclic.PNG)



### Graph Representation
We represent graphs through:

* Adjacency Matrix
* Adjacency List
