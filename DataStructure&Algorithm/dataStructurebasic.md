# Data Structure

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

