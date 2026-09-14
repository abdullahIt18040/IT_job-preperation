# Queue

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
