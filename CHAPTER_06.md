## Graph
- A Graph is a non-linear data structure consisting of vertices and edges.
- Graph is composed of a non-empty set of vertices( V ) and a set of edges( E ).
- The graph is denoted by G(V, E).
## Directed Graph:
- A graph in which every edge is directed is called directed graph or digraph.
## Undirected Graph:
- A graph in which every edge is undirected is called undirected graph.
<p float="left">
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20200630111809/graph18.jpg" width=30% >
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20200630114438/directed.jpg" width=30%>
</p>

## Tree Traversal
- The following are the techniques for traversing the trees:
1. Preorder
  - Visit the root.
  - Traverse the left sub tree in preorder.
  - Traverse the right sub tree in preorder.
2. Inorder
  - Traverse the left sub tree in inorder.
  - Visit the root.
  - Traverse the right sub tree in inorder.
3) Postorder
  - Traverse the left sub tree in Post order.
  - Traverse the right sub tree in Post order.
  - Visit the root
  
## Graph Traversals
- Graph traversal refers to the process of visiting each vertex in a graph. 
- Such traversals are classified by the order in which the vertices are visited. 
- Tree traversal is a special case of graph traversal.
- The graph has two types of traversal algorithms. 
- These are called the Breadth First Search and Depth First Search.

## DFS - Depth First Search Algorithm
- Graph traversal means visiting all the nodes of a graph.
- The graph has two types of traversal algorithms. 
- These are called the Breadth First Search and Depth First Search.
- Depth first Search or Depth first traversal is a recursive algorithm for searching all the vertices of a graph or tree data structure. 
#### Application of DFS Algorithm
- For finding the path
- For finding the strongly connected components of a graph
- For detecting cycles in a graph
#### Complexity of Depth First Search
- The time complexity of the DFS algorithm is  O(V + E), where V is the number of nodes and E is the number of edges.
- The space complexity of the DFS algorithm is O(V).
#### DFS Pseudocode or Algorithm
```ruby

procedure dfsearch(G)
  for each v Є N do 
    mark[v] ← not-visited
  for each v Є N do
    if mark[v] ≠ visited 
     then dfs(v)
    
procedure dfs(v)
  {Node v has not previously been visited}
  mark[v] ← visited
  for each node w adjacent to v do
    if mark[w] ≠ visited 
      then dfs(w)
```

#### Depth First Search Example
<a href="https://www.programiz.com/dsa/graph-dfs"> DFS EXAMPLE </a>

## BFS - Breadth First Search Algorithm
- Graph traversal means visiting all the nodes of a graph.
- The graph has two types of traversal algorithms. 
- These are called the Breadth First Search and Depth First Search.
- Breadth First Traversal or Breadth First Search is a recursive algorithm for searching all the vertices of a graph or tree data structure.

#### BFS Algorithm Applications
- For GPS navigation
- Path finding algorithms
- Cycle detection in an undirected graph
- In minimum spanning tree

#### BFS Algorithm Complexity
- The time complexity of the BFS algorithm is O(V + E), where V is the number of nodes and E is the number of edges.
- The space complexity of the algorithm is O(V).
#### BFS Pseudocode or Algorithm
```ruby

procedure search(G)
  for each v ε N do 
    mark[v] ← not visited
  for each v ε N do
    if mark[v] ≠ visited
      then bfs(v)

procedure bfs(v)
  Q ← empty-queue
  mark[v] ← visited
  enqueue v into Q
  while Q is not empty do
    u ← first(Q)
    dequeue u from Q
  for each node w adjacent to u do
    if mark[w] ≠ visited
      then mark[w] ← visited
    enqueue w into Q
```
#### Breadth First Search Example
<a href="https://www.programiz.com/dsa/graph-bfs"> BFS EXAMPLE </a>

## DFS VS BFS
| No.        | Parameters                              | BFS                                                                                                                                                                   | DFS                                                                                                                                                                                      |
|------------|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.         | Stands for                              | BFS stands for Breadth First Search.                                                                                                                                  | DFS stands for Depth First Search.                                                                                                                                                       |
| 2.         | Data Structure                          | BFS(Breadth First Search) uses Queue data structure for finding the shortest path.                                                                                    | DFS(Depth First Search) uses Stack data structure.                                                                                                                                       |
| 3.         | Definition                              | BFS is a traversal approach in which we first walk through all nodes on the same level before moving on to the next level.                                            | DFS is also a traversal approach in which the traverse begins at the root node and proceeds through the nodes as far as possible until we reach the node with no unvisited nearby nodes. |
| 4.         | Technique                               | BFS can be used to find a single source shortest path in an unweighted graph because, in BFS, we reach a vertex with a minimum number of edges from a source vertex.  | In DFS, we might traverse through more edges to reach a destination vertex from a source.                                                                                                |
| 5.         | Conceptual Difference                   | BFS builds the tree level by level.                                                                                                                                   | DFS builds the tree sub-tree by sub-tree.                                                                                                                                                |
| 6.         | Approach used                           | It works on the concept of FIFO (First In First Out).                                                                                                                 | It works on the concept of LIFO (Last In First Out).                                                                                                                                     |
| 7.         | Suitable for                            | BFS is more suitable for searching vertices closer to the given source.                                                                                               | DFS is more suitable when there are solutions away from source.                                                                                                                          |
| 8.         | Suitable for Decision Treestheirwinning | BFS considers all neighbors first and therefore not suitable for decision-making trees used in games or puzzles.                                                      | DFS is more suitable for game or puzzle problems. We make a decision, and the then explore all paths through this decision. And if this decision leads to win situation, we stop.        |
| 9.         | Time Complexity                         | The Time complexity of BFS is O(V + E) when Adjacency List is used and O(V^2) when Adjacency Matrix is used, where V stands for vertices and E stands for edges.      | The Time complexity of DFS is also O(V + E) when Adjacency List is used and O(V^2) when Adjacency Matrix is used, where V stands for vertices and E stands for edges.                    |
| 10.        | Visiting of Siblings/ Children          | Here, siblings are visited before the children.                                                                                                                       | Here, children are visited before the siblings.                                                                                                                                          |
| 11.        | Removal of Traversed Nodes              | Nodes that are traversed several times are deleted from the queue.                                                                                                    | The visited nodes are added to the stack and then removed when there are no more nodes to visit.                                                                                         |
| 12.        | Backtracking                            | In BFS there is no concept of backtracking.                                                                                                                           | DFS algorithm is a recursive algorithm that uses the idea of backtracking                                                                                                                |
| 13.        | Applications                            | BFS is used in various applications such as bipartite graphs, shortest paths, etc.                                                                                    | DFS is used in various applications such as acyclic graphs and topological order etc.                                                                                                    |
| 14.        | Memory                                  | BFS requires more memory.                                                                                                                                             | DFS requires less memory.                                                                                                                                                                |
| 15.        | Optimality                              | BFS is optimal for finding the shortest path.                                                                                                                         | DFS is not optimal for finding the shortest path.                                                                                                                                        |
| 16.        | Space complexity                        | In BFS, the space complexity is more critical as compared to time complexity.                                                                                         | DFS has lesser space complexity because at a time it needs to store only a single path from the root to the leaf node.                                                                   |
| 17.        | Speed                                   | BFS is slow as compared to DFS.                                                                                                                                       | DFS is fast as compared to BFS.                                                                                                                                                          |
| 18.        | When to use?                            | When the target is close to the source, BFS performs better.                                                                                                          | When the target is far from the source, DFS is preferable.                                                                                                                               |


## Topological Sorting
- Topological sorting is a linear ordering of vertices such that for every directed edge (u,v) , vertex u comes before v in the ordering.
- Topological Sorting is possible if the graph is Directed Acyclic Graph (DAG).
- In DFS, we print a vertex and then recursively call DFS for its adjacent vertices. 
- In topological sorting, we need to print a vertex before its adjacent vertices. 
- Time Complexity: O(V+E). 
- Auxiliary space: O(V). The extra space is needed for the stack.
#### Applications of Topological Sorting:
- Topological Sorting is mainly used for scheduling jobs from the given dependencies among jobs. 
- In computer science, applications of this type arise in:
- Instruction scheduling
- Ordering of formula cell evaluation when recomputing formula values in spreadsheets
- Logic synthesis
- Determining the order of compilation tasks to perform in make files
- Data serialization
- Resolving symbol dependencies in linkers
#### Example 
<img src="https://assets.leetcode.com/users/images/63bd7ad6-403c-42f1-b8bb-2ea41e42af9a_1613794080.8115625.png" width=50%>

## Articulation point
- A vertex is said to be an articulation point in a graph if removal of the vertex and associated edges disconnects the graph.
<img src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/ArticulationPoints21-300x177.png" width=50%>

## Connected Component
- A connected component or simply component of an undirected graph is a subgraph in which each pair of nodes is connected with each other via a path.
- In connected components, all the nodes are always reachable from each other.
- The undirected graph has three connected components:
<img src="https://www.baeldung.com/wp-content/uploads/sites/4/2020/05/3-component.png" width=50%>
