# Data Structure
<img width="917" height="376" alt="image" src="https://github.com/user-attachments/assets/9b4d59a8-dcc1-4a73-98d1-41e3cd8d3578" />


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
### Array
```
# Array — IT Government Job Preparation

## 1. What is an Array?

An **Array** is a linear data structure that stores multiple elements of the **same data type** in a contiguous/sequential memory structure and accesses elements using an **index**.

```java
int[] numbers = {10, 20, 30, 40, 50};
```

```text
Index:    0    1    2    3    4
Value:   10   20   30   40   50
```

### Important

```text
First Index = 0
Last Index  = length - 1
```

For an array of size `n`:

```text
Valid Index = 0 to n-1
```

---

# 2. Important Features of Array

* Linear data structure
* Index-based access
* Fixed size in Java
* Fast random access
* Stores elements of the same declared type
* Supports 1D, 2D and multidimensional arrays
* Easy traversal
* Efficient for sequential access
* Array indexing starts from `0`

### Most Important for MCQ

> **Array provides O(1) random access using an index.**

---

# 3. Types of Array

## 3.1 One-Dimensional Array

```java
int[] arr = {10, 20, 30, 40};
```

```text
10   20   30   40
0    1    2    3
```

---

## 3.2 Two-Dimensional Array

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6}
};
```

```text
1  2  3
4  5  6
```

Access:

```java
matrix[1][2];   // 6
```

---

## 3.3 Multidimensional Array

```java
int[][][] data = new int[2][3][4];
```

---

## 3.4 Jagged Array

A jagged array is an array whose rows can have different lengths.

```java
int[][] arr = {
    {1, 2},
    {3, 4, 5},
    {6}
};
```

```text
Row 0 → 2 elements
Row 1 → 3 elements
Row 2 → 1 element
```

### Exam Point

> Java supports jagged arrays because a 2D array is actually an **array of arrays**.

---

# 4. Array Declaration and Initialization

## Declaration

```java
int[] arr;
```

or

```java
int arr[];
```

Both are valid Java syntax.

---

## Initialization

```java
int[] arr = {10, 20, 30};
```

or

```java
int[] arr = new int[5];
```

Default values:

```text
int      → 0
long     → 0
float    → 0.0
double   → 0.0
boolean  → false
char     → '\u0000'
Reference → null
```

### Important

```java
int[] arr = new int[5];
```

creates an array containing **5 elements**, with valid indexes:

```text
0 1 2 3 4
```

---

# 5. Array Length

Java array uses the `length` property.

```java
int[] arr = {10, 20, 30};

System.out.println(arr.length);
```

Output:

```text
3
```

### Important Exam Trap

Array:

```java
arr.length
```

ArrayList:

```java
list.size()
```

String:

```java
str.length()
```

> Array uses `length`, not `length()`.

---

# 6. Accessing an Array Element

```java
int[] arr = {10, 20, 30, 40};

System.out.println(arr[2]);
```

Output:

```text
30
```

Time Complexity:

```text
O(1)
```

Because the index directly identifies the element location.

---

# 7. Updating an Element

```java
arr[2] = 100;
```

Before:

```text
10  20  30  40
```

After:

```text
10  20  100  40
```

Time Complexity:

```text
O(1)
```

---

# 8. Array Traversal

## Normal For Loop

```java
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```

## Enhanced For Loop

```java
for (int value : arr) {
    System.out.println(value);
}
```

Time Complexity:

```text
O(n)
```

---

# 9. Searching in Array

## Linear Search

Checks elements one by one.

```java
for (int i = 0; i < arr.length; i++) {
    if (arr[i] == target) {
        System.out.println("Found");
        break;
    }
}
```

Complexity:

```text
Best Case    → O(1)
Average Case → O(n)
Worst Case   → O(n)
```

### Important

> Linear Search does **not require a sorted array**.

---

# 10. Binary Search

Binary Search repeatedly divides the search space into two halves.

Example:

```text
10  20  30  40  50  60  70
             ↑
           Middle
```

Complexity:

```text
Best Case    → O(1)
Average Case → O(log n)
Worst Case   → O(log n)
```

### Important Condition

Binary Search normally requires the array to be **sorted**.

```java
Arrays.binarySearch(arr, target);
```

### Exam Point

```text
Linear Search  → O(n)
Binary Search  → O(log n)
```

---

# 11. Array Time Complexity

| Operation           | Time Complexity |
| ------------------- | --------------: |
| Access              |            O(1) |
| Update              |            O(1) |
| Traversal           |            O(n) |
| Linear Search       |            O(n) |
| Binary Search       |        O(log n) |
| Insert at Beginning |            O(n) |
| Insert in Middle    |            O(n) |
| Delete at Beginning |            O(n) |
| Delete in Middle    |            O(n) |

### Why Insert/Delete is O(n)?

Because elements may need to be shifted.

```text
10 20 30 40

Insert 5

5 10 20 30 40
```

---

# 12. Advantages of Array

### 1. Fast Random Access

```java
arr[index]
```

Time:

```text
O(1)
```

### 2. Simple

Easy to declare, access and traverse.

### 3. Memory Efficient

Compared with many dynamic data structures, arrays have relatively low structural overhead.


### 4. Cache Friendly

Sequential access can benefit from CPU cache locality.
Cache Friendly মানে হলো, Array-এর data যেহেতু memory-তে সাধারণত পরপর (sequentially) থাকে, তাই CPU খুব দ্রুত পরের data access করতে পারে।

### 5. Useful for Algorithms

Arrays are commonly used in:

* Searching
* Sorting
* Two Pointer
* Sliding Window
* Prefix Sum
* Dynamic Programming
* Matrix problems
* Heap
* Graph representation

---

# 13. Disadvantages of Array

### 1. Fixed Size

Java arrays cannot be resized after creation.

```java
int[] arr = new int[5];
```

The size remains `5`.

### 2. Insertion Can Be Expensive

Insertion in the beginning or middle may require shifting.

```text
O(n)
```

### 3. Deletion Can Be Expensive

Deletion in the beginning or middle may require shifting.

```text
O(n)
```

### 4. Possible Unused Space

If a large array is allocated but only a few positions are used, some allocated memory may remain unused.

---

# 14. Array vs ArrayList

| Feature              | Array | ArrayList    |
| -------------------- | ----- | ------------ |
| Size                 | Fixed | Dynamic      |
| Access               | O(1)  | O(1) average |
| Primitive Types      | Yes   | No           |
| Resize               | No    | Yes          |
| Collection Framework | No    | Yes          |
| Memory Overhead      | Lower | Higher       |

Example:

```java
int[] arr = new int[5];
```

```java
ArrayList<Integer> list = new ArrayList<>();
```

### Important

`ArrayList` stores objects, so primitive values use wrapper classes:

```java
ArrayList<Integer>
ArrayList<Double>
ArrayList<Character>
```

---

# 15. Java Array Utility Methods

Import:

```java
import java.util.Arrays;
```

## Sort

```java
Arrays.sort(arr);
```

Average/worst-case complexity for primitive array sorting is implementation-dependent; for common exam preparation, remember:

```text
Arrays.sort() → Sorting
```

Do not assume every Java sorting implementation has the same complexity.

---

## Binary Search

```java
Arrays.binarySearch(arr, 20);
```

> Array should be sorted for meaningful binary-search behavior.

---

## Copy

```java
Arrays.copyOf(arr, 10);
```

---

## Print

```java
System.out.println(Arrays.toString(arr));
```

---

## Compare

```java
Arrays.equals(arr1, arr2);
```

---

# 16. Important Array Algorithms

## Basic Problems

* Find Maximum
* Find Minimum
* Find Sum
* Reverse Array
* Count Even/Odd
* Find Duplicate
* Find Missing Number
* Find Second Largest

## Searching

* Linear Search
* Binary Search

## Sorting

* Bubble Sort
* Selection Sort
* Insertion Sort
* Merge Sort
* Quick Sort

## Important Techniques

* Two Pointer
* Sliding Window
* Prefix Sum
* Binary Search
* Kadane's Algorithm

---

# 17. Important Complexity Questions

### Array Access

```text
O(1)
```

### Array Update

```text
O(1)
```

### Array Traversal

```text
O(n)
```

### Linear Search

```text
O(n)
```

### Binary Search

```text
O(log n)
```

### Insert at Beginning

```text
O(n)
```

### Delete at Beginning

```text
O(n)
```

---

# 18. Important Government Job MCQ Facts

### Q1. What is the first index of an array in Java?

```text
0
```

### Q2. What is the last index of an array of size `n`?

```text
n - 1
```

### Q3. What is the time complexity of array access?

```text
O(1)
```

### Q4. What is the time complexity of traversing an array?

```text
O(n)
```

### Q5. What is the worst-case complexity of Linear Search?

```text
O(n)
```

### Q6. What is the worst-case complexity of Binary Search?

```text
O(log n)
```

### Q7. Does Binary Search require sorted data?

```text
Yes
```

### Q8. Can a Java array change its size after creation?

```text
No
```

### Q9. Which Java collection provides a resizable array?

```text
ArrayList
```

### Q10. Which property gives the size of a Java array?

```text
length
```

### Q11. Does Array use `length()`?

```text
No
```

Correct:

```java
arr.length
```

### Q12. What happens if an invalid array index is accessed?

```text
ArrayIndexOutOfBoundsException
```

Example:

```java
int[] arr = {10, 20, 30};

System.out.println(arr[3]);
```

Result:

```text
ArrayIndexOutOfBoundsException
```

---

# 19. Important Java Array MCQ Traps

## Trap 1: `length` vs `length()`

```java
arr.length       // Array
str.length()     // String
list.size()      // ArrayList
```

---

## Trap 2: Array Index

```text
Array size = 5

Valid indexes:
0, 1, 2, 3, 4
```

Not:

```text
1, 2, 3, 4, 5
```

---

## Trap 3: Default Value

```java
int[] arr = new int[3];
```

Result:

```text
0 0 0
```

---

## Trap 4: Invalid Index

```java
int[] arr = new int[3];

arr[3] = 10;
```

Invalid because valid indexes are:

```text
0, 1, 2
```

Exception:

```text
ArrayIndexOutOfBoundsException
```

---

## Trap 5: Array Size

```java
int[] arr = new int[10];
```

Number of elements:

```text
10
```

Last index:

```text
9
```

---

# 20. Array vs Linked List

| Feature          | Array          | Linked List              |
| ---------------- | -------------- | ------------------------ |
| Access           | O(1)           | O(n)                     |
| Search           | O(n)           | O(n)                     |
| Insert Beginning | O(n)           | O(1)*                    |
| Delete Beginning | O(n)           | O(1)*                    |
| Memory           | Lower overhead | Extra node/link overhead |
| Random Access    | Fast           | Slow                     |
| Size             | Fixed          | Dynamic                  |

`*` Assuming the required node/reference is already available.

### Remember

```text
Array       → Fast Access
Linked List → Easy Insert/Delete
```

---

# 21. Array Important Formula

For an array with `n` elements:

```text
First Index = 0
Last Index  = n - 1
```

If an element starts at address `Base Address` and each element occupies `W` bytes:

```text
Address of A[i] = Base Address + (i × W)
```

### Example

```text
Base Address = 1000
W = 4 bytes
i = 3
```

```text
Address = 1000 + (3 × 4)
        = 1012
```

This explains why array index access can be performed in:

```text
O(1)
```

---

# 22. Quick Revision

```text
ARRAY
│
├── Linear Data Structure
├── Index Based
├── First Index = 0
├── Last Index = n - 1
├── Fixed Size
│
├── Access         → O(1)
├── Update         → O(1)
├── Traversal      → O(n)
├── Linear Search  → O(n)
├── Binary Search  → O(log n)
├── Insert         → O(n)
└── Delete         → O(n)
```

---

# 23. One-Minute Revision for Exam

```text
Array
→ Linear data structure

Index
→ Starts from 0

Last Index
→ n - 1

Access
→ O(1)

Update
→ O(1)

Traversal
→ O(n)

Linear Search
→ O(n)

Binary Search
→ O(log n)
→ Requires sorted data

Insert/Delete
→ O(n) in beginning/middle

Java Array
→ Fixed size

Array Size
→ arr.length

ArrayList Size
→ list.size()

String Length
→ str.length()

Invalid Index
→ ArrayIndexOutOfBoundsException

Resizable Array in Java
→ ArrayList
```

---

# 24. Most Important for Bangladesh IT Government Jobs

For **Programmer / Assistant Programmer / ICT Officer / Senior Officer (IT) / Officer (IT)** exams, prioritize these Array topics:

### ⭐ Very High Priority

1. Array definition
2. Indexing
3. First and last index
4. Array declaration and initialization
5. Array `length`
6. Default values
7. Access complexity — `O(1)`
8. Linear Search — `O(n)`
9. Binary Search — `O(log n)`
10. Sorted array requirement for Binary Search
11. Insertion and deletion complexity
12. Array vs ArrayList
13. 1D / 2D / Multidimensional array
14. Jagged array
15. `ArrayIndexOutOfBoundsException`

### ⭐ High Priority

16. Arrays vs Linked List
17. `Arrays.sort()`
18. `Arrays.binarySearch()`
19. `Arrays.copyOf()`
20. `Arrays.toString()`
21. `Arrays.equals()`
22. Array default values
23. Memory/address calculation
24. Two Pointer
25. Sliding Window
26. Prefix Sum
27. Kadane's Algorithm

---

# Final Remember

> **Array = Index + Fast Access + Fixed Size**

```text
Access       → O(1)
Update       → O(1)
Search       → O(n)
Binary Search→ O(log n)
Insert       → O(n)
Delete       → O(n)
```
# Linked List — IT Government Job Preparation

## 1. What is a Linked List?

A **Linked List** is a linear data structure where elements are stored in separate objects called **nodes**.

Each node generally contains:

1. **Data**
2. **Reference/Link** to the next node

```text
Node
┌──────────┬──────────┐
│  Data    │  Next    │
└──────────┴──────────┘
```

Example:

```text
10 → 20 → 30 → 40 → null
```

Here:

```text
10 → First Node
20 → Second Node
30 → Third Node
40 → Last Node
null → End of List
```

### Important

> Unlike an array, Linked List elements are not required to be stored in contiguous memory locations.

---

# 2. Structure of a Node

A simple Java Node:

```java
class Node {
    int data;
    Node next;

    Node(int data) {
        this.data = data;
        this.next = null;
    }
}
```

Example:

```java
Node first = new Node(10);
Node second = new Node(20);

first.next = second;
```

Structure:

```text
first
  ↓
┌──────┬──────┐
│  10  │  ────────┐
└──────┴──────┘   │
                   ↓
              ┌──────┬──────┐
              │  20  │ null │
              └──────┴──────┘
```

---

# 3. Important Terminology

| Term     | Meaning                                          |
| -------- | ------------------------------------------------ |
| Node     | Stores data and link/reference                   |
| Head     | First node                                       |
| Tail     | Last node                                        |
| Next     | Reference to next node                           |
| Previous | Reference to previous node in doubly linked list |
| Null     | Indicates end of list                            |

Example:

```text
Head
 ↓
10 → 20 → 30 → 40 → null
                      ↑
                     Tail
```

### Most Important

> **Head points to the first node.**

> **Tail points to the last node.**

---

# 4. Features of Linked List

* Linear data structure
* Dynamic size
* Consists of nodes
* Nodes contain data and references
* Does not require contiguous memory
* Sequential access
* Easy insertion and deletion
* Random access is not efficient
* Uses extra memory for references

---

# 5. Types of Linked List

There are mainly four important types:

```text
Linked List
│
├── Singly Linked List
├── Doubly Linked List
├── Circular Singly Linked List
└── Circular Doubly Linked List
```

---

# 6. Singly Linked List

Each node contains:

```text
Data + Next
```

Structure:

```text
10 → 20 → 30 → 40 → null
```

Java:

```java
class Node {
    int data;
    Node next;
}
```

### Diagram

```text
┌─────┬──────┐    ┌─────┬──────┐
│ 10  │  ─────────→ 20  │  ─────────→ ...
└─────┴──────┘    └─────┴──────┘
```

### Important

> Singly Linked List can move only in the **forward direction**.

---

# 7. Doubly Linked List

Each node contains:

```text
Previous + Data + Next
```

Structure:

```text
null ← 10 ⇄ 20 ⇄ 30 ⇄ 40 → null
```

Java:

```java
class Node {
    int data;
    Node prev;
    Node next;
}
```

### Important

> Doubly Linked List supports traversal in **both directions**.

---

# 8. Circular Singly Linked List

In a Circular Linked List, the last node points back to the first node.

```text
     ┌──────────────────────┐
     ↓                      │
10 → 20 → 30 → 40 ─────────┘
```

There is no `null` at the end.

```text
Last.next = Head
```

### Important

> Circular Singly Linked List forms a loop.

---

# 9. Circular Doubly Linked List

Both directions form a circle.

```text
      ┌─────────────────────┐
      ↓                     │
10 ⇄ 20 ⇄ 30 ⇄ 40
↑                     ↓
└─────────────────────┘
```

Each node has:

```text
Previous + Data + Next
```

---

# 10. Linked List vs Array

| Feature                | Array                               | Linked List                 |
| ---------------------- | ----------------------------------- | --------------------------- |
| Memory                 | Sequential/contiguous storage model | Nodes can be non-contiguous |
| Size                   | Fixed                               | Dynamic                     |
| Random Access          | O(1)                                | O(n)                        |
| Search                 | O(n)                                | O(n)                        |
| Insert Beginning       | O(n)                                | O(1)*                       |
| Delete Beginning       | O(n)                                | O(1)*                       |
| Extra Reference Memory | No                                  | Yes                         |
| Cache Locality         | Better generally                    | Usually poorer              |
| Memory Allocation      | Usually one array allocation        | Node-by-node allocation     |

`*` Assuming the required head/reference is already available.

### Remember

```text
Array
→ Fast Random Access

Linked List
→ Efficient Insert/Delete at known positions
```

---

# 11. Linked List Time Complexity

For a typical singly linked list:

| Operation                  | Time Complexity |
| -------------------------- | --------------: |
| Access by Index            |            O(n) |
| Search                     |            O(n) |
| Insert at Beginning        |            O(1) |
| Delete at Beginning        |            O(1) |
| Insert at End              |           O(n)* |
| Delete at End              |            O(n) |
| Insert After Known Node    |            O(1) |
| Delete After/At Known Node |           O(1)* |
| Traversal                  |            O(n) |

`*` Complexity can change if the implementation maintains a tail pointer or the required node/reference is already available.

---

# 12. Why Random Access is O(n)?

Suppose:

```text
10 → 20 → 30 → 40 → 50
```

To access `40`, we cannot directly jump to index `3`.

We must traverse:

```text
10 → 20 → 30 → 40
```

Therefore:

```text
Access by Index → O(n)
```

### Array vs Linked List

```text
Array:

arr[3]
  ↓
Direct Access → O(1)
```

```text
Linked List:

Head
 ↓
10 → 20 → 30 → 40
               ↑
           Traverse
           
→ O(n)
```

---

# 13. Insertion at Beginning

Original:

```text
10 → 20 → 30
```

Insert `5`:

```text
5 → 10 → 20 → 30
```

Java idea:

```java
newNode.next = head;
head = newNode;
```

Complexity:

```text
O(1)
```

---

# 14. Insertion at End

Original:

```text
10 → 20 → 30
```

Insert `40`:

```text
10 → 20 → 30 → 40
```

Without a tail pointer, we need to traverse to the last node.

Complexity:

```text
O(n)
```

With a maintained tail pointer:

```text
O(1)
```

---

# 15. Deletion from Beginning

Original:

```text
10 → 20 → 30
```

Delete first node:

```text
20 → 30
```

Java:

```java
head = head.next;
```

Complexity:

```text
O(1)
```

---

# 16. Searching in Linked List

Example:

```text
10 → 20 → 30 → 40
```

Search for `30`.

We check:

```text
10 → 20 → 30
```

Complexity:

```text
Best Case    → O(1)
Average Case → O(n)
Worst Case   → O(n)
```

---

# 17. Traversal

Java:

```java
Node current = head;

while (current != null) {
    System.out.println(current.data);
    current = current.next;
}
```

Complexity:

```text
O(n)
```

---

# 18. Basic Singly Linked List Implementation

```java
class Node {

    int data;
    Node next;

    Node(int data) {
        this.data = data;
        this.next = null;
    }
}
```

Linked List:

```java
class LinkedList {

    Node head;

    void add(int data) {

        Node newNode = new Node(data);

        if (head == null) {
            head = newNode;
            return;
        }

        Node current = head;

        while (current.next != null) {
            current = current.next;
        }

        current.next = newNode;
    }
}
```

---

# 19. Important Linked List Operations

Common operations:

```text
1. Insert
2. Delete
3. Search
4. Traverse
5. Reverse
```

---

# 20. Reverse a Linked List

Original:

```text
10 → 20 → 30 → null
```

After Reverse:

```text
30 → 20 → 10 → null
```

Typical Java approach:

```java
Node previous = null;
Node current = head;

while (current != null) {

    Node next = current.next;

    current.next = previous;

    previous = current;
    current = next;
}

head = previous;
```

Complexity:

```text
Time  → O(n)
Space → O(1)
```

### Important Exam Point

> Iterative Linked List reversal can be done in **O(n) time and O(1) extra space**.

---

# 21. Advantages of Linked List

### 1. Dynamic Size

Linked List can grow and shrink dynamically.

### 2. Easy Insertion

Insertion at the beginning is:

```text
O(1)
```

### 3. Easy Deletion

Deletion at the beginning is:

```text
O(1)
```

### 4. No Contiguous Memory Requirement

Nodes do not need to be stored next to each other in memory.

### 5. Useful for Dynamic Data

Useful when the number of elements changes frequently.

---

# 22. Disadvantages of Linked List

### 1. Slow Random Access

Accessing an element by index:

```text
O(n)
```

### 2. Extra Memory

Each node needs one or more references.

Example:

```text
Data + Next
```

Doubly linked list:

```text
Previous + Data + Next
```

### 3. Poor Cache Locality

Nodes may be scattered in memory.

### 4. More Complex

Pointer/reference manipulation can introduce bugs.

### 5. Reverse Traversal

Singly Linked List cannot directly move backward.

---

# 23. Singly vs Doubly Linked List

| Feature            | Singly  | Doubly       |
| ------------------ | ------- | ------------ |
| Next Reference     | Yes     | Yes          |
| Previous Reference | No      | Yes          |
| Forward Traversal  | Yes     | Yes          |
| Backward Traversal | No      | Yes          |
| Memory Usage       | Lower   | Higher       |
| Implementation     | Simpler | More complex |

Remember:

```text
Singly
→ next

Doubly
→ prev + next
```

---

# 24. Singly vs Circular Linked List

| Feature   | Singly         | Circular                          |
| --------- | -------------- | --------------------------------- |
| Last Node | Points to null | Points to first node              |
| End       | null           | No null at end                    |
| Structure | Linear         | Circular                          |
| Traversal | Stops at null  | Stops when reaching starting node |

---

# 25. Important Applications

Linked Lists are commonly used in:

* Stack implementation
* Queue implementation
* Hash table chaining
* Graph adjacency lists
* Browser history
* Undo/Redo systems
* Music playlists
* Memory management concepts

---

# 26. Java Collections Related to Linked List

Java provides:

```java
import java.util.LinkedList;
```

Example:

```java
LinkedList<Integer> list = new LinkedList<>();

list.add(10);
list.add(20);
list.add(30);
```

Output:

```text
10 → 20 → 30
```

Java's `LinkedList` implements:

```text
List
Deque
Queue
```

and is implemented as a **doubly linked list**.

---

# 27. LinkedList vs ArrayList in Java

| Feature             | ArrayList       | LinkedList         |
| ------------------- | --------------- | ------------------ |
| Internal Structure  | Resizable array | Doubly linked list |
| Random Access       | Fast            | Slow               |
| `get(index)`        | O(1)            | O(n)               |
| Memory              | Lower           | Higher             |
| Insert at Beginning | O(n)            | O(1)               |
| Remove First        | O(n)            | O(1)               |
| Implements List     | Yes             | Yes                |
| Implements Deque    | No              | Yes                |

### Important

> `LinkedList` is **not automatically faster** than `ArrayList`. For frequent random access, `ArrayList` is usually better.

---

# 28. Important Government Job MCQ Questions

### Q1. What is a Linked List?

A linear data structure consisting of nodes connected through references.

### Q2. What does a node contain?

```text
Data + Reference
```

### Q3. What does the Head represent?

```text
First node
```

### Q4. What does the last node point to in a normal singly linked list?

```text
null
```

### Q5. Time complexity of accessing an element by index?

```text
O(n)
```

### Q6. Time complexity of insertion at the beginning?

```text
O(1)
```

### Q7. Time complexity of deletion at the beginning?

```text
O(1)
```

### Q8. Does Linked List require contiguous memory?

```text
No
```

### Q9. Which Linked List supports forward and backward traversal?

```text
Doubly Linked List
```

### Q10. In Circular Linked List, where does the last node point?

```text
First node / Head
```

### Q11. Which Linked List uses `prev` and `next`?

```text
Doubly Linked List
```

### Q12. Which Java collection is implemented as a doubly linked list?

```text
LinkedList
```

### Q13. What is the search complexity in a Linked List?

```text
O(n)
```

### Q14. What is the extra memory requirement of a node?

```text
Reference/link storage
```

### Q15. Can a singly linked list traverse backward directly?

```text
No
```

---

# 29. Important MCQ Traps

## Trap 1: Random Access

```text
Array       → O(1)
Linked List → O(n)
```

---

## Trap 2: First Insertion

If inserting at the beginning:

```text
Array       → O(n)
Linked List → O(1)
```

---

## Trap 3: Last Node

Normal Singly Linked List:

```text
Last.next = null
```

Circular Linked List:

```text
Last.next = Head
```

---

## Trap 4: Doubly Linked List

Doubly Linked List has:

```text
prev + data + next
```

---

## Trap 5: Java LinkedList

```java
LinkedList<Integer> list = new LinkedList<>();
```

Java's `LinkedList` is a:

```text
Doubly Linked List
```

---

# 30. Important Complexity Comparison

```text
                 Array       Linked List
------------------------------------------------
Access           O(1)        O(n)
Search           O(n)        O(n)
Insert Beginning O(n)        O(1)
Delete Beginning O(n)        O(1)
Insert Middle    O(n)        O(1)*
Delete Middle    O(n)        O(1)*
```

`*` For Linked List, the relevant position/node reference must already be known; finding it can take `O(n)`.

---

# 31. Array vs Linked List — One Line

```text
Array
→ Fast Access

Linked List
→ Flexible Size + Efficient Insert/Delete
```

---

# 32. Quick Revision

```text
Linked List
│
├── Linear Data Structure
├── Node Based
├── Dynamic Size
├── Non-contiguous Nodes
│
├── Singly
│   └── next
│
├── Doubly
│   └── prev + next
│
├── Circular
│   └── Last → Head
│
├── Access       → O(n)
├── Search       → O(n)
├── Insert Head  → O(1)
├── Delete Head  → O(1)
└── Traversal    → O(n)
```

---

# 33. One-Minute Revision for Exam

```text
Linked List
→ Node-based linear data structure

Node
→ Data + Reference

Head
→ First node

Tail
→ Last node

Singly
→ next

Doubly
→ prev + next

Circular
→ Last points to Head

Access
→ O(n)

Search
→ O(n)

Insert at Beginning
→ O(1)

Delete at Beginning
→ O(1)

Normal Singly Last Node
→ next = null

Circular Last Node
→ next = Head

Java LinkedList
→ Doubly Linked List

Java LinkedList
→ List + Deque + Queue
```

---

# 34. Most Important for Bangladesh IT Government Jobs

For **Programmer / Assistant Programmer / ICT Officer / Senior Officer (IT) / Officer (IT)** preparation, prioritize:

### ⭐ Very High Priority

1. Linked List definition
2. Node
3. Head and Tail
4. Singly Linked List
5. Doubly Linked List
6. Circular Linked List
7. Array vs Linked List
8. Access complexity
9. Search complexity
10. Insert/Delete complexity
11. `null` vs circular connection
12. Java `LinkedList`

### ⭐ High Priority

13. Reverse Linked List
14. Linked List traversal
15. ArrayList vs LinkedList
16. Stack using Linked List
17. Queue using Linked List
18. Doubly Linked List structure
19. Circular Linked List applications
20. Time and space complexity

---

# Final Remember

> **Linked List = Nodes + References + Dynamic Size**

```text
Array
→ Fast Access
→ O(1)

Linked List
→ Sequential Access
→ O(n)

Linked List Insert/Delete at Head
→ O(1)

Singly
→ next

Doubly
→ prev + next

Circular
→ Last → Head
```


