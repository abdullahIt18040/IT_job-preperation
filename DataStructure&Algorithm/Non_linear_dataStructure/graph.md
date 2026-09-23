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
### Graph representaion 
# Graph Representation

**Graph Representation** means storing a graph in computer memory so that we can efficiently perform operations such as:

* Add/remove vertices
* Add/remove edges
* Check whether two vertices are connected
* Traverse the graph using BFS/DFS
* Find paths

A graph consists of:

```text
Graph = Vertices (V) + Edges (E)
```

There are several common ways to represent a graph:

1. Adjacency Matrix
2. Adjacency List
3. Incidence Matrix
4. Edge List

---

# 1. Adjacency Matrix

An **Adjacency Matrix** represents a graph using a **2D matrix**.

If there are `n` vertices, the matrix size is:

```text
n × n
```

For an unweighted graph:

```text
1 → Edge exists
0 → No edge
```

---

## Example Graph

Consider:

```text
      1
     / \
    /   \
   2-----3
```

Edges are:

```text
E = {(1,2), (1,3), (2,3)}
```

The vertices are:

```text
V = {1,2,3}
```

### Adjacency Matrix

```text
      1  2  3
    +---------
1   |  0  1  1
2   |  1  0  1
3   |  1  1  0
```

Explanation:

```text
Matrix[1][2] = 1
```

means:

```text
1 is connected to 2
```

Similarly:

```text
Matrix[1][3] = 1
```

means:

```text
1 is connected to 3
```

---

## Important Property of Undirected Graph

For an undirected graph:

```text
A[i][j] = A[j][i]
```

Therefore, the adjacency matrix is **symmetric**.

Example:

```text
A[1][2] = 1
A[2][1] = 1
```

---

## Adjacency Matrix Space Complexity

For `n` vertices:

```text
Space = O(n²)
```

because we need:

```text
n × n
```

cells.

### Edge Checking

To check whether an edge exists:

```text
A[u][v]
```

This takes:

```text
O(1)
```

### Key Points

```text
Adjacency Matrix
       ↓
2D Array
       ↓
Size = n × n
       ↓
Space = O(n²)
       ↓
Edge lookup = O(1)
```

---

# 2. Adjacency List

An **Adjacency List** stores a list of the neighboring vertices for each vertex.

Consider the same graph:

```text
      1
     / \
    /   \
   2-----3
```

Edges:

```text
(1,2)
(1,3)
(2,3)
```

### Adjacency List

```text
1 → 2 → 3

2 → 1 → 3

3 → 1 → 2
```

This means:

```text
Vertex 1
→ Connected to 2 and 3

Vertex 2
→ Connected to 1 and 3

Vertex 3
→ Connected to 1 and 2
```

---

## Adjacency List Using Array/List

Conceptually:

```text
Adj[1] = [2, 3]
Adj[2] = [1, 3]
Adj[3] = [1, 2]
```

---

# Adjacency List Space Complexity

For a graph with:

```text
V = Number of vertices
E = Number of edges
```

Space complexity is:

```text
O(V + E)
```

For a **sparse graph**, adjacency lists are usually much more space-efficient than an `O(V²)` matrix.

### Key Points

```text
Adjacency List
       ↓
Stores neighbors
       ↓
Space = O(V + E)
```

---

# 3. Incidence Matrix

An **Incidence Matrix** represents the relationship between:

```text
Vertices ↔ Edges
```

Unlike an adjacency matrix:

```text
Adjacency Matrix
→ Vertex × Vertex
```

while:

```text
Incidence Matrix
→ Vertex × Edge
```

---

## Example

Consider:

```text
      1
     / \
    /   \
   2-----3
```

Edges:

```text
e1 = (1,2)
e2 = (1,3)
e3 = (2,3)
```

The incidence matrix is:

```text
       e1 e2 e3
      ----------
1      1  1  0
2      1  0  1
3      0  1  1
```

Here:

```text
1 → incident to e1 and e2
2 → incident to e1 and e3
3 → incident to e2 and e3
```

### Matrix Size

If:

```text
V = Number of vertices
E = Number of edges
```

then:

```text
Incidence Matrix Size = V × E
```

---

# 4. Edge List

An **Edge List** simply stores all edges of the graph.

Example:

```text
      1
     / \
    /   \
   2-----3
```

Edges:

```text
(1,2)
(1,3)
(2,3)
```

Therefore:

```text
Edge List:

[
  (1,2),
  (1,3),
  (2,3)
]
```

For a weighted graph:

```text
(1,2,10)
(1,3,20)
(2,3,15)
```

where the third value represents the edge weight.

---

# Weighted Graph Representation

Consider:

```text
1 ----10---- 2
 \           /
  \         /
   20      15
     \     /
       3
```

Here:

```text
Weight(1,2) = 10
Weight(1,3) = 20
Weight(2,3) = 15
```

### Weighted Adjacency Matrix

```text
      1   2   3
    +-----------
1   |  0  10  20
2   | 10   0  15
3   | 20  15   0
```

The value represents the edge weight.

---

# Directed Graph Representation

Consider:

```text
1 --------> 2
|            |
|            ↓
└──────────> 3
```

Edges:

```text
1 → 2
1 → 3
2 → 3
```

### Directed Adjacency Matrix

```text
      1  2  3
    +---------
1   |  0  1  1
2   |  0  0  1
3   |  0  0  0
```

Notice:

```text
A[1][2] = 1
```

but:

```text
A[2][1] = 0
```

because the edge exists only:

```text
1 → 2
```

not:

```text
2 → 1
```

---

# Adjacency Matrix vs Adjacency List

| Feature                       | Adjacency Matrix | Adjacency List          |
| ----------------------------- | ---------------- | ----------------------- |
| Data structure                | 2D Array         | Array/List of neighbors |
| Space                         | `O(V²)`          | `O(V + E)`              |
| Edge lookup                   | `O(1)`           | Usually `O(degree)`     |
| Best for                      | Dense graphs     | Sparse graphs           |
| Easy to implement             | Yes              | Yes                     |
| BFS/DFS                       | Possible         | Very common             |
| Represents neighbors directly | No               | **Yes**                 |

---

# Dense vs Sparse Graph

## Dense Graph

A graph is **dense** when it has a large number of edges, close to the maximum possible.

Example:

```text
Many vertices
+
Many edges
↓
Dense Graph
```

For dense graphs:

```text
Adjacency Matrix
```

can be convenient.

---

## Sparse Graph

A graph is **sparse** when it has relatively few edges compared with the number of vertices.

Example:

```text
Many vertices
+
Few edges
↓
Sparse Graph
```

For sparse graphs:

```text
Adjacency List
```

is generally more space-efficient.

---

# Graph Representation and BFS/DFS

BFS and DFS commonly use an **Adjacency List**.

Example:

```text
Adjacency List

1 → 2, 3
2 → 1, 4
3 → 1
4 → 2
```

### BFS

```text
Queue
 ↓
Visit level by level
```

### DFS

```text
Stack / Recursion
 ↓
Go deep first
```

The graph representation stores the connections; BFS/DFS uses those connections for traversal.

---

# ⭐ Exam Must Remember

```text
Adjacency Matrix
→ Vertex × Vertex
→ 2D Array
→ O(V²)
→ Edge lookup O(1)
```

```text
Adjacency List
→ Vertex → Neighbors
→ O(V + E)
→ Good for sparse graphs
```

```text
Incidence Matrix
→ Vertex × Edge
→ V × E
```

```text
Edge List
→ Stores edges directly
→ (u,v)
```

---

# 🎯 Quick MCQ Table

| Question                                     | Answer                       |
| -------------------------------------------- | ---------------------------- |
| Which representation uses a 2D array?        | **Adjacency Matrix**         |
| Adjacency matrix size for `V` vertices?      | **V × V**                    |
| Space complexity of adjacency matrix?        | **O(V²)**                    |
| Edge lookup in adjacency matrix?             | **O(1)**                     |
| Which representation stores neighbors?       | **Adjacency List**           |
| Space complexity of adjacency list?          | **O(V + E)**                 |
| Which is generally better for sparse graphs? | **Adjacency List**           |
| Which is convenient for dense graphs?        | **Adjacency Matrix**         |
| Incidence matrix represents what?            | **Vertex–Edge relationship** |
| Incidence matrix size?                       | **V × E**                    |
| Edge list stores what?                       | **List of edges**            |
| Undirected adjacency matrix is what?         | **Symmetric**                |

---

# 🧠 Super Short Memory Trick

```text
Adjacency Matrix
→ Who is connected to whom?
→ Vertex × Vertex

Adjacency List
→ Who are my neighbors?
→ Vertex → Neighbors

Incidence Matrix
→ Which vertex belongs to which edge?
→ Vertex × Edge

Edge List
→ What are the edges?
→ (u, v)
```

---



## adjacent matrix & Adjacency list 
<img width="833" height="400" alt="image" src="https://github.com/user-attachments/assets/fa8e7e10-a8e3-475a-bc1f-54867dd81f6d" />


# Cycle Detection using BFS and DFS

## 1. BFS — Undirected Graph

```text
1. Start BFS from a vertex.
2. Mark the vertex as visited.
3. Put the vertex into the queue.
4. Remove a vertex from the queue.
5. Check all its neighbors.

6. If neighbor is unvisited:
   → Mark visited
   → Set parent
   → Add to queue

7. If neighbor is already visited
   and neighbor != parent:
   → Cycle exists.

8. Repeat for all vertices.
```

### Rule

```text
Visited Neighbor + Not Parent = Cycle
```

---

## 2. DFS — Undirected Graph

```text
1. Start DFS from a vertex.
2. Mark the vertex as visited.
3. Check all its neighbors.

4. If neighbor is unvisited:
   → Set parent
   → Apply DFS on neighbor

5. If neighbor is already visited
   and neighbor != parent:
   → Cycle exists.

6. Repeat for all vertices.
```

### Rule

```text
Visited Neighbor + Not Parent = Cycle
```

---

## BFS vs DFS

```text
BFS → Queue
DFS → Recursion / Stack

Both:
Visited Neighbor + Not Parent → Cycle
```

### Complexity

```text
Time  = O(V + E)
Space = O(V)
```
<img width="817" height="330" alt="image" src="https://github.com/user-attachments/assets/2302aad6-c5b2-44c8-8ae0-8f0a20069758" />

## Excercise DFS
<img width="731" height="341" alt="image" src="https://github.com/user-attachments/assets/ad3ef1c1-0b0a-407a-a97e-e93ce01caa47" />

<img width="747" height="220" alt="image" src="https://github.com/user-attachments/assets/93e55419-7c3e-4bb6-9045-5818194c52e0" />
<img width="1263" height="726" alt="image" src="https://github.com/user-attachments/assets/d7cd2979-5705-4918-93e8-423c208cce35" />
<img width="1308" height="741" alt="image" src="https://github.com/user-attachments/assets/f8eeeacd-85be-4ff3-a27c-3c13f0e882fa" />
## excercise :

<img width="926" height="439" alt="image" src="https://github.com/user-attachments/assets/b5cdb87f-445e-400f-8664-87f4a23740dc" />
<img width="949" height="445" alt="image" src="https://github.com/user-attachments/assets/a83229e7-c8e8-480a-9e2a-ed604ca33b69" />



# Dijkstra's Algorithm

**Dijkstra's Algorithm** is a **Greedy Algorithm** used to find the **Single-Source Shortest Path (SSSP)** in a **weighted graph with non-negative edge weights**.

## Key Points

```text
Type        → Greedy Algorithm
Problem     → Single-Source Shortest Path
Graph       → Weighted Graph
Weight      → Non-negative (≥ 0)
Data Struct → Priority Queue / Min Heap
```

### Basic Idea

```text
1. Set source distance = 0
2. Set all other distances = ∞
3. Select the unvisited vertex with minimum distance
4. Relax its neighboring vertices
5. Repeat until all vertices are processed
```

### Relaxation

```text
if dist[u] + weight(u,v) < dist[v]

    dist[v] = dist[u] + weight(u,v)
```

### Example

```text
A ----4---- B
|
1
|
C ----3---- D
```

Source:

```text
A
```

Shortest path to `D`:

```text
A → C → D
```

Distance:

```text
1 + 3 = 4
```

## Complexity

Using **Priority Queue + Adjacency List**:

```text
Time  → O((V + E) log V)
Space → O(V + E)
```

## Important Rules

```text
Dijkstra → Non-negative weights
BFS      → Unweighted shortest path
Bellman-Ford → Negative weights
```
## Bellman for algoritm
```
Bellman-Ford:
V = number of vertices
Maximum iterations = V - 1

If an iteration makes no distance update:
→ Stop early
→ Further iterations are unnecessary
n= vertix , iteration = n-1
 iteration maximum n-1 ber kora lagbe er basi kore lav nai same value repeat hoi
```
<img width="1176" height="655" alt="image" src="https://github.com/user-attachments/assets/a660d5ff-6475-4c0d-be06-53276faa2678" />
<img width="1176" height="470" alt="image" src="https://github.com/user-attachments/assets/ac60e0c8-0199-490b-9c5f-d8f6964bb857" />
<img width="1176" height="660" alt="image" src="https://github.com/user-attachments/assets/4b71cb63-e52f-4eca-8fee-20afdce6323c" />

```
negative cycle থাকলে Bellman-Ford shortest path নির্দিষ্টভাবে বের করতে পারে না—তবে গুরুত্বপূর্ণ বিষয় হলো, Bellman-Ford negative cycle detect করতে পারে।

🔴 Negative Cycle কী?

যদি কোনো cycle-এর সব edge-এর weight যোগ করলে ফলাফল negative হয়:

A → B = 2
B → C = -5
C → A = 1

Total = 2 + (-5) + 1
      = -2

তাহলে এটি একটি Negative Cycle।
Dijkstra vs Bellman-Ford:



Dijkstra → Negative edge weight and → Negative edge cycle  handle করতে পারে না 

Bellman-Ford → Negative edge handle করতে পারে 

Bellman-Ford → Negative cycle detect করতে পারে 

Reachable negative cycle থাকলে → shortest path undefined/does not exist।

```
### We have to write in bellfor algorim in exaim is 
```

Time complext is 

```

<img width="840" height="428" alt="image" src="https://github.com/user-attachments/assets/e8c2fbb6-3d2f-48de-be93-f5d72d3283ed" />


