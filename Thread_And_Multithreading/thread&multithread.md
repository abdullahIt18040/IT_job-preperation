#proccess
<img width="746" height="389" alt="image" src="https://github.com/user-attachments/assets/5aa03526-59a3-4324-a7c9-56ab7d382528" />
# Creating Threads in Java

## 1. What is a Thread?

A **Thread** is a lightweight unit of execution within a program.

Java supports **Multithreading**, which allows multiple threads to execute tasks concurrently within a single process.

## 2. Ways to Create a Thread in Java

There are three common ways:

1. By extending the `Thread` class.
2. By implementing the `Runnable` interface.
3. By using a Lambda Expression (Java 8+).

---

## 3. Extending the Thread Class

Create a class that extends the `Thread` class and override its `run()` method.

### Example:

```java
class MyThread extends Thread {

    @Override
    public void run() {
        System.out.println("Thread is running...");
    }
}

public class Main {
    public static void main(String[] args) {

        MyThread t1 = new MyThread();

        t1.start();
    }
}
```

### Explanation:

- `extends Thread`: Inherits the Thread class.
- `run()`: Defines the task performed by the thread.
- `start()`: Starts a new thread and internally invokes `run()`.

**Important:** Always use `start()` to start a new thread, not directly `run()`.

---

## 4. Implementing the Runnable Interface

Create a class that implements the `Runnable` interface and override the `run()` method.

### Example:

```java
class MyTask implements Runnable {

    @Override
    public void run() {
        System.out.println("Thread is running...");
    }
}

public class Main {
    public static void main(String[] args) {

        MyTask task = new MyTask();

        Thread t1 = new Thread(task);

        t1.start();
    }
}
```

### Explanation:

- `Runnable`: An interface that defines a task.
- `run()`: Contains the task to execute.
- `new Thread(task)`: Creates a thread with the Runnable task.
- `start()`: Starts the new thread.

### Why use Runnable?

Java does not support multiple inheritance with classes.

By implementing `Runnable`, a class can also extend another class.

---

## 5. Using Lambda Expression (Java 8+)

We can create a thread without creating a separate class by using a Lambda Expression.

### Example:

```java
public class Main {
    public static void main(String[] args) {

        Thread t1 = new Thread(() -> {
            System.out.println("Thread is running...");
        });

        t1.start();
    }
}
```

**Explanation:**

- Lambda Expression provides a shorter way to implement the `Runnable` interface.
- No need to create a separate class.
- Useful for simple thread tasks.

---

## 6. Creating Multiple Threads

We can create multiple threads in a single program.

### Example:

```java
public class Main {
    public static void main(String[] args) {

        Thread t1 = new Thread(() -> {
            System.out.println("Thread 1 is running");
        });

        Thread t2 = new Thread(() -> {
            System.out.println("Thread 2 is running");
        });

        t1.start();
        t2.start();
    }
}
```

**Output:**

```text
Thread 1 is running
Thread 2 is running
```

**Note:** The execution order is not guaranteed. The thread scheduler decides which thread runs first.

---

## 7. Difference Between Thread and Runnable

| Thread | Runnable |
|---|---|
| Thread is a class. | Runnable is an interface. |
| Uses `extends`. | Uses `implements`. |
| Cannot extend another class. | Can extend another class. |
| Less flexible. | More flexible. |
| Task and thread are combined. | Task and thread are separated. |

**Recommendation:** Implementing `Runnable` is generally preferred because it separates task logic from thread management.

---

## 8. Difference Between start() and run()

| start() | run() |
|---|---|
| Starts a new thread. | Executes like a normal method when called directly. |
| Executes concurrently. | Direct invocation does not create a new thread. |
| Internally invokes run(). | Contains the task logic. |

### Example:

```java
Thread t1 = new Thread(() -> {
    System.out.println(Thread.currentThread().getName());
});

// Starts a new thread
t1.start();

// Direct method call (does not start a new thread)
t1.run();
```

---
# Multithreading in Java

## 1. What is Multithreading?

**Multithreading is the process of executing multiple threads concurrently within a single process.**

In simple words:

Multithreading allows a program to perform multiple tasks concurrently.

### Example

In a web browser:

- Thread 1: Handles user input.
- Thread 2: Loads web pages.
- Thread 3: Plays videos.
- Thread 4: Downloads files.

All these threads work within the same browser process.

---

## 2. How Multithreading Works

- A process can contain multiple threads.
- Each thread has its own stack.
- Threads share the process's heap memory.
- Each thread executes its own task.
- Multiple threads can execute in parallel on multiple CPU cores.

### Memory Structure

```text
             Process
                |
      ---------------------
      |         |         |
    Thread 1  Thread 2  Thread 3
      |         |         |
     Stack     Stack     Stack
      |         |         |
      ---------------------
                |
          Shared Heap
```

**Remember:**

- Each thread has its own JVM Stack.
- Each thread has its own stack frames.
- Threads share Heap memory.

---

## 3. Advantages of Multithreading

1. **Better Performance:** Multiple tasks can execute concurrently.
2. **CPU Utilization:** Makes better use of CPU resources.
3. **Responsiveness:** The application remains responsive while background tasks execute.
4. **Resource Sharing:** Threads share the same process memory.
5. **Parallel Execution:** Independent tasks can execute in parallel on multiple CPU cores.

## 4. Disadvantages of Multithreading

1. **Complexity:** Managing multiple threads is difficult.
2. **Deadlock:** Threads may wait indefinitely for each other.
3. **Race Condition:** Multiple threads accessing shared data can produce unexpected results.
4. **Synchronization Overhead:** Synchronization can reduce performance.
5. **Debugging Difficulty:** Thread-related bugs are difficult to identify.

---

## 5. Example of Multithreading in Java

```java
class MyThread extends Thread {

    @Override
    public void run() {
        for (int i = 1; i <= 5; i++) {
            System.out.println(
                Thread.currentThread().getName() + " : " + i
            );
        }
    }
}

public class Main {
    public static void main(String[] args) {

        MyThread t1 = new MyThread();
        MyThread t2 = new MyThread();

        t1.start();
        t2.start();
    }
}
```

### Possible Output

```text
Thread-0 : 1
Thread-1 : 1
Thread-0 : 2
Thread-1 : 2
Thread-1 : 3
Thread-0 : 3
Thread-0 : 4
Thread-1 : 4
Thread-0 : 5
Thread-1 : 5
```

**Note:** Output order is not guaranteed because thread scheduling is controlled by the JVM and operating system.

---

## 6. Difference Between Multitasking and Multithreading

| Multitasking | Multithreading |
|---|---|
| Executes multiple processes. | Executes multiple threads. |
| Process-level execution. | Thread-level execution. |
| Processes have separate memory spaces. | Threads share process memory. |
| Generally more resource-intensive. | Generally lightweight. |

---

# Problems of Multithreading in Java

## 1. Introduction

Multithreading allows multiple threads to execute concurrently within a single process.

However, when multiple threads access shared resources, several problems may occur.

### Main Problems of Multithreading

1. Race Condition
2. Deadlock
3. Starvation
4. Livelock
5. Thread Interference
6. Memory Visibility Problem

---

## 2. Race Condition

### Definition

A Race Condition occurs when multiple threads access and modify shared data concurrently, and the final result is inconsistance.

### Simple Explanation

When multiple threads modify the same data at the same time, one thread's update may be lost, resulting in an unexpected output.

### Example

Suppose a bank account has 1000 টাকা.

- Thread 1 deposits 500 টাকা.
- Thread 2 deposits 300 টাকা.

Expected balance:

```text
1000 + 500 + 300 = 1800
```

But both threads may read the old balance (1000).

| Thread | Operation | Result |
|---|---|---:|
| Thread 1 | Read balance | 1000 |
| Thread 2 | Read balance | 1000 |
| Thread 1 | Add 500 | 1500 |
| Thread 2 | Add 300 | 1300 |
| Thread 1 | Write balance | 1500 |
| Thread 2 | Write balance | 1300 |

Final balance = 1300 instead of 1800.

This is called a **Lost Update Problem**.

### Java Example

```java
class Counter {

    int count = 0;

    void increment() {
        count++;
    }
}

public class Main {

    public static void main(String[] args)
            throws InterruptedException {

        Counter c = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                c.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                c.increment();
            }
        });

        t1.start();
        t2.start();

        t1.join();
        t2.join();

        System.out.println(c.count);
    }
}
```

Expected result: `2000`

Actual result may be less than `2000` because of Race Condition.

### Solutions

- Use `synchronized`.
- Use `Lock`.
- Use `AtomicInteger`.

---

## 3. Deadlock

### Definition

Deadlock is a situation where two or more threads wait indefinitely for resources held by each other.

### Simple Explanation

Two threads are waiting for each other's locks. As a result, neither thread can continue execution.

### Example

- Thread 1 holds Lock A and waits for Lock B.
- Thread 2 holds Lock B and waits for Lock A.

Both threads wait forever.

### Diagram

```text
Thread 1                  Thread 2
   |                         |
 Holds Lock A             Holds Lock B
   |                         |
 Waits for Lock B         Waits for Lock A
   |                         |
   -------- DEADLOCK --------
```

### Solutions
import java.util.concurrent.atomic.AtomicInteger;

class Counter {

    AtomicInteger count = new AtomicInteger(0);

    void increment() {
        count.incrementAndGet();
    }
}

public class Main {
    public static void main(String[] args)
            throws InterruptedException {

        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        t1.join();
        t2.join();

        System.out.println(counter.count.get());
    }
}
<img width="985" height="349" alt="image" src="https://github.com/user-attachments/assets/15c3fdc6-8e2b-477f-8105-0751bcbbb12d" />
<img width="560" height="292" alt="image" src="https://github.com/user-attachments/assets/c2b3bf5a-77bf-4162-a1e1-8ece2a679c79" />

- Acquire locks in a consistent order.
- Avoid unnecessary nested locks.
- Use `tryLock()` with a timeout when appropriate.
- Avoid holding locks longer than necessary.

---

## 4. Starvation

### Definition

Starvation occurs when a thread waits for a long time because other threads continuously get access to CPU time or shared resources.

### Simple Explanation

A thread cannot get enough resources to execute because other threads continuously get priority.

### Example

Suppose:

- Thread 1 = High Priority
- Thread 2 = High Priority
- Thread 3 = Low Priority

High-priority threads continuously execute, so the low-priority thread may wait for a long time.

### Solutions

- Use fair locks.
- Avoid unnecessary priority differences.
- Apply proper resource scheduling.

---

## 5. Livelock

### Definition

Livelock occurs when two or more threads continuously respond to each other but cannot make progress.

### Simple Explanation

Threads are active and repeatedly changing their actions, but no useful work is completed.

### Real-Life Example

Two people are walking toward each other in a narrow hallway.

- Person A moves left.
- Person B also moves left.
- Both move right.
- Again, both block each other.

They keep moving but cannot pass.

### Difference Between Deadlock and Livelock

| Deadlock | Livelock |
|---|---|
| Threads are blocked. | Threads remain active. |
| No progress occurs. | No useful progress occurs. |
| Threads wait for resources. | Threads repeatedly respond to each other. |

### Solutions

- Introduce random delays.
- Use different retry strategies.
- Avoid repeated identical actions.

---

## 6. Thread Interference

### Definition

Thread interference occurs when multiple threads perform operations on shared data and their operations overlap unexpectedly, causing incorrect results.

### Simple Explanation

One thread's operation interferes with another thread's operation.

### Example

Suppose:

```java
int count = 5;
```

Two threads execute:

```java
count++;
```

The `count++` operation consists of three steps:

1. Read the current value.
2. Add 1.
3. Write the updated value.

Both threads may read 5 and write 6.

Expected result = 7.

Actual result = 6.

### Solutions

- Use `synchronized`.
- Use atomic variables.
- Use appropriate locking mechanisms.

---

## 7. Memory Visibility Problem

### Definition

A Memory Visibility Problem occurs when changes made by one thread to a shared variable are not immediately visible to another thread.

### Simple Explanation

One thread updates a variable, but another thread may continue seeing an old value because of memory visibility and caching issues.

### Example

```java
class SharedData {

    boolean running = true;

    void stop() {
        running = false;
    }
}
```

If one thread changes `running` to false, another thread may not observe the update promptly.

### Solution

Use:

- `volatile`
- `synchronized`
- Atomic classes

Example:

```java
volatile boolean running = true;
```

**Note:** `volatile` provides visibility and ordering guarantees, but does not make compound operations like `count++` atomic.

---

## 8. Comparison of Multithreading Problems

| Problem | Meaning |
|---|---|
| Race Condition | Unexpected result due to concurrent data access |
| Deadlock | Threads wait indefinitely for each other's locks |
| Starvation | A thread cannot get sufficient resources |
| Livelock | Threads remain active but make no progress |
| Thread Interference | Overlapping operations affect shared data |
| Memory Visibility | One thread cannot see another thread's update promptly |

---

## 9. Java Mechanisms to Handle Multithreading Problems

| Mechanism | Purpose |
|---|---|
| `synchronized` | Controls access to shared resources |
| `volatile` | Ensures visibility of variable updates |
| `Lock` | Provides explicit locking mechanisms |
| `AtomicInteger` | Performs atomic integer operations |
| `ExecutorService` | Manages thread execution |
| `join()` | Waits for another thread to finish |
| `ConcurrentHashMap` | Provides thread-safe map operations |

---

## 10. Important Job Exam Questions

**Q1. What is a Race Condition?**

When multiple threads access and modify shared data concurrently, and the result depends on their execution order.

**Q2. What is Deadlock?**

A situation where two or more threads wait indefinitely for resources held by each other.

**Q3. What is Starvation?**

A situation where a thread waits for a long time because other threads continuously get resources.

**Q4. What is Livelock?**

A situation where threads remain active but cannot make useful progress.

**Q5. What is Thread Interference?**

When multiple threads' operations overlap on shared data and produce unexpected results.

**Q6. What is a Memory Visibility Problem?**

When changes made by one thread are not visible to another thread as expected.

**Q7. How can we prevent Race Conditions?**

Using synchronization, locks, and atomic variables.

**Q8. Is `count++` an atomic operation?**

No. It involves reading, incrementing, and writing.

**Q9. What is the difference between Deadlock and Starvation?**

- Deadlock: Threads are stuck waiting for each other's resources.
- Starvation: A thread continuously fails to get the resources it needs.

**Q10. Does volatile make a variable thread-safe?**

It ensures visibility, but it does not make compound operations atomic.

---

## 11. Important Points to Remember

```text
Race Condition  = Unexpected Result
Deadlock        = Waiting Forever
Starvation      = Resource Not Available
Livelock        = Activity Without Progress
Thread Interference = Overlapping Operations
Memory Visibility   = Updated Value Not Visible
```

### Quick Revision

- Race Condition → Use `synchronized` or `AtomicInteger`.
- Deadlock → Maintain consistent lock ordering.
- Starvation → Use fair locking.
- Livelock → Use random delays or retry strategies.
- Thread Interference → Protect shared data.
- Memory Visibility → Use `volatile` or synchronization.

---

## 12. Next Topics to Learn

1. Thread Life Cycle
2. Thread Synchronization
3. `synchronized` Method and Block
4. `volatile` Keyword
5. `wait()`, `notify()` and `notifyAll()`
6. Lock Interface
7. Atomic Classes
8. ExecutorService
9. Producer-Consumer Problem
10. Thread Pool
