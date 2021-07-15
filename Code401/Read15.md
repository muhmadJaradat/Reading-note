# Tree 

A tree is a non linier data structure that is like a list but that uses nodes starting at a root then then point to more than one "next" node.

* Terminology:

  * Tree Node: a node contain value, and two references: right and left.

  * Root: the first node in the tree.

  * left : a reference hold a node as value in the node.

  * right: a reference hold a node as value in the node.

  * edge : a connection between parent node and child node.

  * leaf node: a node has no children.

  * tree height: the total number of edges between root and the deepest leaf.

  * K - A : number specify the max number of children that node can have.

  * Tree Example:
  ![TREE EXAMPLE](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG) 

## Traversals 

If we want to deal with trees we need to know how we can Traversals, and there is two categories of traversals which is Depth First and Breadth First.

* There are two ways of traversing tree.

  * Depth First.

  * breadth First.

### Depth First

   * Depth first visit tree nodes from root to the down end of tree node by node.

   * It uses Stack.

   * There are 3 methods to iterate using depth:

     * pre order depth.

     * in order depth.

     * post order depth.

#### Pre Order

* pre order where traversing start from root and accessing each element on the left first then do something to the left leaf.

* it uses recursion.

* Mechanism:

      1. first method `preOrder(root)` called and passed root to it.

      2. add the root value to stack.

      3. check if it's left node not null then call method again.

      4. if null check it's right node if it's not null call method again.

      5. if both right and left are null it will `pop()` root from stack and check for higher level node than root.

      6. if no higher node it will stop calling the `preOrder(root)`.

      7.  **it will apply this pattern on all nodes in the tree**
