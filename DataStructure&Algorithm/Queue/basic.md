# Queue or implemetation Linklist 
## Enque and Dequeue OPeration
<img width="618" height="266" alt="image" src="https://github.com/user-attachments/assets/4837475b-2a81-4a1a-8255-36b3c755c438" />


## 1. What is a Queue?

A **Queue** is a linear data structure that follows:

> **FIFO — First In, First Out**

যে element আগে ঢোকে, সেটি আগে বের হয়।

Example:

```text
Enqueue → [10, 20, 30] → Dequeue
                         ↓
                        10
```

---

## 2. Basic Operations

### Enqueue

Queue-এর **rear/end**-এ element যোগ করা।

```text
Enqueue(10)
Enqueue(20)
Enqueue(30)

Queue:
[10, 20, 30]
```

### Dequeue

Queue-এর **front** থেকে element remove করা।

```text
[10, 20, 30]
 ↓
Dequeue()

Result = 10
```

Queue becomes:

```text
[20, 30]
```

### Peek / Front

Front element দেখা কিন্তু remove না করা।

```text
[20, 30]

Peek() → 20
```

### isEmpty

Queue empty কিনা check করে।

```text
isEmpty() → true / false
```

---

# 3. Queue Structure

```text
             Queue
               ↓

Front                    Rear
  ↓                        ↓
[10] → [20] → [30] → [40]
```

* **Front** → এখান থেকে element বের হয়
* **Rear** → এখানে নতুন element যোগ হয়

---

# 4. Queue Example

Real-life example:

```text
People waiting in a line
```

```text
Person A → Person B → Person C
   ↓
First                    Last
```

A আগে এসেছে, তাই A আগে service পাবে।

This is:

```text
FIFO
```

---

# 5. Queue Complexity

For a proper Queue implementation:

| Operation |   Time |
| --------- | -----: |
| Enqueue   | `O(1)` |
| Dequeue   | `O(1)` |
| Peek      | `O(1)` |
| isEmpty   | `O(1)` |

---

# 6. Types of Queue

Important types:

```text
1. Simple Queue
2. Circular Queue
3. Priority Queue
4. Deque
```

---

# 7. Circular Queue

A **Circular Queue** is a queue where the last position is connected back to the first position.
```text


```
<img width="758" height="289" alt="image" src="https://github.com/user-attachments/assets/e1d3d090-b36d-42b5-ad65-8f84c93f2ed8" />
It helps utilize unused spaces efficiently.

### Important

```text
Front → Remove
Rear  → Insert
```

---

# 8. Priority Queue

In a **Priority Queue**, elements are removed according to their **priority**, not simply FIFO order.

Example:

```text
Element     Priority
A              3
B              1
C              2
```

If smaller number means higher priority:

```text
B → C → A
```

Java provides:

```java
PriorityQueue<Integer> pq = new PriorityQueue<>();

pq.add(30);
pq.add(10);
pq.add(20);

System.out.println(pq.poll()); // 10
```

---

# 9. Deque

**Deque = Double Ended Queue**

Insertion and deletion can happen from **both ends**.

```text
Front                    Rear
  ↓                        ↓
[10] → [20] → [30] → [40]
  ↑                        ↑
Insert/Delete          Insert/Delete
```

Java:

```java
Deque<Integer> deque = new ArrayDeque<>();
```

---

# 10. Queue vs Stack

| Feature   | Queue        | Stack           |
| --------- | ------------ | --------------- |
| Principle | FIFO         | LIFO            |
| Insert    | Rear         | Top             |
| Remove    | Front        | Top             |
| Example   | Waiting line | Stack of plates |

### Memory Trick

```text
Queue → FIFO
Stack → LIFO
```

---

# 11. Queue in Java

Using `Queue` interface:

```java
Queue<Integer> queue = new LinkedList<>();

queue.offer(10);
queue.offer(20);
queue.offer(30);

System.out.println(queue.peek()); // 10

System.out.println(queue.poll()); // 10
```

### Common Methods

```text
offer() → Insert
poll()  → Remove + return front
peek()  → Return front without removing
isEmpty() → Check empty
```

---

# 12. Important Interview Points

```text
Queue
→ FIFO

Enqueue
→ Insert at Rear

Dequeue
→ Remove from Front

Peek
→ See Front element

Circular Queue
→ Reuses empty spaces

Priority Queue
→ Highest priority element first

Deque
→ Insert/Delete from both ends
```

## Easy Memory Trick

```text
        Queue

Insert → REAR
           ↓
[10] [20] [30]
 ↑
FRONT
 ↓
Remove

FIFO → First In, First Out
```
# Queue — Enqueue and Dequeue

A **Queue** follows the **FIFO (First In, First Out)** principle.

```text
First In → First Out
```

```text
Front                         Rear
  ↓                             ↓
[10] → [20] → [30] → [40]
```

---

# 1. Enqueue Operation

**Enqueue** means inserting a new element into the Queue.

The new element is always inserted at the **Rear**.

## Rule

```text
Enqueue → Insert at Rear
```

```text
If Queue is Full
    → Overflow
Otherwise
    → Add element at Rear
```

## Algorithm

```text
ENQUEUE(Queue, item)

1. If REAR == MAX - 1
       Print "Queue Overflow"
       Return

2. If FRONT == -1
       FRONT = 0

3. REAR = REAR + 1

4. Queue[REAR] = item
```

## Example

Before:

```text
Front                 Rear
  ↓                     ↓
[10] → [20] → [30]
```

Perform:

```text
ENQUEUE(40)
```

After:

```text
Front                        Rear
  ↓                            ↓
[10] → [20] → [30] → [40]
```

## Time Complexity

```text
Enqueue = O(1)
```

---

# 2. Dequeue Operation

**Dequeue** means removing an element from the Queue.

The element is always removed from the **Front**.

## Rule

```text
Dequeue → Remove from Front
```

```text
If Queue is Empty
    → Underflow
Otherwise
    → Remove element from Front
```

## Algorithm

```text
DEQUEUE(Queue)

1. If FRONT == -1 OR FRONT > REAR
       Print "Queue Underflow"
       Return

2. item = Queue[FRONT]

3. FRONT = FRONT + 1

4. Return item
```

## Example

Before:

```text
Front                        Rear
  ↓                            ↓
[10] → [20] → [30] → [40]
```

Perform:

```text
DEQUEUE()
```

Removed:

```text
10
```

After:

```text
Front                 Rear
  ↓                     ↓
[20] → [30] → [40]
```

## Time Complexity

```text
Dequeue = O(1)
```

---

# 3. Enqueue vs Dequeue

| Operation | Action | Position | Complexity |
| --------- | ------ | -------- | ---------: |
| Enqueue   | Insert | Rear     |     `O(1)` |
| Dequeue   | Remove | Front    |     `O(1)` |

---

# 4. Important Terms

### Overflow

Queue full থাকা অবস্থায় নতুন element insert করতে গেলে:

```text
Overflow
```

### Underflow

Queue empty থাকা অবস্থায় element remove করতে গেলে:

```text
Underflow
```

---

# 5. Easy Memory Trick

```text
ENQUEUE
   ↓
INSERT
   ↓
REAR
```

```text
DEQUEUE
   ↓
REMOVE
   ↓
FRONT
```

### Final Rule

> **Enqueue → Insert at Rear**
> **Dequeue → Remove from Front**
> **Both → O(1)**
> 
### dequeue algorithm explanation
```
এটা Array দিয়ে Queue-এর Dequeue operation। অর্থাৎ Queue থেকে একটি element বের করে/মুছে ফেলার algorithm।

মূল Rule

Dequeue → Remove/Delete from FRONT

ধরি:

Queue = [10, 20, 30, 40, _]
          ↑           ↑
        FRONT        REAR

FRONT = 0
REAR  = 3

এখন Dequeue করলে 10 বের হবে।

Line by Line Explanation
1. Check Queue Empty
If FRONT == -1 OR FRONT > REAR
    Print "Queue Underflow"
    Return

প্রথমে check করবে Queue-তে কোনো element আছে কি না।

Condition 1:
FRONT == -1

সাধারণত শুরুতে:

FRONT = -1
REAR = -1

মানে Queue empty।

Condition 2:
FRONT > REAR

ধরি:

FRONT = 4
REAR = 3

তাহলে:

FRONT > REAR
4 > 3

সত্য → Queue empty।

তাই:

Queue Underflow

Underflow = Empty Queue থেকে element remove করার চেষ্টা।

2. FRONT-এর elementটি item-এ রাখা
item = Queue[FRONT]

ধরি:

Queue = [10, 20, 30, 40, _]

FRONT = 0

তাহলে:

item = Queue[0]
     = 10

অর্থাৎ যে element-টি remove করব, সেটি আগে item variable-এ রাখছি।

item = 10
3. FRONT এক ধাপ সামনে নেওয়া
FRONT = FRONT + 1

আগে:

FRONT = 0

তাহলে:

FRONT = 0 + 1
      = 1

এখন 10 আর Queue-এর active অংশে নেই।

Queue = [10, 20, 30, 40, _]
          X   ↑
              FRONT

10 memory-তে থাকতে পারে, কিন্তু Queue-এর হিসেবে এটি আর available element নয়।

Active Queue এখন:

[20, 30, 40]
 ↑        ↑
FRONT    REAR
4. Removed item Return করা
Return item

আমরা Step 2-তে পেয়েছিলাম:

item = 10

তাই:

Return 10

অর্থাৎ Dequeue operation-এর result হলো 10।

পুরো Example

ধরি:

Queue = [10, 20, 30, 40, _]

FRONT = 0
REAR = 3
Dequeue()

Step 1:

FRONT == -1 OR FRONT > REAR

0 == -1 OR 0 > 3
False

তাই continue।

Step 2:

item = Queue[FRONT]
     = Queue[0]
     = 10

Step 3:

FRONT = FRONT + 1
      = 0 + 1
      = 1

Step 4:

Return item

Result:

10

Queue-এর active elements:

Queue = [10, 20, 30, 40, _]
             ↑        ↑
           FRONT     REAR

অর্থাৎ:

FRONT = 1
REAR = 3
এরপর আবার Dequeue করলে

এবার:

FRONT = 1

তাই:

item = Queue[1]
     = 20

তারপর:

FRONT = 1 + 1
      = 2

Return:

20

তারপর 30, তারপর 40 বের হবে।
```
### Enqueue Explanation 
```
এটা Array দিয়ে Queue-এর Enqueue operation—অর্থাৎ Queue-তে নতুন element যোগ করার algorithm।

আগে Queue-এর variable বুঝি

ধরি:

Queue = [10, 20, 30, _, _]

MAX = 5
FRONT = 0
REAR = 2

এখানে:

MAX = Queue-এর সর্বোচ্চ capacity
FRONT = প্রথম element-এর index
REAR = শেষ element-এর index
item = যে নতুন element যোগ করব
Algorithm Line by Line
1. Check Queue Full
If REAR == MAX - 1
    Print "Queue Overflow"
    Return

ধরি:

MAX = 5

তাহলে valid index:

0   1   2   3   4

সুতরাং শেষ index:

MAX - 1 = 5 - 1 = 4

যদি:

REAR == 4

তাহলে Queue পুরোপুরি full।

[10, 20, 30, 40, 50]
                    ↑
                  REAR

এখন নতুন element যোগ করার জায়গা নেই।

তাই:

Queue Overflow

Overflow = Full Queue-তে নতুন element ঢোকানোর চেষ্টা।

2. প্রথম element হলে FRONT সেট করা
If FRONT == -1
    FRONT = 0

শুরুতে যদি Queue empty থাকে:

FRONT = -1
REAR = -1

এখন আমরা প্রথম element 10 insert করতে চাই।

তখন:

FRONT == -1

সত্য।

তাই:

FRONT = 0

এখন:

FRONT = 0
REAR = -1
3. REAR এক ধাপ সামনে নেওয়া
REAR = REAR + 1

এটি নতুন element রাখার জন্য REAR-কে পরবর্তী position-এ নিয়ে যায়।

যদি:

REAR = 2

তাহলে:

REAR = 2 + 1
     = 3
4. নতুন item রাখা
Queue[REAR] = item

ধরি:

item = 40
REAR = 3

তাহলে:

Queue[3] = 40

Queue হবে:

Index:   0    1    2    3    4
        -------------------------
Queue: [10,  20,  30,  40,   _]
         ↑              ↑
       FRONT           REAR
পুরো Process Example

ধরি শুরুতে:

MAX = 5
FRONT = -1
REAR = -1
Queue = [_, _, _, _, _]

আমরা 10 Enqueue করব।

Step 1
REAR == MAX - 1
-1 == 4

False → Continue.

Step 2
FRONT == -1

True:

FRONT = 0
Step 3
REAR = REAR + 1
     = -1 + 1
     = 0
Step 4
Queue[REAR] = item
Queue[0] = 10

Final:

Queue = [10, _, _, _, _]

FRONT = 0
REAR  = 0
এরপর 20 Enqueue করলে

FRONT == -1 আর সত্য নয়।

REAR = 0 + 1 = 1
Queue[1] = 20

Result:

Queue = [10, 20, _, _, _]
          ↑    ↑
        FRONT REAR
```
