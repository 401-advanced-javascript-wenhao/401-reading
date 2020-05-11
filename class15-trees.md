# Reading 5 - Trees - 5/10/2020

## Common Terminology
* Node - A node is the individual item/data that makes up the Tree data structure
* Root - First/Top node in the tree
* Left Child - Positioned to the left of a parent node in the Binary Tree
* Right Child - Positioned to the right of a parent node in the Binary Tree
* Edge - Link between a parent and child node
* Leaf - A node that does not have any children
* Height - Number of edges from root to bottom

## Traversals for Binary Tree
1. Depth First 
  * Pre-order: `root -> left -> right`
  ```javascript
  psuedo
  ALGORITHM preOrder(root)
  // INPUT <-- root node
  // OUTPUT <-- pre-order output of tree nodes

    OUTPUT <-- root.value
    
    if root.left is not NULL
        preOrder(root.left)

    if root.right is not NULL
        preOrder(root.right)
  ```

  * In-order: `left -> root -> right`
  ```javascript
  ALGORITHM inOrder(node)
  // INPUT <-- root node
  // OUTPUT <-- in-order output of tree nodes

      if node.left is not NULL
          inOrder(node.left)

      OUTPUT <-- node.value

      if node.right is not NULL
          inOrder(node.right)
  ```

  * Post-order: `left -> right -> root`
  ```javascript
  ALGORITHM postOrder(node)
  // INPUT <-- root node
  // OUTPUT <-- post-order output of tree nodes

      if node.left is not NULL
          inOrder(node.left)

      if node.right is not NULL
          inOrder(node.right)

      OUTPUT <-- node.value
  ```

2. Breadth First  
Iterates through the tree by going through each level of the tree from left to right. Using Queue to track which node is going and coming next. When dequeques front node, enqueque that node's left and right node if exists.
```javascript
ALGORITHM breadthFirst(root)
// INPUT  <-- root node
// OUTPUT <-- front node of queue to console

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while breadth.peek()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)
```

## Binary Trees 
Each node in the Binary Tree has at most 2 children nodes (left node and right node)

### Binary Search Trees (BST)
* It is a sorted Binary Tree, all nodes that have values that less than root node's value will be placed on the left side of the root node. Otherwise, will be placed on the right side of the root node
* Searching is best done with a while loop, cycling until we hit a leaf or match we are looking for
* Time complexity is O(height). In a balanced tree, it is O(log(n)) and in a worst case, it is O(n)
* Space complexity is O(1)


