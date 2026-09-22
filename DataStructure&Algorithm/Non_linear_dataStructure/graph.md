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
### Type of graph 
<img width="843" height="420" alt="image" src="https://github.com/user-attachments/assets/6cc3cec4-a454-48a2-acdc-2cd201d444f1" />
<img width="857" height="498" alt="image" src="https://github.com/user-attachments/assets/8bb2ce75-fe6a-469f-bec1-4ff93877535e" />
# Basic Types of Graphs

These are the important graph types to know for **IT Job / Computer Science exams**.

---

## 1. Null Graph

A **Null Graph** is a graph that has **vertices but no edges**.

### Example

```text
   1       2       3       4
   ●       ●       ●       ●
```

There is no connection between any vertices.

```text
V = {1, 2, 3, 4}
E = ∅
```

Therefore:

```text
Number of Edges = 0
```

### Key Point

```text
Null Graph
    ↓
Vertices exist
    ↓
No Edges
```

> **Exam Note:** The term *null graph* is used differently in some textbooks. Some define it as a graph with no vertices and no edges, while others use it for an edgeless graph. Follow your syllabus/textbook definition.

---

# 2. Trivial Graph

A **Trivial Graph** contains **exactly one vertex and no edge**.

### Example

```text
      ●
      1
```

Therefore:

```text
V = {1}
E = ∅
```

### Key Point

```text
Trivial Graph
      ↓
Exactly 1 Vertex
      +
0 Edges
```

### Null Graph vs Trivial Graph

| Graph         |              Vertices | Edges |
| ------------- | --------------------: | ----: |
| Null Graph    | Depends on definition |     0 |
| Trivial Graph |         **Exactly 1** | **0** |

---

# 3. Undirected Graph

In an **Undirected Graph**, edges have **no direction**.

### Example

```text
1 -------- 2
```

The connection can be represented as:

```text
{1, 2}
```

The relationship between `1` and `2` is mutual.

### Real-Life Example

Friendship:

```text
Person A -------- Person B
```

If A and B are connected by a friendship edge, the edge does not have a direction.

### Key Point

```text
Undirected Graph
       ↓
Edges have NO direction
```

---

# 4. Directed Graph

A **Directed Graph**, also called a **Digraph**, has edges with a **specific direction**.

### Example

```text
1 --------> 2
```

This represents:

```text
1 → 2
```

It does **not necessarily** mean:

```text
2 → 1
```

A directed edge is commonly represented as:

```text
(1, 2)
```

### Real-Life Example

Following relationship:

```text
A --------> B
```

A follows B, but B does not necessarily follow A.

### Key Point

```text
Directed Graph
       ↓
Edges have direction
```

---

# 5. Connected Graph

An **Undirected Graph** is called **Connected** if there is a **path between every pair of vertices**.

### Example

```text
1 -------- 2
            |
            |
            3 -------- 4
```

We can travel from every vertex to every other vertex.

For example:

```text
1 → 2 → 3 → 4
```

Therefore, the graph is connected.

### Key Point

```text
Connected Graph
       ↓
There is a path between
every pair of vertices
```

---

# 6. Disconnected Graph

A graph is **Disconnected** if there is **at least one pair of vertices for which no path exists between them**.

### Example

```text
1 -------- 2


3 -------- 4
```

There is no path between:

```text
{1, 2}
```

and:

```text
{3, 4}
```

Therefore, this is a **Disconnected Graph**.

### Connected Components

The graph has **2 connected components**:

```text
Component 1 = {1, 2}

Component 2 = {3, 4}
```

### Key Point

```text
Disconnected Graph
        ↓
Graph contains multiple
connected components
```

---

# 7. Regular Graph

A graph is called a **Regular Graph** if **every vertex has the same degree**.

### Example

```text
       1
      / \
     /   \
    2-----3
```

Degree of every vertex:

```text
Degree(1) = 2
Degree(2) = 2
Degree(3) = 2
```

Therefore, this is a:

```text
2-Regular Graph
```

### Another Example

If every vertex has degree `3`:

```text
Degree of every vertex = 3
```

Then the graph is called a:

```text
3-Regular Graph
```

### General Rule

If every vertex has degree `k`:

```text
Graph = k-Regular Graph
```

### Key Point

```text
Regular Graph
      ↓
Every vertex has
the same degree
```

---

# 8. Complete Graph

A **Complete Graph** is a graph in which **every pair of distinct vertices is directly connected by an edge**.

A complete graph with `n` vertices is represented by:

```text
Kₙ
```

where:

```text
n = Number of vertices
```

---

## Example: K₃

```text
      1
     / \
    /   \
   2-----3
```

Every pair of vertices is directly connected:

```text
1 — 2
1 — 3
2 — 3
```

Therefore, this is:

```text
K₃
```

---

## Complete Graph K₄

```text
       1
      /|\
     / | \
    2--|--3
     \ | /
      \|/
       4
```

Every pair of vertices is connected.

### Number of Edges

For a complete graph with `n` vertices:

```text
E = n(n - 1) / 2
```

For `K₄`:

```text
E = 4(4 - 1) / 2
  = 4 × 3 / 2
  = 6
```

Therefore:

```text
K₄
↓
4 vertices
6 edges
```

### Degree of Each Vertex

In `Kₙ`, every vertex is connected to the other `n - 1` vertices.

Therefore:

```text
Degree = n - 1
```

For `K₄`:

```text
Degree = 4 - 1
       = 3
```

---

# Regular Graph vs Complete Graph

This is an **important exam concept**.

| Feature               | Regular Graph         | Complete Graph        |
| --------------------- | --------------------- | --------------------- |
| Degree                | Same for every vertex | Same for every vertex |
| Every pair connected? | Not necessarily       | **Yes**               |
| Degree                | Can be `k`            | Always `n - 1`        |
| Example               | Cycle Graph           | `K₃`, `K₄`, `K₅`      |

### Important Relationship

```text
Every Complete Graph
        ↓
   is Regular
```

But:

```text
Every Regular Graph
        ↓
is NOT necessarily Complete
```

### Example

A cycle graph:

```text
1 -------- 2
|          |
|          |
4 -------- 3
```

Every vertex has degree `2`:

```text
Degree(1) = 2
Degree(2) = 2
Degree(3) = 2
Degree(4) = 2
```

Therefore:

```text
It is 2-Regular
```

But vertices `1` and `3` are not directly connected.

Therefore:

```text
2-Regular ≠ necessarily Complete
```

---

# 9. Bipartite Graph

A **Bipartite Graph** is a graph whose vertices can be divided into **two disjoint sets** such that no edge connects two vertices within the same set.

Suppose:

```text
Set A = {1, 2}

Set B = {3, 4}
```

Edges can exist between the sets:

```text
1 -------- 3
|          |
|          |
2 -------- 4
```

But there should be no edge:

```text
1 -------- 2
```

and no edge:

```text
3 -------- 4
```

### Key Point

```text
Bipartite Graph
       ↓
Vertices can be divided
into 2 sets
       ↓
No edge within the
same set
```

---

## Bipartite and Odd Cycle

A very important theorem:

> **A graph is bipartite if and only if it contains no odd cycle.**

In simple terms:

```text
No Odd Cycle
     ↓
Bipartite
```

and:

```text
Odd Cycle Exists
     ↓
Not Bipartite
```

### Example

A triangle:

```text
      1
     / \
    /   \
   2-----3
```

It contains a cycle of length `3`.

Since `3` is odd:

```text
Odd Cycle
   ↓
Not Bipartite
```

---

# Quick Revision

```text
Null Graph
→ Vertices but no edges
→ Definition may vary by textbook

Trivial Graph
→ Exactly 1 vertex and 0 edges

Undirected Graph
→ Edges have no direction

Directed Graph
→ Edges have direction

Connected Graph
→ There is a path between every pair of vertices

Disconnected Graph
→ At least one pair of vertices has no path between them

Regular Graph
→ Every vertex has the same degree

Complete Graph
→ Every pair of distinct vertices is directly connected

Bipartite Graph
→ Vertices can be divided into 2 sets
→ No edge within the same set
→ Contains no odd cycle
```

---

# ⭐ Must Remember for MCQ

## Complete Graph

```text
Kₙ
 ↓
n vertices
 ↓
Every pair of vertices connected
 ↓
Degree of each vertex = n - 1
 ↓
Number of edges = n(n - 1) / 2
```

## Regular Graph

```text
Regular Graph
      ↓
All vertices have
the same degree
```

## Bipartite Graph

```text
Bipartite Graph
      ↓
2 sets
      ↓
No edge within the same set
      ↓
No odd cycle
```

## Complete Graph Relationship

```text
Complete Graph
      ↓
Regular Graph
```

But:

```text
Regular Graph
      ↓
NOT necessarily
Complete Graph
```

---

# 🎯 Exam Shortcut

| Type               | Remember                  |
| ------------------ | ------------------------- |
| **Null**           | No edges                  |
| **Trivial**        | 1 vertex + 0 edges        |
| **Undirected**     | No edge direction         |
| **Directed**       | Edge has direction        |
| **Connected**      | Path between every pair   |
| **Disconnected**   | Separate components       |
| **Regular**        | Same degree               |
| **Complete**       | Every pair connected      |
| **Bipartite**      | 2 sets + no same-set edge |
| **Bipartite Test** | No odd cycle              |




