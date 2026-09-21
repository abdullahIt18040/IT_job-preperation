## Graph 
# Graph — Introduction

## What is a Graph?

A **Graph** is a non-linear data structure used to represent relationships between objects.

A graph consists of:

* **Vertex (Node)** → Represents an object.
* **Edge** → Represents a connection between two vertices.

Example:

```text
    A
   / \
  B---C
   \
    D
```

Here:

```text
Vertices = A, B, C, D
Edges    = (A,B), (A,C), (B,C), (B,D)
```

## Types of Graph

### 1. Undirected Graph

Edges have **no direction**.

```text
A ─── B
```

`A → B` and `B → A` are treated as the same connection.

### 2. Directed Graph

Edges have a **direction**.

```text
A ───→ B
```

`A → B` does not necessarily mean `B → A`.

### 3. Weighted Graph

Edges have a **weight/cost**.

```text
A ──5── B
```

Here, `5` is the edge weight.

### 4. Unweighted Graph

Edges have no weight.

```text
A ─── B
```

## Graph Traversal

Two common graph traversal algorithms are:

```text
DFS → Depth First Search
BFS → Breadth First Search
```

### Easy Remember

```text
Graph
 ├── Vertex / Node
 ├── Edge
 ├── Directed / Undirected
 ├── Weighted / Unweighted
 └── Traversal
      ├── DFS
      └── BFS
```
# Max Heap and Min Heap

## 1. What is a Heap?

A **Heap** is a **Complete Binary Tree** that follows a specific **Heap Property**.

Two types:

* **Max Heap**
* **Min Heap**

---

## 2. Max Heap

In a **Max Heap**:

```text
Parent ≥ Children
```

The **largest element is always at the root**.

Example:

```text
          50
        /    \
      30      40
     /  \    /
    10  20  35
```

```text
50 ≥ 30, 40
30 ≥ 10, 20
40 ≥ 35
```

### Key Point

```text
Maximum element → Root
```

---

## 3. Min Heap

In a **Min Heap**:

```text
Parent ≤ Children
```

The **smallest element is always at the root**.

Example:

```text
          10
        /    \
      20      15
     /  \    /
    30  40  25
```

```text
10 ≤ 20, 15
20 ≤ 30, 40
15 ≤ 25
```

### Key Point

```text
Minimum element → Root
```

---

## 4. Max Heap vs Min Heap

| Feature  | Max Heap          | Min Heap          |
| -------- | ----------------- | ----------------- |
| Root     | Maximum           | Minimum           |
| Property | Parent ≥ Children | Parent ≤ Children |
| Used for | Maximum priority  | Minimum priority  |

---

## 5. Important Properties

A Heap is a **Complete Binary Tree**.

For an array representation using **0-based indexing**:

```text
Parent(i) = (i - 1) / 2
Left(i)   = 2i + 1
Right(i)  = 2i + 2
```

Example:

```text
Array:
[50, 30, 40, 10, 20, 35]
```

represents:

```text
          50
        /    \
      30      40
     /  \    /
    10  20  35
```

---

## 6. Complexity

| Operation   |     Time |
| ----------- | -------: |
| Get Max/Min |     O(1) |
| Insert      | O(log n) |
| Delete Root | O(log n) |
| Build Heap  |     O(n) |
| Search      |     O(n) |

---

## 7. Easy Memory Trick

```text
Max Heap → Maximum → Root
Min Heap → Minimum → Root
```

> **Max Heap:** Parent is greater than or equal to its children.
> **Min Heap:** Parent is less than or equal to its children.

