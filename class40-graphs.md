# Reading 40 - Graphs - 6/5/2020  

### Graphs 
A non-linear data structure that can be looked at as a collection of `vertices/nodes` poentially connected by line segments named `edges`.  
* Common Terminology  
  * Vertex - A vertex, also called a `node`, is a data object that can have zero or more adjacent vertices  
  * Edge - An dege is a connection between two nodes  
  * Neighor - The neighbors of a node are its adjacent nodes  
  * Degree - The degree of a vertex is the number of edges connected to that vertex 

### Directed vs Undirected 
* An `Undirected Graph` is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction 
* A `Directed Graph` is a graph where every edge is directed. Each node is directed at another node with a specific requirement of what node should be referenced next  

### Complete vs Connected vs Disconnected  
* Complete Graph - when all nodes are connected to all other nodes 
* Connected Graph - all of `vertices/nodes` have at least one edge 
* Disconnected Graph - where some vertices may not have edges 

### Acyclic vs Cyclic 
* Acyclic Graph - a directed graph without cycles. A cycle is when a node can be traversed through and potentially end up back at itself  
* Cyclic Graph - a graph that has cycles. A cycle is defined as a path of a positive length that starts and ends at the same vertax 

### Graph Representation  
* Adjacency Matrix - represented through a 2D array. Each row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn't a connection  
* Adjacency List - a collection of linked lists or array that lists all of the other vertices that are connected. It makes it easy to view if one vertice connects to another 

### Traversals  
* Breadth First 
  1. `Enqueque` the declared start node into the Queue. 
  2. Create a loop that will run while the node still has nodes present.  
  3. `Dequeque` the first node from the queue 
  4. If the `Dequeque`'d node has unvisited child nodes, mark the unvisited children as visited and re-insert them back into the queue.
  ```javascript
  /*
  ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    breadth.Enqueque(vertex)

    while(breadth is not empty)
      DECLARE front <-- breadth.Dequeque()
      nodes.Add(front)

      for each child in front.Children
        if (child is not visited) 
          child.visited <-- true
          breadth.Enqueque(child)
    return nodes;
  */
  ```
* Depth First 
  1. `Push` the root node into the stack  
  2. Start a while loop while the stack is not empty  
  3. `Peek` at the top node in the stack  
  4. If the top node has unvisited children, mark the top node as visited, and then `Push` any unvisited children back into the stack 
  5. If the top node does not have any unvisited children, `Pop` that node off the stack  
  6. Repeat until the stack is empty  
  