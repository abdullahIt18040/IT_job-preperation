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
### B tree
<img width="1161" height="633" alt="image" src="https://github.com/user-attachments/assets/81384e69-191e-4219-9079-5f8a20ce3680" />
<img width="558" height="375" alt="image" src="https://github.com/user-attachments/assets/866632a1-867f-47ef-b98c-a76d8774a135" />
<img width="534" height="625" alt="image" src="https://github.com/user-attachments/assets/d9667985-e9d7-490b-b673-c8c292224188" />

# 3-Order B-Tree

A **3-Order B-Tree** is a balanced multiway search tree where:

* Maximum **Children = 3**
* Maximum **Keys = 2**
* If a node gets **3 keys**, it causes **overflow**
* During split, the **middle key moves to the parent**
* All leaf nodes remain at the **same level**

---

## Example

Given array:

```text
6, 2, 4, 15, 18, 8, 27, 9, 10, 13, 12, 17
```

### Step 1: Insert 6

```text
[6]
```

### Step 2: Insert 2

```text
[2 | 6]
```

### Step 3: Insert 4

```text
[2 | 4 | 6]  → Overflow
```

Middle key `4` moves up:

```text
      [4]
     /   \
   [2]   [6]
```

---

### Step 4: Insert 15

```text
      [4]
     /   \
   [2]   [6 | 15]
```

### Step 5: Insert 18

Right node becomes:

```text
[6 | 15 | 18] → Overflow
```

Split and move `15` up:

```text
        [4 | 15]
       /   |    \
     [2]  [6]  [18]
```

---

### Step 6: Insert 8

```text
        [4 | 15]
       /    |      \
     [2]  [6 | 8]  [18]
```

### Step 7: Insert 27

```text
        [4 | 15]
       /    |       \
     [2]  [6 | 8]  [18 | 27]
```

---

### Step 8: Insert 9

`9` goes into `[6 | 8]`:

```text
[6 | 8 | 9] → Overflow
```

Split:

```text
Middle key = 8
```

Parent becomes:

```text
[4 | 8 | 15] → Overflow
```

Again split. Middle key `8` becomes the new root:

```text
              [8]
             /   \
           [4]   [15]
          /  \   /   \
        [2] [6] [9] [18 | 27]
```

---

### Step 9: Insert 10

```text
              [8]
             /   \
           [4]   [15]
          /  \   /     \
        [2] [6] [9|10] [18|27]
```

---

### Step 10: Insert 13

Right-middle node:

```text
[9 | 10 | 13] → Overflow
```

Middle key `10` moves to parent:

```text
              [8]
             /   \
           [4]   [10 | 15]
          /  \   /   |     \
        [2] [6] [9] [13] [18|27]
```

---

### Step 11: Insert 12

`12` goes to `[13]`:

```text
              [8]
             /   \
           [4]   [10 | 15]
          /  \   /      |       \
        [2] [6] [9]   [12 | 13] [18|27]
```

---

### Step 12: Insert 17

`17` goes to `[18 | 27]`:

```text
[17 | 18 | 27] → Overflow
```

Middle key `18` moves to parent:

```text
[10 | 15 | 18] → Overflow
```

Middle key `15` moves to root.

---

# Final 3-Order B-Tree

```text
                    [8 | 15]
                   /    |     \
                [4]    [10]   [18]
               /  \    /  \    /  \
             [2] [6] [9] [12|13] [17] [27]
```

---

## Split Summary

| Insert | Overflow       | Middle Key     |
| ------ | -------------- | -------------- |
| 4      | `[2, 4, 6]`    | `4`            |
| 18     | `[6, 15, 18]`  | `15`           |
| 9      | `[6, 8, 9]`    | `8`            |
| 9      | `[4, 8, 15]`   | `8` → New Root |
| 13     | `[9, 10, 13]`  | `10`           |
| 17     | `[17, 18, 27]` | `18`           |
| 17     | `[10, 15, 18]` | `15` → Root    |

---

## Important Rules

```text
Order = 3

Maximum Children = 3
Maximum Keys     = 2

If Keys > 2
      ↓
   Overflow
      ↓
    Split
      ↓
Middle Key → Parent
```

### Easy Formula

```text
Maximum Keys = Order - 1

For Order 3:

Maximum Keys = 3 - 1 = 2
```

### Remember

> **3-Order B-Tree = 2-3 Tree**

The tree always remains **balanced**, and all leaf nodes stay at the **same level**.
# B-Tree Time & Space Complexity

A **B-Tree** is a self-balancing multiway search tree.

## Time Complexity

| Operation | Time Complexity |
| --------- | --------------- |
| Search    | `O(log n)`      |
| Insertion | `O(log n)`      |
| Deletion  | `O(log n)`      |
| Traversal | `O(n)`          |

### Search

Because a B-Tree is balanced, its height is logarithmic:

```text
Height = O(log n)
```

Therefore:

```text
Search = O(log n)
```

### Insertion

Insertion may require node splitting:

```text
Find position
     ↓
Insert key
     ↓
Overflow?
     ↓
Split node
     ↓
Move middle key to parent
```

Overall:

```text
Insertion = O(log n)
```

### Deletion

Deletion may require:

* Borrowing a key
* Merging nodes
* Adjusting the parent

Overall:

```text
Deletion = O(log n)
```

### Traversal

Every key needs to be visited:

```text
Traversal = O(n)
```

---

# Space Complexity

If the B-Tree contains `n` keys:

```text
Space Complexity = O(n)
```

The tree needs memory to store all keys and child references.

---

# Summary

```text
B-Tree Complexity
-----------------

Search     → O(log n)
Insertion  → O(log n)
Deletion   → O(log n)
Traversal  → O(n)

Space      → O(n)

Height     → O(log n)
```

## MCQ Shortcut

> **B-Tree Search = O(log n)**
> **B-Tree Insertion = O(log n)**
> **B-Tree Deletion = O(log n)**
> **B-Tree Space = O(n)**
> 
###  B+ tree

<img width="1182" height="498" alt="image" src="https://github.com/user-attachments/assets/f449baf1-ca4e-477d-ac8c-55d990122175" />
<img width="966" height="672" alt="image" src="https://github.com/user-attachments/assets/c61ae3c0-f54b-40d2-b083-0b36bbe5c888" />
<img width="579" height="445" alt="image" src="https://github.com/user-attachments/assets/112f795f-4602-4053-9cd1-e54789a47811" />
# B+ Tree

A **B+ Tree** is a **self-balancing multiway search tree** and is widely used in **Databases and File Systems**.

## Key Features

* All actual **data/records are stored only in leaf nodes**.
* Internal nodes contain **keys/indexes** used for navigation.
* All leaf nodes are connected using a **linked list**.
* All leaf nodes remain at the **same level**.
* It is efficient for **search, insertion, deletion, and range queries**.

---

## Basic Structure

```text
                 [20 | 40]
                /    |     \
               /     |      \
          [5 | 10] [20 | 30] [40 | 50 | 60]
             ↓          ↓             ↓
             └──────────┴─────────────┘
                 Linked Leaf Nodes
```

### Important

```text
Internal Node
      ↓
Keys / Indexes

Leaf Node
      ↓
Actual Data / Records
```

---

# Search Example

Search for `30`:

```text
                 [20 | 40]
                /    |     \
               /     |      \
          [5 | 10] [20 | 30] [40 | 50]
                       ↑
                      30
```

Steps:

```text
30 > 20
30 < 40
      ↓
Go to middle child
      ↓
[20 | 30]
      ↓
Found 30
```

---

# Leaf Node Linked List

One of the most important features of a B+ Tree is that **leaf nodes are linked together**.

```text
[5 | 10] → [20 | 30] → [40 | 50 | 60]
```

This makes **sequential access and range queries efficient**.

---

# Range Search

Suppose we want:

```text
20 ≤ key ≤ 50
```

First find `20`:

```text
[5 | 10] → [20 | 30] → [40 | 50 | 60]
             ↑
           Start
```

Then follow the linked leaf nodes:

```text
[20 | 30] → [40 | 50]
```

Therefore, range search is efficient.

### Range Query Complexity

If `k` records are returned:

```text
O(log n + k)
```

Where:

* `O(log n)` → Find the starting key
* `O(k)` → Read `k` records

---

# B-Tree vs B+ Tree

| Feature           | B-Tree          | B+ Tree            |
| ----------------- | --------------- | ------------------ |
| Data location     | Internal + Leaf | **Only Leaf**      |
| Internal nodes    | Keys + Data     | **Keys/Indexes**   |
| Leaf nodes linked | Usually No      | **Yes**            |
| Range Search      | Less efficient  | **More efficient** |
| Sequential Access | Less efficient  | **More efficient** |
| Database Usage    | Common          | **Very common**    |

---

# Time Complexity

| Operation    | Complexity     |
| ------------ | -------------- |
| Search       | `O(log n)`     |
| Insertion    | `O(log n)`     |
| Deletion     | `O(log n)`     |
| Range Search | `O(log n + k)` |
| Traversal    | `O(n)`         |

Where `k` = number of records returned by the range query.

---

# Space Complexity

For `n` keys/records:

```text
Space Complexity = O(n)
```

---

# Why B+ Tree is Useful in Database?

Consider:

```sql
SELECT *
FROM employee
WHERE id BETWEEN 1000 AND 2000;
```

B+ Tree can:

```text
Find 1000
   ↓
Go to corresponding leaf
   ↓
Follow linked leaves
   ↓
Read 1001, 1002, ... 2000
```

This makes **range queries and sequential data access efficient**.

---

# Exam Shortcut

```text
B+ Tree
-------
Data → Only Leaf Nodes

Internal Node → Keys / Indexes

Leaf Nodes → Linked List

Search      → O(log n)
Insertion   → O(log n)
Deletion    → O(log n)
Range Search → O(log n + k)
Space       → O(n)
```

> **Remember:** B+ Tree = **Data in Leaf + Linked Leaves + Efficient Range Search**





### B tree and B+ tree
<img width="979" height="684" alt="image" src="https://github.com/user-attachments/assets/9f825bc4-a23b-4cde-812f-a3da49116ab6" />
<img width="1172" height="603" alt="image" src="https://github.com/user-attachments/assets/8296c20e-89a0-4946-9a1e-397f4b18d6f0" />
## Binary Search Tree
<img width="1203" height="600" alt="image" src="https://github.com/user-attachments/assets/4762fa9f-85e9-479f-a0bf-04aa4eaef8d4" />
# Binary Search Tree (BST)

## 1. What is BST?

A **Binary Search Tree (BST)** is a binary tree where:

```text
Left Subtree < Root < Right Subtree
```

Example:

```text
        50
       /  \
     30    70
    / \    / \
   20 40  60 80
```

## 2. Main Properties

* Each node has **at most 2 children**.
* Left values are **smaller** than the root.
* Right values are **greater** than the root.
* Inorder traversal gives **sorted order**.

```text
Inorder → 20 30 40 50 60 70 80
```

## 3. Search

To search for a value:

```text
If value < root → go left
If value > root → go right
If value == root → Found
```

Example: Search `60`

```text
60 < 50 ? No
60 > 50 → Right

60 < 70 → Left

60 == 60 → Found
```

## 4. Insert

Example: Insert `65`

```text
        50
          \
           70
          /
         60
           \
            65
```

Rule:

```text
Smaller → Left
Greater → Right
```

## 5. Delete

Three cases:

### Case 1: Leaf Node

```text
Delete 20
```

Simply remove it.

### Case 2: One Child

Replace the deleted node with its child.

### Case 3: Two Children

Replace with:

* **Inorder Successor** = smallest value in right subtree
* or **Inorder Predecessor** = largest value in left subtree

## 6. Time Complexity

| Operation |  Average | Worst |
| --------- | -------: | ----: |
| Search    | O(log n) |  O(n) |
| Insert    | O(log n) |  O(n) |
| Delete    | O(log n) |  O(n) |

**Space:** O(h)

Where `h` = height of the tree.

## 7. Why Worst Case O(n)?

If the tree becomes **skewed**:

```text
10
  \
   20
     \
      30
        \
         40
```

The BST behaves like a **Linked List**.

Therefore:

```text
Height = n
Time = O(n)
```

## 8. Key Point

> **BST = Binary Tree + Search Property**

```text
Left < Root < Right
```

### Memory Trick

**Search:** Compare → Left/Right
**Insert:** Compare → Find Empty Position
**Delete:** Leaf / One Child / Two Children
**Inorder:** Always gives Sorted Order










