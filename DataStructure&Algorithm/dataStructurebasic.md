# Data Structure

## What is Data Structure?

A **Data Structure** is a way of **organizing, storing, and managing data** in a computer so that we can use the data efficiently.

In simple words:

> **Data Structure = A way to store and organize data so that operations like access, search, insertion, deletion, and update can be performed efficiently.**

### Example

Suppose we have student marks:

```text
80, 75, 90, 65, 88
```

We can store them in an Array:

```java
int[] marks = {80, 75, 90, 65, 88};
```

Now we can easily access:

```java
marks[2]
```

Result:

```text
90
```

So, **Array is a Data Structure**.

---

# Types of Data Structure

Data Structures are mainly divided into two types:

```text
                         Data Structure
                              │
                ┌─────────────┴─────────────┐
                │                           │
             Linear                    Non-Linear
          Data Structure             Data Structure
                │                           │
       ┌────────┼────────┐           ┌──────┴──────┐
       │        │        │           │             │
     Array    Stack    Queue        Tree          Graph
       │
  Linked List
```

---

# 1. Linear Data Structure

In a **Linear Data Structure**, data elements are arranged **sequentially, one after another**.

Example:

```text
10 → 20 → 30 → 40 → 50
```

The elements follow a linear sequence.

### Main Linear Data Structures

* Array
* Linked List
* Stack
* Queue

---

## A. Array

An **Array** stores multiple elements of the same type and provides access using an **index**.

Example:

```text
Index:  0    1    2    3
       ┌────┬────┬────┬────┐
Data:  │ 10 │ 20 │ 30 │ 40 │
       └────┴────┴────┴────┘
```

Java:

```java
int[] arr = {10, 20, 30, 40};
```

Access:

```java
arr[2]
```

Result:

```text
30
```

**Access Time Complexity:** `O(1)`

---

## B. Linked List

A **Linked List** consists of nodes where each node contains data and a reference to another node.

```text
10 → 20 → 30 → 40 → null
```

Example:

```java
class Node {
    int data;
    Node next;
}
```

**Access Time Complexity:** `O(n)`

---

## C. Stack

A **Stack** follows:

> **LIFO — Last In, First Out**

Example:

```text
        30 ← Top
        20
        10
```

If we call `pop()`, `30` will be removed first.

### Common Operations

```text
push() → Add element
pop()  → Remove top element
peek() → View top element
```

### Real-World Examples

* Undo/Redo
* Browser history
* Function call stack
* Recursion
* DFS

---

## D. Queue

A **Queue** follows:

> **FIFO — First In, First Out**

Example:

```text
Front                    Rear
  ↓                        ↓
10 → 20 → 30 → 40
```

If we remove an element, `10` will be removed first.

### Common Operations

```text
enqueue() → Add element
dequeue() → Remove element
peek()    → View front element
```

### Real-World Examples

* Printer queue
* CPU scheduling
* Message processing
* Producer-Consumer
* BFS

---

# 2. Non-Linear Data Structure

In a **Non-Linear Data Structure**, elements are not arranged sequentially.

They can represent:

* **Hierarchical relationships**
* **Network relationships**

Main examples:

* Tree
* Graph

---

# A. Tree

A **Tree** represents hierarchical data.

Example:

```text
              10
            /    \
           5      20
         /  \    /  \
        2    7  15   30
```

Here:

```text
10       → Root
5, 20    → Child Nodes
2, 7, 15, 30 → Leaf Nodes
```

### Types of Trees

* Binary Tree
* Binary Search Tree (BST)
* AVL Tree
* Red-Black Tree
* B-Tree
* Trie

### Real-World Examples

* File systems
* Database indexes
* HTML DOM
* Organization hierarchy

---

# B. Graph

A **Graph** represents (network relationship) relationships or connections between entities.

Example:

```text
       A
      / \
     B---C
      \ /
       D
```

Here:

```text
A, B, C, D → Vertices / Nodes
Connections → Edges
```

### Real-World Examples

```text
Google Maps      → City = Node, Road = Edge
Social Network   → Person = Node, Friendship = Edge
Computer Network → Computer = Node, Connection = Edge
Airline Network  → Airport = Node, Flight Route = Edge
```

### Important Graph Algorithms

* BFS
* DFS
* Dijkstra
* Bellman-Ford
* Floyd-Warshall
* Prim
* Kruskal

---

# 3. Static vs Dynamic Data Structure

Data Structures can also be classified based on whether their size can change.

## Static Data Structure

The size is generally fixed after creation.

### Example

```java
int[] arr = new int[10];
```

The array has a fixed size of `10`.

**Example:**

```text
Array
```

---

## Dynamic Data Structure

The size can grow or shrink during program execution.

### Examples

* Linked List
* Stack
* Queue
* Tree
* Graph

### Java Examples

```text
ArrayList
LinkedList
HashMap
HashSet
PriorityQueue
```

> Note: Java's `ArrayList` is a dynamic array implementation, while `HashMap`/`HashSet` are hash-based structures rather than simply "dynamic versions" of an array.

---

# 4. Important Java Data Structures

| Data Structure | Java Implementation   |
| -------------- | --------------------- |
| Array          | `int[]`, `String[]`   |
| Dynamic Array  | `ArrayList`           |
| Linked List    | `LinkedList`          |
| Stack          | `Deque`, `Stack`      |
| Queue          | `Queue`, `ArrayDeque` |
| Hash Table     | `HashMap`             |
| Set            | `HashSet`             |
| Sorted Set     | `TreeSet`             |
| Priority Queue | `PriorityQueue`       |

---

# 5. Complete Picture

```text
                         DATA STRUCTURE
                              │
             ┌────────────────┴────────────────┐
             │                                 │
          LINEAR                           NON-LINEAR
             │                                 │
     ┌───────┼────────┐                 ┌──────┴──────┐
     │       │        │                 │             │
   Array   Stack    Queue              Tree         Graph
     │
 Linked List
```

### Based on Size

```text
Data Structure
│
├── Static
│   └── Array
│
└── Dynamic
    ├── Linked List
    ├── Stack
    ├── Queue
    ├── Tree
    └── Graph
```

---

# ⭐ Interview Definition

> **A Data Structure is a systematic way of organizing and storing data in memory so that data can be accessed and modified efficiently.**

## Quick Memory

```text
Linear
→ Array
→ Linked List
→ Stack
→ Queue

Non-Linear
→ Tree
→ Graph

Static
→ Array

Dynamic
→ Linked List
→ Stack
→ Queue
→ Tree
→ Graph
```

## Key Idea

```text
Data Structure
     ↓
Organize Data
     ↓
Efficient Operations
     ↓
Access | Search | Insert | Delete | Update
```
