# Trees

* Trees consist of a few common terminologies
    * Node - A node is the individual item/data that makes up the data structure
    * Root - The root is the first/top Node in the tree
    * Left Child - The node that is positioned to the left of a root or node
    * Right Child - The node that is positioned to the right of a root or node
    * Edge - The edge in a tree is the link between a parent and child node
    * Leaf - A leaf is a node that does not contain any children
    * Height - The height of a tree is determined by the number of edges from the root to the bottommost node

* Traversing a list allows us to search for a node, print the contents, and more. This is done using two types of traversals.
    * Depth First - Prioritizing going through the depth (height) first. The most common way to do this is with *recursion*.
    * Breadth First - Iterates through the tree by going through each level of the tree node-by-node.

* Binary trees restrict the number of children a node can have to *two*.
* Because there are no structural rules for where nodes are “supposed to go” in a binary tree, it really doesn’t matter where a new node gets placed.
* In `Binary Search Trees` the nodes are organized where all values smaller than the `root` are placed to the left, and all values larger to the right.
