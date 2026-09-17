# Non-Linear Data Structure

## 1. What is Non-Linear Data Structure?

A **Non-Linear Data Structure** stores data in a **hierarchical or interconnected way**, rather than sequentially.

An element can be connected to **multiple other elements**.

### Examples

* **Tree**
* **Graph**
* **Heap**
* **Trie**

## 2. Linear vs Non-Linear

| Linear                           | Non-Linear                                  |
| -------------------------------- | ------------------------------------------- |
| Data arranged sequentially       | Data arranged hierarchically/interconnected |
| One-by-one relationship          | One-to-many or many-to-many                 |
| Array, Linked List, Stack, Queue | Tree, Graph, Heap, Trie                     |

## 3. Tree

A **Tree** is a hierarchical data structure consisting of **nodes and edges**.

```text
        A
       / \
      B   C
     / \
    D   E
```

Examples:

* Binary Tree
* Binary Search Tree (BST)
* AVL Tree
* Heap

## 4. Graph

A **Graph** consists of **vertices (nodes)** and **edges**.

```text
    A ----- B
    |       |
    |       |
    C ----- D
```

Types:

* Directed Graph
* Undirected Graph
* Weighted Graph
* Unweighted Graph

Common algorithms:

* BFS
* DFS
* Dijkstra
* Prim's
* Kruskal's

## 5. Heap

A **Heap** is a **complete binary tree** that follows a heap property.

### Max Heap

```text
        50
       /  \
     30    40
```

Parent ≥ Children

### Min Heap

```text
        10
       /  \
     20    30
```

Parent ≤ Children

## 6. Trie

A **Trie** is a tree-based data structure mainly used for storing and searching **strings/prefixes**.

Example:

```text
       root
      /    \
     c      d
     |
     a
     |
     t
```

## 7. Key Point

> **Non-Linear Data Structure = Data is not arranged sequentially; elements can have hierarchical or multiple relationships.**

### Memory Trick

**Tree → Hierarchy**
**Graph → Connections**
**Heap → Priority**
**Trie → Prefix**
## Tree
<img width="905" height="567" alt="image" src="https://github.com/user-attachments/assets/1dd5032b-56b1-4fa5-b071-dda63c25167f" />
<img width="1011" height="619" alt="image" src="https://github.com/user-attachments/assets/b34a3ab6-d7f6-4616-a005-ac07ff954499" />
<img width="1236" height="339" alt="image" src="https://github.com/user-attachments/assets/726fbefa-0c94-4aea-9823-ea0f03e3881c" />
<img width="1006" height="606" alt="image" src="https://github.com/user-attachments/assets/500bd45d-9c01-4a2b-b1d7-343b0ef86fa0" />
# Tree Data Structure

## 1. What is a Tree?

A **Tree** is a **non-linear data structure** that represents data in a **hierarchical structure** using **nodes and edges**.

Example:

```text
          A          ← Root
        /   \
       B     C
      / \
     D   E
```

## 2. Important Terms

* **Root:** Topmost node → `A`
* **Parent:** Node having children → `B` is parent of `D, E`
* **Child:** Node below a parent → `D` is child of `B`
* **Leaf:** Node with no children → `C, D, E`
* **Sibling:** Nodes having the same parent → `D, E`
* **Edge:** Connection between two nodes
* **Subtree:** A smaller tree inside a tree
* **Depth:** Distance from root to a node
* **Height:** Longest path from a node to a leaf

## 3. Basic Properties

For a tree with `n` nodes:

```text
Number of edges = n - 1
```

A tree is:

* Connected
* Acyclic (no cycle)
* Non-linear

## 4. Types of Trees

### Binary Tree

Each node has **at most 2 children**.

```text
        10
       /  \
      5    15
```

### Binary Search Tree (BST)

```text
Left < Root < Right
```

Example:

```text
        10
       /  \
      5    15
```

### Other Types

* Full Binary Tree
* Complete Binary Tree
* Perfect Binary Tree
* Balanced Tree
* AVL Tree
* Heap
* Trie
* B-Tree

## 5. Tree Traversal

Traversal means **visiting all nodes**.

### DFS Traversals

**Preorder:**

```text
Root → Left → Right
```

**Inorder:**

```text
Left → Root → Right
```

**Postorder:**

```text
Left → Right → Root
```

### BFS Traversal

**Level Order:**

```text
Level by Level
```

Example:

```text
        A
       / \
      B   C
     / \
    D   E
```

```text
Preorder   → A B D E C
Inorder    → D B E A C
Postorder  → D E B C A
Level Order → A B C D E
```

## 6. Complexity

For traversal:

```text
Time  = O(n)
Space = O(h)
```

Where:

* `n` = number of nodes
* `h` = height of tree

## 7. Key Points

> **Tree = Nodes + Edges + Hierarchy**

```text
Root
 ↓
Parent
 ↓
Child
 ↓
Leaf
```

### Memory Trick

**Preorder:** Root → Left → Right
**Inorder:** Left → Root → Right
**Postorder:** Left → Right → Root
**Level Order:** Level by Level






