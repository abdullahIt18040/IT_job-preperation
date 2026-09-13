### Data Structure

### What is Data Structure?
```
A Data Structure is a way of organizing, storing, and managing data in a computer so that we can use the data efficiently.

In simple words:

Data Structure = A way to store and organize data so that operations like access, search, insertion, deletion, and update can be performed efficiently.

Example

Suppose we have student marks:

80, 75, 90, 65, 88

We can store them in an Array:

int[] marks = {80, 75, 90, 65, 88};

Now we can easily access:

marks[2]

Result:

90

So, Array is a Data Structure.

Types of Data Structure

Data Structures are mainly divided into two types:

                    Data Structure
                         │
             ┌───────────┴───────────┐
             │                       │
         Linear                  Non-Linear
       Data Structure           Data Structure
             │                       │
      ┌──────┼──────┐          ┌─────┴─────┐
      │      │      │          │           │
    Array  Stack  Queue       Tree        Graph
             │
       Linked List
1. Linear Data Structure

In a Linear Data Structure, data elements are arranged sequentially, one after another.

Example:

10 → 20 → 30 → 40 → 50

The elements follow a linear sequence.

Main Linear Data Structures
A. Array

Stores elements using indexes.

Index:  0   1   2   3
       ┌───┬───┬───┬───┐
Data:  │10 │20 │30 │40 │
       └───┴───┴───┴───┘

Example:

int[] arr = {10, 20, 30, 40};

Access: O(1)
2. Non-Linear Data Structure

In a Non-Linear Data Structure, elements are not arranged sequentially.

They can have hierarchical or network relationships.

Main examples:

Tree
Graph
A. Tree

A Tree represents hierarchical data.

Example:

              10
            /    \
           5      20
         /  \    /  \
        2    7  15   30

Here:

10 → Root
5,20 → Children
2,7,15,30 → Leaf nodes

Types of Tree:

Binary Tree
Binary Search Tree (BST)
AVL Tree
Red-Black Tree
B-Tree
Trie

Real-world examples:

File system
Database indexes
HTML DOM
Organization hierarchy
B. Graph

A Graph represents relationships between entities.

Example:

       A
      / \
     B---C
      \ /
       D

Here:

A, B, C, D = Vertices/Nodes
Connections = Edges

Real-world examples:

Google Maps
Social networks
Computer networks
Airline routes

Important algorithms:

BFS
DFS
Dijkstra
Bellman-Ford
Floyd-Warshall
Prim
Kruskal
3. Another Important Classification

Data Structures can also be classified as:

Static Data Structure

Size generally cannot change after creation.

Example:

Array
int[] arr = new int[10];

The size is 10.

Dynamic Data Structure

Size can grow or shrink during program execution.

Examples:

Linked List
Stack
Queue
Tree
Graph

Java examples:

ArrayList
LinkedList
HashMap
HashSet
PriorityQueue
4. Important Java Data Structures

Since you are working with Java/Spring Boot, these are especially important:

Data Structure	Java Collection
Array	int[], String[]
Dynamic Array	ArrayList
Linked List	LinkedList
Stack	Deque / Stack
Queue	Queue
Hash Table	HashMap
Set	HashSet
Sorted Set	TreeSet
Priority Queue	PriorityQueue
5. Complete Picture
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

And another classification:

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
⭐ Interview Definition

A data structure is a systematic way of organizing and storing data in memory so that data can be accessed and modified efficiently.

সবচেয়ে গুরুত্বপূর্ণভাবে মনে রাখুন:

Linear → Array, Linked List, Stack, Queue

Non-Linear → Tree, Graph

Static → Array

Dynamic → Linked List, Stack, Queue, Tree, Graph
```
