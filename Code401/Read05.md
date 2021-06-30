# Linked Lists

* linked list a a way to structure data together and it's a linear data-structure.

* linked list is a **sequence** of nodes.

* each node contain **value**, and **reference** to another node.

* The **current** node is the node that we are currntly at and we can use current method to check the current node.

* the **reference** refer to the next node in the list.

![](https://www.geeksforgeeks.org/wp-content/uploads/gq/2013/03/Linkedlist.png)

## Linked list types:

1. **singular list**: is a list where each node contain only **1** reference that refers only to the **next** node.

2. **doubly list:**  is a list where each node contian **2** refrences, one refer to **next** node and other refer to **prevous** node.

3. **circular**: is a linked list where each node contain 2 references, exactly like the doubly, the o**nly difference** is that the last node in the list refer to the first node in the list.

![](https://camo.githubusercontent.com/16663f95c5962d1e1655912b7bd1ac7a263438524eb858d07953b39f5eecc567/68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f3631352f312a694d596d6b5944435372585864777062716d2d656b412e6a706567)

## Traversal

* since in linked list each node refer to next node by using reference(not a counter) it can't be used inside a forEach or for loop. that's why while loop is useful here, because I will be using the reference to move to next node.

* the while run on the reference not value itself, so when I loop over list and value is being null, it will not throw error (because i check for reference) and move to next node.

* Current node and traversing: the current node will allow me to know where exactly i stand in the list, and what is next or prevoius node (depends on type of linked list i am using).

## Add a Node

when it comes to working with linked list, order of operations matter because you don't want to lose the reference.

same goes for adding, when you want to add a new node you should find it's place but before node take it's place it should take the reference from prevoius node so it point to the next node instead of prevoius one do.

example of adding a node : Order here is intended to add new node without losing reference.

```java
ALGORITHM Add(newValue)
// INPUT <-- Value to add
// OUTPUT <-- No output

  newNode <-- NEW Node
  newNode.Value <-- newValue
  newNode.Next <-- Head
  Head <-- newNode
  ```

find and print a node

```java
ALGORITHM Print()
// INPUT <-- None
// OUTPUT <-- string to console

  Current <-- Head

  WHILE Current is not equal to NULL
    OUTPUT <-- "{Current.Value} --> "
    Current <-- Current.Next

  OUTPUT <-- "NULL"
  ```

