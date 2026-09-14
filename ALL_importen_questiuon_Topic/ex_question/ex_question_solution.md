##1. Difference between DFS and bfs With example .
# BFS vs DFS

## 1. Overview

**BFS (Breadth-First Search)** and **DFS (Depth-First Search)** are graph and tree traversal algorithms.

They are used to visit all or selected nodes of a graph/tree systematically.

---

# 2. Example Graph

```text
        A
       / \
      B   C
     / \   \
    D   E   F
```

---

# 3. BFS — Breadth-First Search

BFS visits nodes **level by level**.

### Traversal

```text
A → B → C → D → E → F
```

### Level Order

```text
Level 0 → A
Level 1 → B, C
Level 2 → D, E, F
```

### Data Structure

BFS uses a **Queue**.

```text
Queue → FIFO
       First In, First Out
```

### Basic Process

```text
1. Start from the source node.
2. Add the source node to the Queue.
3. Mark it as visited.
4. Remove a node from the Queue.
5. Visit all unvisited neighbors.
6. Add those neighbors to the Queue.
7. Repeat until the Queue is empty.
```

### Java Example

```java
Queue<Integer> queue = new LinkedList<>();
boolean[] visited = new boolean[n];

queue.offer(start);
visited[start] = true;

while (!queue.isEmpty()) {

    int node = queue.poll();

    System.out.println(node);

    for (int neighbor : graph[node]) {

        if (!visited[neighbor]) {
            visited[neighbor] = true;
            queue.offer(neighbor);
        }
    }
}
```

---

# 4. DFS — Depth-First Search

DFS visits a node and then goes **as deep as possible** before backtracking.

### Traversal

One possible traversal:

```text
A → B → D → E → C → F
```

### Data Structure

DFS uses:

```text
Stack
```

or

```text
Recursion
```

### Basic Process

```text
1. Start from the source node.
2. Mark the node as visited.
3. Visit an unvisited neighbor.
4. Continue deeper.
5. When there are no unvisited neighbors, backtrack.
6. Repeat until all reachable nodes are visited.
```

### Java Example — Recursive DFS

```java
boolean[] visited = new boolean[n];

void dfs(int node) {

    visited[node] = true;

    System.out.println(node);

    for (int neighbor : graph[node]) {

        if (!visited[neighbor]) {
            dfs(neighbor);
        }
    }
}
```

---

# 5. BFS vs DFS

| Feature            | BFS                            | DFS                                   |
| ------------------ | ------------------------------ | ------------------------------------- |
| Full Form          | Breadth-First Search           | Depth-First Search                    |
| Approach           | Level by level                 | Go as deep as possible                |
| Data Structure     | Queue                          | Stack / Recursion                     |
| Principle          | FIFO                           | LIFO                                  |
| Shortest Path      | Guaranteed in unweighted graph | Not guaranteed                        |
| Memory             | Can require more memory        | Usually requires less for wide graphs |
| Tree Traversal     | Level-order                    | Preorder/Inorder/Postorder concepts   |
| Backtracking       | Not the main approach          | Commonly used                         |
| Cycle Detection    | Yes                            | Yes                                   |
| Topological Sort   | Kahn's Algorithm               | DFS-based approach                    |
| Maze/Path Problems | Useful                         | Very useful                           |
| Time Complexity    | O(V + E)                       | O(V + E)                              |
| Space Complexity   | O(V)                           | O(V)                                  |

---

# 6. Shortest Path Example

Consider:

```text
A ── B ── D
│
└── C ── E
```

We want to find the shortest path from `A` to `E`.

### BFS

BFS explores level by level:

```text
Level 0 → A
Level 1 → B, C
Level 2 → D, E
```

Therefore:

```text
A → C → E
```

is found as the shortest path.

### DFS

DFS may first explore:

```text
A → B → D
```

Then backtrack:

```text
A → C → E
```

DFS can find a path, but it **does not guarantee the shortest path**.

---

# 7. Time Complexity

For a graph:

```text
V = Number of Vertices
E = Number of Edges
```

### BFS

```text
Time Complexity  → O(V + E)
Space Complexity → O(V)
```

### DFS

```text
Time Complexity  → O(V + E)
Space Complexity → O(V)
```

---

# 8. When to Use BFS?

Use BFS when:

* You need the shortest path in an **unweighted graph**.
* You need **level-order traversal**.
* You need to find nodes based on their distance from the source.
* You need to process nodes level by level.

### Common Problems

```text
Shortest path in unweighted graph
Level order traversal
Minimum number of steps
Social network distance
Word ladder
```

---

# 9. When to Use DFS?

Use DFS when:

* You need to explore deeply.
* You need backtracking.
* You need to detect cycles.
* You need connected components.
* You need topological sorting.
* You are solving maze/path exploration problems.

### Common Problems

```text
Cycle detection
Connected components
Topological sorting
Maze solving
Backtracking
Number of islands
Path existence
```

---

# 10. Easy Memory Trick

Remember these:

```text
BFS → Queue → FIFO → Level → Shortest Path
```

```text
DFS → Stack → LIFO → Depth → Backtracking
```

### One-Line Difference

```text
BFS explores neighbors first.
DFS explores deeper nodes first.
```

---

# 11. Interview / Exam Questions

### Q1. Which data structure is used by BFS?

```text
Answer: Queue
```

### Q2. Which data structure is used by DFS?

```text
Answer: Stack or Recursion
```

### Q3. Which algorithm guarantees the shortest path in an unweighted graph?

```text
Answer: BFS
```

### Q4. What is the time complexity of BFS?

```text
Answer: O(V + E)
```

### Q5. What is the time complexity of DFS?

```text
Answer: O(V + E)
```

### Q6. Which algorithm is commonly used for backtracking?

```text
Answer: DFS
```

### Q7. Which traversal visits nodes level by level?

```text
Answer: BFS
```

### Q8. Which traversal goes as deep as possible before backtracking?

```text
Answer: DFS
```

---

# 12. Final Comparison

```text
             Graph Traversal
                   |
          ┌────────┴────────┐
          │                 │
         BFS               DFS
          │                 │
        Queue          Stack/Recursion
          │                 │
         FIFO              LIFO
          │                 │
     Level by Level       Depth First
          │                 │
   Shortest Path*        Backtracking
```

`* BFS guarantees the shortest path when the graph is unweighted (or all edges have equal cost).`

