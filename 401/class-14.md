## Trees

### Common Terminology 
- **Node**: A tree node is a component which may contain its own values and references to other nodes
- **Root**: The root is the node at the beginning of the tree
- **K**: A number that specifies the max number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- **Left**: A reference to one child node in a binary tree.
- **Right**: A reference to the other child node in a binary tree.
- **Edge**: The edge in a tree is the link between parent and child node. 
- **Leaf**: A leaf is a node that does not have any children. 
- **Height**: The height of a tree in the number of edges from the root to the furthest leaf. 

### Sample Tree
<img src ="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG">

### Traversals
- An important aspect of trees is how to traverse them. 
- It allows us to search for a node, print the contents of a tree, and more. 
<img src ="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png">
- Two categories:

- **Depth First**: Going through the depth (height) of the tree is prioritized first. 
- Three methods:
- Pre-order: root >> left >> right
- In-order: left >> root >> right
- Post-order: left >> right >> root 
- Pre-order: A, B, D, E, C, F
- In-order: D, B, E, A, F, C
- Post-order: D, E, B, F, C, A
- The most common way to traverse through a tree is to use recursion. With these traversals, we rely on a call stack to navigate back up the tree when the end of a sub-path is reached. 
- **Breadth First**: Iterates through the tree by going through each level of the tree node-by-node. 
- Output: A, B, C, D, E, F

### Binary Tree vs K-ary Trees
- **Binary Trees** restrict the number of children to two (hence left and right children).
- There is no specific sorting order for a binary tree. Nodes can be added wherever space allows. 
- **K-ary Trees** allow nodes to have more than two children. 
- K is used to refer to the max number of children that each Node is able to have. 
- Breadth First Traversal requires a similar approach in K-ary. 
- Nodes are still being pushed into a queue, but it moves down a list of children of k length, instead of checking for the presence of left and right child. 
<img src ="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/KaryTree1.png">
- Output: A, B, C, D, E, F, G, H