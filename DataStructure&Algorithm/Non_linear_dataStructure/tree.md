## Tree Trasvarsal
## Sorting Algorith
## Searching algorithm
### must be learn algoritm with code :

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
# BST — Case 3: Two Children

When a node has **two children**, we cannot simply remove it because the **BST property may be violated**.

We replace the node with either:

1. **Inorder Successor**
2. **Inorder Predecessor**

---

## 1. Inorder Successor

**Inorder Successor = Smallest value in the Right Subtree**

### Example

```text
        50
       /  \
     30    70
          /  \
        60    80
```

Delete `70`.

Right subtree of `70`:

```text
    80
```

So:

```text
Inorder Successor = 80
```

Replace `70` with `80`:

```text
        50
       /  \
     30    80
          /
        60
```

---

## 2. Inorder Predecessor

**Inorder Predecessor = Largest value in the Left Subtree**

Using the same tree:

```text
        50
       /  \
     30    70
          /  \
        60    80
```

Delete `70`.

Left subtree of `70`:

```text
    60
```

So:

```text
Inorder Predecessor = 60
```

Replace `70` with `60`:

```text
        50
       /  \
     30    60
             \
              80
```

---
### BST — Case 3: Two Children
```
Consider this BST:

        50
       /  \
     30    70
          /  \
        60    80
             / \
            78  90

Now we want to delete 70.

Using Inorder Successor
Step 1: Find the Right Subtree

Right subtree of 70:

        80
       /  \
      78   90
Step 2: Find the Smallest Value

The smallest value in the right subtree is:

78

Therefore:

Inorder Successor = 78
Step 3: Replace 70 with 78
        50
       /  \
     30    78
          /  \
        60    80
                \
                 90

The original 78 is removed from under 80.
```


# Why BST Worst Case = O(n)?

BST-এর **worst case** হয় যখন tree টি **skewed** বা একদিকে লম্বা হয়ে যায়।

```text
10
  \
   20
     \
      30
        \
         40
```

এখানে প্রত্যেক node-এর **শুধু একটি child** আছে। তাই এই BST দেখতে অনেকটা **Linked List-এর মতো** হয়ে গেছে।

## Search করলে কী হয়?

ধরি, আমরা `40` খুঁজছি:

```text
40
 ↓
10 → 20 → 30 → 40
```

এক এক করে **10, 20, 30, 40** — সব node দেখতে হচ্ছে।

যদি মোট `n`টি node থাকে:

```text
Number of nodes checked ≈ n
```

তাই:

```text
Time Complexity = O(n)
```

## Balanced BST হলে

```text
        40
       /  \
     20    60
    / \    / \
   10 30  50 70
```

প্রতিবার search করলে প্রায় অর্ধেক অংশ বাদ দেওয়া যায়।

```text
Time Complexity = O(log n)
```

## Easy Comparison

```text
Balanced BST → Height ≈ log n → O(log n)

Skewed BST   → Height ≈ n     → O(n)
```

## Key Point

> BST-এর **Search, Insert, Delete** complexity মূলত tree-এর **height (h)**-এর উপর নির্ভর করে।

```text
h ≈ log n → O(log n)

h ≈ n     → O(n)
```
<img width="785" height="246" alt="image" src="https://github.com/user-attachments/assets/23203d7b-7260-4c74-807e-b0dd06eb9886" />
<img width="812" height="574" alt="image" src="https://github.com/user-attachments/assets/875f1ceb-e1e0-4343-897c-a42acbe17e92" />
<img width="1142" height="649" alt="image" src="https://github.com/user-attachments/assets/aba5b1ab-5b6e-42bd-98bb-ee2625a81b3b" />
<img width="1089" height="463" alt="image" src="https://github.com/user-attachments/assets/4ec5f380-bb77-4069-81e3-1d0584d1a68c" />




<img width="1191" height="542" alt="image" src="https://github.com/user-attachments/assets/eb47c356-5b57-457b-9a95-31b471f82f90" />

<img width="611" height="655" alt="image" src="https://github.com/user-attachments/assets/3ecf29cf-213f-40d3-8309-e9d2d63ac412" />
<img width="1101" height="487" alt="image" src="https://github.com/user-attachments/assets/3b8221fc-1dc0-436b-9362-acdb88065101" />
<img width="745" height="476" alt="image" src="https://github.com/user-attachments/assets/382cd769-7374-45e4-afda-aa010211fd50" />
<img width="791" height="308" alt="image" src="https://github.com/user-attachments/assets/0a576178-42cc-4523-b45f-2c4f5055726d" />
<img width="1088" height="547" alt="image" src="https://github.com/user-attachments/assets/9ae353b6-f852-4657-8b1b-253d02c74579" />
### FUll Binay tree
<img width="1332" height="746" alt="image" src="https://github.com/user-attachments/assets/a0f065cc-5090-441e-aa21-848d0b0d8185" />
<img width="502" height="620" alt="image" src="https://github.com/user-attachments/assets/a0e3ea1f-787d-434c-bc22-dd556c63f120" />
<img width="653" height="631" alt="image" src="https://github.com/user-attachments/assets/6c746a8d-d0e3-4298-82da-595bd71c2cf9" />
<img width="607" height="413" alt="image" src="https://github.com/user-attachments/assets/d3cf78d1-c0c0-4872-a8b6-455e1828c708" />
<img width="1018" height="310" alt="image" src="https://github.com/user-attachments/assets/08b2000a-3b86-4196-9f39-612617420120" />
<img width="716" height="537" alt="image" src="https://github.com/user-attachments/assets/6573ee9e-c231-4e48-8cd5-ce22541dd87c" />
<img width="861" height="548" alt="image" src="https://github.com/user-attachments/assets/836d4b6f-787d-4faf-8037-5213f395dd8b" />
<img width="1046" height="514" alt="image" src="https://github.com/user-attachments/assets/b5069547-4d71-4f5e-b028-6e2dc4a5cfd3" />
<img width="1193" height="416" alt="image" src="https://github.com/user-attachments/assets/a865b4ce-ff8d-47e4-9b3d-d060217f3d6b" />
### Complete Binay tree
<img width="739" height="369" alt="image" src="https://github.com/user-attachments/assets/02ea95f4-1107-412d-9a01-fa95f025e758" />
## not complete binARY tree 
<img width="345" height="170" alt="image" src="https://github.com/user-attachments/assets/200e2ca3-4bda-424e-b0a2-e9f1046bd3f2" />
## complete binary tree math 
<img width="764" height="393" alt="image" src="https://github.com/user-attachments/assets/8bea3cda-f28c-41cc-8897-350b5965c3c3" />

### Perfecr Binary tree 
<img width="366" height="449" alt="image" src="https://github.com/user-attachments/assets/d12116a1-2883-4ebd-961b-f21084656822" />

## AVL tree 
<img width="894" height="583" alt="image" src="https://github.com/user-attachments/assets/8e1514fd-a235-4ce6-8ab6-dba787b4cd9e" />

<img width="631" height="375" alt="image" src="https://github.com/user-attachments/assets/7e94aaf8-c400-4467-a92e-876d3cdc809f" />

<img width="748" height="383" alt="image" src="https://github.com/user-attachments/assets/185bc1a1-09d7-4421-b90c-c89025dcd702" />





<img width="1253" height="483" alt="image" src="https://github.com/user-attachments/assets/f98a44db-20eb-48d1-83d3-d8da37028e23" />
<img width="632" height="473" alt="image" src="https://github.com/user-attachments/assets/9dab53ee-eae8-423e-8c09-3092b98f5bf8" />
<img width="573" height="391" alt="image" src="https://github.com/user-attachments/assets/0b532d0e-cc91-41c4-bceb-54013a697967" />
<img width="531" height="279" alt="image" src="https://github.com/user-attachments/assets/8661f3ae-dadb-4625-a05d-174ca113df45" />
<img width="1050" height="254" alt="image" src="https://github.com/user-attachments/assets/995b580d-bf93-4bff-a156-a1355a65d7ac" />
<img width="1029" height="521" alt="image" src="https://github.com/user-attachments/assets/0ffa0481-d3c9-4d38-b7f9-83b4b2acfeab" />
## Heap
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

##
<img width="744" height="251" alt="image" src="https://github.com/user-attachments/assets/f8084c87-cbec-453b-980a-31c1231a1fa6" />
## Tree must be Complete binary tree  to work heap 
<img width="1046" height="272" alt="image" src="https://github.com/user-attachments/assets/cf3880e2-e0bd-47d1-93a0-abb0a62abc7e" />
<img width="454" height="636" alt="image" src="https://github.com/user-attachments/assets/66e9ad9b-e253-4402-8562-c1c2aff5d500" />
<img width="658" height="666" alt="image" src="https://github.com/user-attachments/assets/7e8b225f-63fb-46d7-b7ba-aac854d9085b" />
same vabe min heap jonno odelete hobe:

## Algorithm of Heap 
<img width="1154" height="648" alt="image" src="https://github.com/user-attachments/assets/cfe3ec0e-3d32-4e6c-9f98-9edc0ccce1ba" />
## Question 
<img width="1050" height="570" alt="image" src="https://github.com/user-attachments/assets/b96bc033-2fec-4875-81de-c26849f17087" />
<img width="594" height="751" alt="image" src="https://github.com/user-attachments/assets/28188f5d-df97-41c4-b961-1e2def87a544" />

<img width="896" height="569" alt="image" src="https://github.com/user-attachments/assets/efbab298-c794-4963-97cc-00e14f48dd49" />
## BFS Algorith :

 BFS Search level by level 
 
<img width="1162" height="664" alt="image" src="https://github.com/user-attachments/assets/51ae007a-2c61-472c-9537-8243d971cd2d" />

## DFS Algorith 
it work  Deapt 
<img width="1166" height="672" alt="image" src="https://github.com/user-attachments/assets/80690e28-9a62-47d7-b439-9c19f5831d3b" />
<img width="1041" height="541" alt="image" src="https://github.com/user-attachments/assets/e7579ad0-9a1e-4bd7-8992-27afc21e4228" />
<img width="1137" height="382" alt="image" src="https://github.com/user-attachments/assets/07900d0a-cc5f-4b72-bc0d-a8caa0c67050" />













