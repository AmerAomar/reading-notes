# Reading Class 35: Graphs

[Link to the article](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)

WHY are graphs important?
Graphs are fundamental data structures used in computer science and mathematics to model and analyze relationships between objects or entities. They provide a flexible and powerful way to represent complex networks, enabling efficient problem-solving in various domains such as social networks, transportation systems, computer networks, recommendation systems, and more. By understanding graphs, you gain a versatile toolset to tackle a wide range of real-world problems.

WHAT is a graph?
In computer science, a graph is a collection of vertices (also known as nodes) and edges. Vertices represent the objects or entities in the system, and edges represent the connections or relationships between them. A graph can be used to describe intricate relationships between different entities, such as friendships in a social network, interconnected web pages on the Internet, or the flow of goods in a supply chain.

HOW are graphs represented?
There are two primary ways to represent a graph: adjacency matrix and adjacency list.

1. Adjacency Matrix: An adjacency matrix is a two-dimensional matrix where rows and columns represent the vertices. If there is an edge between vertex i and vertex j, the corresponding cell in the matrix will be marked as 1 or contain a weight if the graph is weighted. If there is no edge between the vertices, the cell will be marked as 0. The adjacency matrix is symmetric for an undirected graph, as the presence of an edge between i and j is the same as between j and i.

2. Adjacency List: An adjacency list is a collection of linked lists or arrays where each vertex maintains a list of its adjacent vertices. This representation is more memory-efficient for sparse graphs (graphs with relatively fewer edges) compared to the adjacency matrix. Each vertex stores a list of its neighbors, allowing for efficient traversal of the graph.

Graphs can also be classified based on their characteristics:

- Directed Graphs: In a directed graph, also known as a digraph, the edges have a specific direction. The edges indicate a one-way relationship between vertices, representing actions, dependencies, or flows. For example, a directed graph can be used to model the flow of information in a computer network or the relationships in a web of hyperlinks.

- Undirected Graphs: In an undirected graph, the edges do not have a specific direction. The connections between vertices are bidirectional, allowing information, relationships, or interactions to flow in both directions. An undirected graph can represent symmetric relationships, such as friendships in a social network or connections between web pages.

- Weighted Graphs: In a weighted graph, each edge is assigned a weight or cost. The weight represents a value associated with the relationship between two vertices. Weighted graphs are commonly used to model scenarios where the connections have varying strengths, such as distances between cities or the cost of traveling through different routes.

Understanding graphs enables the application of various graph algorithms and techniques. Some commonly used algorithms include:

- Depth-First Search (DFS): Traverses a graph by exploring as far as possible along each branch before backtracking. DFS is useful for tasks like detecting cycles, exploring connected components, and traversing paths.

- Breadth-First Search (BFS): Traverses a graph by exploring all the neighbors of a vertex before moving on to their neighbors. BFS is employed for tasks like finding the shortest path, calculating distances, and exploring graphs layer by layer.

- Dijkstra's Algorithm: Finds the shortest path between two vertices in a weighted graph. It is commonly used in navigation systems, network routing, and resource allocation.

- Kruskal's Algorithm: Constructs a minimum spanning tree, which is a tree that spans all vertices in a connected, weighted graph with the minimum total edge weight. Minimum spanning trees have applications in network design, clustering, and optimization.

By leveraging these algorithms and representations, you can efficiently analyze graphs, extract valuable insights, optimize processes, and solve a wide range of graph-related problems.
