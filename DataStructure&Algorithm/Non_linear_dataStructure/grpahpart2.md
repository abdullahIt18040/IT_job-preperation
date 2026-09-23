##  spaining tree
<img width="1167" height="688" alt="image" src="https://github.com/user-attachments/assets/489819da-5dec-4158-85b9-2ec3fc51575d" />

<img width="1055" height="661" alt="image" src="https://github.com/user-attachments/assets/e0f42c96-82ee-4aca-8992-51f94f963c5c" />

##  find all spaning tree  how many spanig tree possible  (E c E`) 
``` now For weihgt graph find minimum cost of all spning tree, which cost is minimum this is the minimum spning tree.

take minimum weight always
```
<img width="1119" height="507" alt="image" src="https://github.com/user-attachments/assets/b33df315-22ce-44a4-920f-6d1dd0d73c06" />

When cycle exist  then 
<img width="396" height="342" alt="image" src="https://github.com/user-attachments/assets/279cb879-cde4-487b-9fc2-38e125f6b753" />
## For complete Graph 
<img width="1088" height="343" alt="image" src="https://github.com/user-attachments/assets/d46a8c2e-d5cb-431b-9681-752f65948c9c" />

## Minimum spaning tree

<img width="830" height="427" alt="image" src="https://github.com/user-attachments/assets/2788cefc-a928-4874-ae32-6f0089992449" />
<img width="691" height="161" alt="image" src="https://github.com/user-attachments/assets/e00baaec-3e41-4d21-b16e-966672c42a63" />

<img width="925" height="456" alt="image" src="https://github.com/user-attachments/assets/df440ff1-a9cf-4fff-bfb2-7ee2e4667410" />
<img width="663" height="446" alt="image" src="https://github.com/user-attachments/assets/64e09a15-396e-47b4-96c5-c2348f0f8e96" />

## Prims algorithm 
<img width="660" height="751" alt="image" src="https://github.com/user-attachments/assets/a437c9fb-cb0c-430e-947f-215774f725ec" />
# Minimum Spanning Tree (MST)

A **Minimum Spanning Tree** connects all vertices of a connected, weighted, undirected graph with:

* **V - 1 edges**
* Minimum possible total edge weight
* No cycle

---

## Prim's Algorithm

**Prim's Algorithm** builds the MST by starting from any vertex and repeatedly selecting the **minimum-weight edge** that connects a visited vertex to an unvisited vertex.

### Steps

```text
1. Start from any vertex.
2. Mark it as visited.
3. Select the minimum-weight edge to an unvisited vertex.
4. Add the edge and vertex to MST.
5. Repeat until all vertices are visited.
```

### Complexity

```text
Using Priority Queue → O(E log V)
Using Adjacency Matrix → O(V²)
```

---

## Kruskal's Algorithm

**Kruskal's Algorithm** builds the MST by selecting edges in **increasing order of weight** while avoiding cycles.

### Steps

```text
1. Sort all edges by weight.
2. Select the smallest edge.
3. If it does not create a cycle, add it to MST.
4. Use Disjoint Set / Union-Find for cycle detection.
5. Repeat until V - 1 edges are selected.
```

### Complexity

```text
Time  → O(E log E)
Space → O(V)
```

---

## Prim's vs Kruskal's

```text
Prim's   → Vertex-based → Uses Priority Queue
Kruskal's → Edge-based  → Uses Union-Find
```

> **Remember:**
> **Prim → Grow the tree**
> **Kruskal → Pick the smallest edges**

