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
