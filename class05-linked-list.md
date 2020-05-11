# Reading 5 - Linked Lists - 4/17/2020

## Linked Lists
* A sequence of "linked" nodes
* Each node in the linked list references the following in sequence
* Singly lists just know their next item
* Doubly lists know next and previous
* Circularly linked lists has a later node reference an earlier node in a loop
* Terminology:
  * Singly - node with only reference to next node
  * Doubly - each node has reference to previous and next node
  * Node - individual item, has the data for each link
  * Next - each node has this property, default value for this property is null
  * Head - reference to first node in a linked list
  * Current - reference to the current node looked at 

## Linked Lists VS Arrays
* Linked Lists
  * Linear data structure
  * Can retrieve just the current node and its information, they do not need to be contiguous either
  * When traversing, cannot use `foreach` or `for` like arrays, you need to use `next`
  * Use a `while()` for traversal, `current` for where you are in a list
  * Time complexity of adding a node at the head is always constant - O(1)
  * Time complexity of adding a node to the end of the list is linear - O(n) 
  * Time complexity of `includes` method is linear - O(n)
  * Space complexity of `includes` method is constant - O(1)
* Arrays
  * Linear data structure
  * When using the data, need store entire object in the memory