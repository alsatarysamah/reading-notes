# Big-O
It describe the  Worst Case efficiency of an algorithm or function.

there is 2 factor :

1-Running Time (also known as time efficiency / complexity)
The amount of time a function needs to complete.

2-Memory Space (also known as space efficiency / complexity)
The amount of memory resources a function uses to store data and instructions.

**Input Size**

We will use the letter n to refer to the Input Size value.

**Units of Measurement**

 *Running Time*
 
1-milliseconds

2-operations

3-Basic Operations

 *Memory Space*

 1-The amount of space needed to hold the code for the algorithm

 2-The amount of space needed to hold the input data

 3-The amount of space needed for the output data.

 4-The amount of space needed to hold working space during the calculation

 *Big Omega: The best case analysis of algorithm efficiency.

*Big Theta: The typical or random case used for analysis of algorithm efficiency.

[basic-asympotatic-efficiency-of-code](./sqlScreenShoot/Screenshot%20(134).png)

# Linked Lists

A Linked List is a sequence of Nodes that are connected/linked to each other

Linked List - A data structure that contains nodes that links/points to the next node in the list.

Singly - Singly refers to the number of references the node has.

Doubly - Doubly refers to there being two (double) references within the node. 

Node - Nodes are the individual items/links that live in a linked list. 

Head - The Head is a reference of type Node to the first node in a linked list.

Current - The Current is a reference of type Node to the node that is currently being looked at. 

**Traversal Example**

  WHILE Current is not NULL

    IF Current.Value is equal to value

      return TRUE

    Current <-- Current.Next

    return FALSE

 **Traversal Big O**

 The Big O of time for Includes would be O(n)

The Big O of space for Includes would be O(1). 

**Add node example**

    newNode <-- NEW Node

     newNode.Value <-- newValue

    newNode.Next <-- Head
    
         Head <-- newNode

**Deferencies between array and link list**

1-array need to take up a single block of memory; link list, the memory that they use can be scattered throughout.

2-array is static data structure but link-list is dynamic data structures

(shrink and grow in memory)

**Parts of a linked list**

1-head.  all linked lists must have a head, because this is effectively the only entry point to the list and all of its elements

**add node to the beginning of link-list**

First, we find the head node of the linked list.

Next, we’ll make our new node, and set its pointer to the current first node of the list.

Lastly, we rearrange our head node’s pointer to point at our new node.

O(1)

**add node to the end  of link-list**

Find the node we want to change the pointer of (in this case, the last node)

Create the new node we want to insert and set its pointer (in this case, to null)

Direct the preceding node’s pointer to our new node

O(n)