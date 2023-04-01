# Graphs

### Terminology
- **Graph**: non-linear data structure looked at as a collection of `vertices` (or `nodes`) potentially connected by line segments named `edges`. 
- **Vertex**: also called a node, is a data object that can have zero or more adjacent vertices.
- **Edge**: connection between two nodes.
- **Neighbor**: neighbors of a node are its adjacent nodes, ex. connected via an edge. 
- **Degree**: number of edges connected to a vertex.
- **Undirected graph**: a graph where each edge is **undirected** or **bi-directional**. it does not move in any direction.
- This graph is **bi-directional**:
![bidirectional graph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)
- It has 6 vertices and 7 undirected edges. 
- **Vertices/Nodes** = {a,b,c,d,e,f}
- **Edges** = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}
- **Directed graph**: also called a **Digraph**, is a graph where every edge is directed. each node is directed at another node with a specific requirement of what node should be referenced next. 
- This graph is **directed**:
![directed graph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)
- It has 6 vertices and 8 directed edges. 
- **Vertices** = {a,b,c,d,e,f}
- **Edges** = {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}
- In addition to undirected and directed graphs, we also have acylic and cyclic. 
- **Acyclic graph**: directed graph without cycles. a cycle is when a node can be traversed through and potentially end up back at itself. 
- **Cyclic graph**: has cycles. a cycle is defined as a path of a positive length that starts and ends at the same vertex. 
- Three different types of graphs: completed, connected, and disconnected. 
- **Complete graphs**: when all nodes are connected to all other nodes. 
- **Connected graphs**: all of vertices/nodes have at least one edge. 
- **Disconnected graphs**: where some vertices may not have edges.
- **Graph representation**: through Adjacency Matrix and Adjacency List. 
- **Adjacency Matrix**: represented through a 2-dimensional array. if there are n vertices, then we are looking at an n x n Boolean matrix. 
- **Adjacency List**: most common way to represent graphs. a collection of linked lists or array that lists all of the other vertices that are connected. it makes it easy to view if one vertices connects to another. 
- A **sparse** graph is when there are very few connections. a **dense** graph is when there are many connections. 
- **Weighted graphs**: when numbers are assigned to its edges. these numbers are called weights. 
- **Traversals**: Breadth First and Depth First are used. 
- **Real world usage**: GPS & mapping, driving directions, social networks, airline traffic, and netflix for suggestions of products. 