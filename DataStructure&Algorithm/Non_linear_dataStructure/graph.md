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

# More Important Types of Graphs

This note covers:

* Cycle Graph
* Cyclic Graph
* Directed Acyclic Graph (DAG)
* Bipartite Graph
* Simple Graph

These are important for **DSA, Computer Science, and IT Job exams**.

---

# 1. Cycle Graph

A **Cycle Graph** is a graph in which the vertices form **one single cycle**.

It is commonly represented as:

```text
Cₙ
```

where `n` is the number of vertices.

## Example: C₃

```text
      1
     / \
    /   \
   2-----3
```

The cycle is:

```text
1 → 2 → 3 → 1
```

Therefore, this is:

```text
C₃
```

---

## Example: C₄

```text
1 -------- 2
|          |
|          |
4 -------- 3
```

Cycle:

```text
1 → 2 → 3 → 4 → 1
```

Therefore:

```text
C₄
```

### Properties of Cycle Graph

For `Cₙ`:

```text
Number of vertices = n
Number of edges    = n
Degree of every vertex = 2
```

Therefore:

```text
Cₙ is always 2-Regular
```

### Key Point

```text
Cycle Graph
     ↓
One single cycle
     ↓
Every vertex has degree 2
```

---

# 2. Cyclic Graph

A **Cyclic Graph** is a graph that contains **at least one cycle**.

It does not have to be only one cycle.

## Example

```text
      1
     / \
    /   \
   2-----3
   |
   |
   4
```

There is a cycle:

```text
1 → 2 → 3 → 1
```

Therefore, the graph is **Cyclic**.

It can also contain additional vertices or edges outside the cycle.

---

## Cycle Graph vs Cyclic Graph

This is an important distinction.

| Feature                | Cycle Graph                      | Cyclic Graph                      |
| ---------------------- | -------------------------------- | --------------------------------- |
| Meaning                | The graph itself forms one cycle | Graph contains at least one cycle |
| Extra edges/vertices   | No                               | May exist                         |
| Example                | `C₃`, `C₄`, `C₅`                 | Any graph containing a cycle      |
| Degree of every vertex | Exactly 2                        | Not necessarily 2                 |

### Easy way to remember

```text
Cycle Graph
→ The graph IS a cycle

Cyclic Graph
→ The graph CONTAINS a cycle
```

---

# 3. Directed Acyclic Graph (DAG)

**DAG** stands for:

```text
Directed Acyclic Graph
```

A DAG is a **directed graph that contains no directed cycle**.

In other words:

```text
Directed Graph
      +
No Cycle
      ↓
DAG
```

## Example

```text
1 --------> 2
             |
             ↓
             3 --------> 4
```

There is a direction on every edge.

But there is **no way to start from a vertex and follow directed edges to return to that same vertex**.

Therefore, it is a:

```text
DAG
```

---

## Example of NOT a DAG

```text
1 --------> 2
↑           |
|           ↓
4 <---------3
```

There is a directed cycle:

```text
1 → 2 → 3 → 4 → 1
```

Therefore:

```text
Not a DAG
```

### Important Properties of DAG

```text
DAG
 ↓
Directed
 +
Acyclic
 ↓
No Directed Cycle
```

### Applications of DAG

DAGs are commonly used to represent:

* Task dependencies
* Build systems
* Course prerequisites
* Workflow dependencies
* Version-control relationships
* Dependency graphs

### Important Exam Point

Every DAG has at least one **topological ordering**.

Topological sorting is possible for:

```text
DAG
```

but not for a directed graph containing a cycle.

---

# 4. Bipartite Graph

A **Bipartite Graph** is a graph whose vertices can be divided into **two disjoint sets** such that there is **no edge between vertices belonging to the same set**.

Suppose:

```text
Set A = {1, 2}

Set B = {3, 4}
```

Example:

```text
Set A          Set B

  1 ---------- 3
   \            |
    \           |
     \          |
      2 ------- 4
```

Edges can exist between the two sets.

But there should be no edge like:

```text
1 -------- 2
```

because both `1` and `2` belong to the same set.

Similarly:

```text
3 -------- 4
```

is not allowed.

### Key Point

```text
Bipartite Graph
      ↓
Divide vertices into 2 sets
      ↓
No edge within the same set
```

---

# Bipartite Graph and Odd Cycle

This is a **very important MCQ theorem**:

> A graph is bipartite **if and only if** it contains no odd cycle.

Therefore:

```text
No Odd Cycle
     ↓
Bipartite
```

And:

```text
Odd Cycle Exists
     ↓
Not Bipartite
```

## Example

Triangle:

```text
      1
     / \
    /   \
   2-----3
```

The cycle length is:

```text
3
```

Since `3` is odd:

```text
Odd Cycle
    ↓
Not Bipartite
```

---

# 5. Simple Graph

A **Simple Graph** is an **undirected graph** that has:

1. **No self-loops**
2. **No multiple/parallel edges** between the same pair of vertices.

---

## 5.1 No Self-Loop

A self-loop is an edge from a vertex back to itself.

Example:

```text
    ↺
    1
```

This is:

```text
Not a Simple Graph
```

because vertex `1` has a self-loop.

---

## 5.2 No Parallel Edges

Suppose two vertices have multiple edges between them:

```text
1 ======= 2
```

For example:

```text
1 -------- 2
 \--------/
```

This is a **multigraph**, not a simple graph.

A simple graph allows only **one edge** between two vertices.

---

## Example of a Simple Graph

```text
      1
     / \
    /   \
   2-----3
```

There are:

```text
No self-loops
No parallel edges
```

Therefore, it is a:

```text
Simple Graph
```

---

# Simple Graph: Important Formula

For a simple undirected graph with `n` vertices, the maximum possible number of edges is:

```text
Emax = n(n - 1) / 2
```

Why?

Each vertex can connect to:

```text
n - 1
```

other vertices.

But counting every edge twice gives:

```text
n(n - 1) / 2
```

---

## Example

For `n = 4`:

```text
Emax = 4(4 - 1) / 2
     = 4 × 3 / 2
     = 6
```

Therefore, a simple undirected graph with 4 vertices can have at most:

```text
6 edges
```

A graph having all 6 edges is:

```text
K₄
```

---

# Cycle Graph vs Cyclic Graph

Remember this carefully:

```text
Cycle Graph
     ↓
Graph itself is one cycle
```

while:

```text
Cyclic Graph
     ↓
Graph contains at least one cycle
```

Example:

```text
C₄
```

is both:

```text
Cycle Graph
+
Cyclic Graph
```

But:

```text
      1
     / \
    2---3
    |
    4
```

can be **cyclic** because it contains the cycle `1-2-3-1`, but it is not itself a pure cycle graph.

---

# Bipartite vs Complete Graph

A useful exam concept:

```text
K₂
```

is bipartite.

```text
K₃
```

is **not bipartite**, because it contains a triangle (an odd cycle).

In general:

```text
Kₙ is bipartite only when n ≤ 2
```

---

# Quick Revision

```text
Cycle Graph
→ Graph itself forms one cycle
→ Cₙ
→ Every vertex has degree 2
→ n vertices and n edges

Cyclic Graph
→ Contains at least one cycle
→ May contain other vertices/edges

DAG
→ Directed Acyclic Graph
→ Directed graph
→ No directed cycle
→ Topological sorting is possible

Bipartite Graph
→ Vertices divided into 2 sets
→ No edge within the same set
→ No odd cycle

Simple Graph
→ Undirected graph
→ No self-loops
→ No parallel/multiple edges
```

---

# ⭐ Must Remember for MCQ

```text
Cₙ
↓
Cycle Graph
↓
n vertices
↓
n edges
↓
Every vertex degree = 2
```

```text
Cyclic Graph
↓
Contains at least one cycle
```

```text
DAG
↓
Directed
+
Acyclic
↓
No directed cycle
↓
Topological Sort possible
```

```text
Bipartite
↓
2 Sets
↓
No same-set edge
↓
No odd cycle
```

```text
Simple Graph
↓
Undirected
↓
No self-loop
↓
No parallel edge
```

---

# 🎯 One-Line Exam Tricks

| Question                                              | Answer              |
| ----------------------------------------------------- | ------------------- |
| Graph itself forms one cycle?                         | **Cycle Graph**     |
| Graph contains at least one cycle?                    | **Cyclic Graph**    |
| Directed graph with no cycle?                         | **DAG**             |
| Graph divisible into two sets with no same-set edges? | **Bipartite Graph** |
| Graph with no loops and no parallel edges?            | **Simple Graph**    |
| Every vertex in `Cₙ` has what degree?                 | **2**               |
| `Cₙ` has how many edges?                              | **n**               |
| Bipartite graph contains what type of cycle?          | **No odd cycle**    |
| Can a DAG contain a directed cycle?                   | **No**              |
| Maximum edges in simple undirected graph?             | **n(n−1)/2**        |
| Can a simple graph have a self-loop?                  | **No**              |
| Can a simple graph have parallel edges?               | **No**              |
Acyclic Graph

The word Acyclic means:

A = Without
Cyclic = Cycle

Therefore:

An Acyclic Graph is a graph that contains no cycle.

Example
1 -------- 2
            |
            |
            3 -------- 4

There is no path that starts from a vertex and comes back to the same vertex.

Therefore:

No Cycle
   ↓
Acyclic Graph
Example of a Cyclic Graph
      1
     / \
    /   \
   2-----3

Here we have:

1 → 2 → 3 → 1

This is a cycle.

Therefore:

Contains Cycle
      ↓
Cyclic Graph

It is not acyclic.

Acyclic vs Cyclic
Feature	Acyclic Graph	Cyclic Graph
Contains a cycle?	No	Yes, at least one
Example	Tree	Cycle Graph
Cycle detection	No cycle	At least one cycle
Easy Trick
Acyclic
   ↓
NO Cycle
Cyclic
   ↓
HAS Cycle

<img width="829" height="381" alt="image" src="https://github.com/user-attachments/assets/16791925-7a02-46e8-acc9-7870db5afe65" />
<img width="437" height="250" alt="image" src="https://github.com/user-attachments/assets/310914ea-2b04-43e0-9f08-23c73b1292f6" />

<img width="816" height="410" alt="image" src="https://github.com/user-attachments/assets/1cb0bb45-714a-465e-8fbf-111f44d10c8e" />
<img width="644" height="295" alt="image" src="https://github.com/user-attachments/assets/f3d619da-b593-4ed0-8061-49e4629b7422" />

<img width="833" height="386" alt="image" src="https://github.com/user-attachments/assets/a837448a-4a1e-4f55-bb09-b86792902547" />
<img width="769" height="366" alt="image" src="https://github.com/user-attachments/assets/1de4903f-c910-4e7d-9952-7d3e2efacd92" />
<img width="858" height="446" alt="image" src="https://github.com/user-attachments/assets/5c711c71-6f33-4afd-aaef-57f3d81716a5" />

<img width="645" height="857" alt="image" src="https://github.com/user-attachments/assets/e231d11a-cbf6-4e93-8922-8089044769f0" />
<img width="473" height="669" alt="image" src="https://github.com/user-attachments/assets/12398848-119f-4a61-9dbc-94a0544269ca" />



