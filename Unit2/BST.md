# Binary Search Tree
## Exploration
Please use the [visualizer](https://www.cs.usfca.edu/~galles/visualization/BST.html) to figure out pseudocode 
explanations of the following properties of a binary search tree:

1. What is the instance data of a Binary Search Tree node?
2. How does insert work if there's just one node? If there are more nodes already attached to the root?
3. How does remove work if there's just one node? If the node to remove is a leaf? If the node to remove is a branch?
4. How does search work?
5. How does print work?

## Tasks:
* Build BSTNode class with appropriate getters, setters and a toString that prints its data.

```java
public class Node<Key extends Comparable<Key>, Value> {
private int size;
//other instance data here
//methods- getters, setters, toString
```

* Create a zero input and one input constructor for a binary search tree
```java
public class BinarySearchTree<Key extends Comparable<Key>, Value> {
//just make the instance data and constructors for now.
}
```
