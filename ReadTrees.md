# Trees in Data Structures
## What is a Tree?
A tree is a data structure that consists of nodes in a parent/child relationship.
## Common Terminology
- Node - A node is the individual item/data that makes up the data structure
- Root - The root is the first/top Node in the tree
- Left Child - The node that is positioned to the left of a root or node
- Right Child - The node that is positioned to the right of a root or node
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not contain any children
- Height - The height of a tree is determined by the number of edges from the root to the bottommost node
## Traversals
- An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more!
- There are two categories of traversals when it comes to trees:
- Depth First
- Breadth First

## Depth First
- Depth first traversal is where we prioritize going through the depth (height) of the tree first.
- There are three methods for depth first traversal:
- Pre-order: root >> left >> right
- In-order: left >> root >> right
- Post-order: left >> right >> root
- Pre-order
- Pre-order means that the root has to be looked at first. In our case, looking at the root just means that we output its value.
- Here is the pseudocode for a pre-order traversal:
- ALGORITHM preOrder(root)
- // INPUT <-- root node
- // OUTPUT <-- pre-order output of tree node's values
- OUTPUT <-- root.value
- if root.left is not NULL
- preOrder(root.left)
- if root.right is not NULL
- preOrder(root.right)
- In-order
- In-order means that the root isn't looked at until after the left subtree and right subtree have been looked at. So the left subtree will be traversed first, then the root, and finally the right subtree.
- Here is the pseudocode for an in-order traversal:
- ALGORITHM inOrder(root)
- // INPUT <-- root node

- // OUTPUT <-- in-order output of tree node's values
- if root.left is not NULL
- inOrder(root.left)
- OUTPUT <-- root.value
- if root.right is not NULL
- inOrder(root.right)
- Post-order
- Post-order means that the root isn't looked at until after both subtrees have been looked at. So the left subtree will be traversed first, then the right subtree and finally the root.

- Here is the pseudocode for a post-order traversal:
- ALGORITHM postOrder(root)
- // INPUT <-- root node
- // OUTPUT <-- post-order output of tree node's values
- if root.left is not NULL
- postOrder(root.left)

- if root.right is not NULL
- postOrder(root.right)
- OUTPUT <-- root.value
