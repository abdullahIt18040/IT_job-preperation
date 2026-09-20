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

