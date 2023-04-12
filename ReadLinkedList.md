# Linked List
## What is Linked List?

A linked list is a data structure that consists of a sequence of elements called nodes, each containing two parts: a data part and a reference part, which points to the next node in the sequence. The reference part of the last node in the sequence points to null, indicating the end of the list.

Unlike arrays, linked lists do not require a fixed amount of memory to store their elements. They can dynamically grow and shrink as elements are added or removed, making them a flexible data structure for certain types of operations.

Linked lists can be singly linked, where each node points only to the next node, or doubly linked, where each node points to both the next and previous nodes in the sequence. Doubly linked lists are often used for operations that require traversal in both directions, such as in implementing a text editor.

## What is Singly?
Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list. 

## What is Doubly?
Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous

## What is node?
Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

## What is Next?
Next - Each node contains a property called Next. This property contains the reference to the next node.

## What is Head?
Head - The Head is a reference of type Node to the first node in a linked list.

## What is Current?

Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list