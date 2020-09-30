# Graphs
A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.



## Undirected Graph

    The undirected graph we are looking at has 6 vertices and 7 undirected edges.

    Vertices/Nodes = {a,b,c,d,e,f}

    Edges = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}

## Directed Graphs (Digraph)
    A Directed Graph also called a Digraph is a graph where every edge is directed.

    Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

    Compare the visual below with the undirected graph above. Can you see the difference? The Digraph has arrows pointing to specific nodes.



## The three different types are completed, connected, and disconnected.

1. Complete Graphs
    A complete graph is when all nodes are connected to all other nodes.



2. Connected
    A connected graph is graph that has all of vertices/nodes have at least one edge.



3. Disconnected
    A disconnected graph is a graph where some vertices may not have edges.





## Traversals
You will be required to traverse through a graph. The traversals itself are like those of trees. Below is a breakdown of how you would traverse a graph.

- Breadth First
    In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. The breadth-first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. When a graph has cycles and we are trying to traverse, this leaves the possibility to be in an infinite loop….this is bad. To prevent such behavior, we need to have some sort of flag that specifies if we have already visited that vertices. Upon each visit, we just set the “visited” flag from false to true.



### ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    breadth.Enqueue(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                child.Visited <-- true
                breadth.Enqueue(child)   

    return nodes;

## In a depth first traversal, we approach it a bit different than the way we do when working with a depth first traversal of a tree. Similar to how the breadth-first uses a queue, we are going to use a Stack for our depth-first traversal.

### The algorithm for a depth first traversal is as follows:

    Push the root node into the stack
    Start a while loop while the stack is not empty
    Peek at the top node in the stack
    If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
    If the top node does not have any unvisited children, Pop that node off the stack
    repeat until the stack is empty.
    Let’s look at the visual for a depth-first traversal.


[For more information(SSH)](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)
