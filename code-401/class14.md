# **Trees:**

- Common Terminology:(1)
  - Node - A Tree node is a component which may contain it’s own values, and references to other nodes
  - Root - The root is the node at the beginning of the tree
  - K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
  - Left - A reference to one child node, in a binary tree
  - Right - A reference to the other child node, in a binary tree
  - Edge - The edge in a tree is the link between a parent and child node
  - Leaf - A leaf is a node that does not have any children
  - Height - The height of a tree is the number of edges from the root to the furthest leaf

![tree](./img/BinaryTree1.png)

- Traversing a tree allows to search for a node, print out the contents of a tree. There are two categories of traversals:

  - Depth First: Depth first traversal is where we prioritize going through the depth (height) of the tree first, it have 3 methods:

    - Pre-order: root >> left >> right
    - In-order: left >> root >> right
    - Post-order: left >> right >> root

  - Breadth First: Breadth first traversal iterates through the tree by going through each level of the tree node-by-node

- | BINARY TREE                                                                                                                                       | BINARY SEARCH TREE                                                                                                                                 |
  | ------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
  | BINARY TREE is a non linear data structure where each node can have atmost two child nodes                                                        | BINARY SEARCH TREE is a node based binary tree which further has right and left subtree that too are binary search tree.                           |
  | BINARY TREE is unordered hence slower in process of insertion, deletion, and searching. Insertion, deletion, searching of an element is faster in | BINARY SEARCH TREE than BINARY TREE due to the ordered characteristics                                                                             |
  | IN BINARY TREE there is no ordering in terms of how the nodes are arranged                                                                        | IN BINARY SEARCH TREE the left subtree has elements less than the nodes element and the right subtree has elements greater than the nodes element. |

## Sources:

- (1) [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

[Back to home page](../README.md)
