
# Linked Lists
Definition:
A Linked List is a sequence of Nodes that are connected/linked to each other.

## There are two types of Linked List - **Singly** and **Doubly**


Terminology (definitions):

1. Linked List - A data structure that contains nodes that links/points to the next node in the list.
2. Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
3. Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
4. Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
5. Next - Each node contains a property called Next. This property contains the reference to the next node.
6. Head - The Head is a reference type of type Node to the first node in a linked list.
7. Current - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

## Print Out Nodes
its semilar to Find() method.

The pseudo code for a method to print out all the nodes in a linked list:
```
		ALGORITHM Print()
		// INPUT <-- None
		// OUTPUT <-- string to console

			Current <-- Head

			while Current.Next is not equal to NULL
				OUTPUT <-- "Current.Value --> "
				Current <-- Current.Next

			OUTPUT <-- "Current.Value --> NULL"
```


## Prerequisites

When constructing your code, a few things to keep in mind.

1. When making your *Node* class, consider requiring a value to be passed in **to require that each node has a value.**

2. When making a **Linked List**, you may want to **require** that at **least one node** gets passed in upon instantiation. This first node is what your Head and Current will point too.