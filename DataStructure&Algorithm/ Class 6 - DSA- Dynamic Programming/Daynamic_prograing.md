## Recursive algorithm
<img width="797" height="467" alt="image" src="https://github.com/user-attachments/assets/3d690f23-56c2-4782-a6dd-d7f01f9e83e3" />

<img width="981" height="494" alt="image" src="https://github.com/user-attachments/assets/2d8d6941-dc17-41e9-9dab-ab4378e83846" />

# Recursion with Static Variable — Solution

## Initial Value

Assume the recursive function has a static variable:

```java
static int x = 5;
```

We call:

```java
fun(3);
```

---

## Recursive Calls

### 1. `fun(3)`

First, `x` is increased by `2`:

```text
x = 5 + 2 = 7
```

Then:

```text
fun(3) = fun(2) + x
```

---

### 2. `fun(2)`

Again, `x` is increased by `2`:

```text
x = 7 + 2 = 9
```

Then:

```text
fun(2) = fun(1) + x
```

---

### 3. `fun(1)`

Since:

```text
n <= 1
```

the base case is reached:

```text
fun(1) = 1
```

---

# Returning From Recursion

Now the recursive calls return in **reverse order**.

### `fun(2)`

At this point, `x = 9`.

```text
fun(2) = fun(1) + x
       = 1 + 9
       = 10
```

### `fun(3)`

```text
fun(3) = fun(2) + x
       = 10 + 9
       = 19
```

Therefore:

```text
fun(3) = 19
```

---

# Call Stack

The execution can be visualized as:

```text
fun(3)
  x = 7
    ↓
fun(2)
  x = 9
    ↓
fun(1)
  return 1
    ↑
fun(2)
  return 1 + 9 = 10
    ↑
fun(3)
  return 10 + 9 = 19
```

---

# Important Point: Static Variable

`x` is a **static variable**:

```java
static int x = 5;
```

A static variable has **one shared copy** for the entire class.

Therefore, every recursive call uses the **same `x`**.

```text
Initial x = 5
     ↓
fun(3) → x = 7
     ↓
fun(2) → x = 9
     ↓
fun(1) → x remains 9
```

So when the recursive calls return, `x` is still:

```text
x = 9
```

The important thing is that `x` is **not created separately for each recursive call**.

---

# Final Answer

```text
fun(3) = 19
```

**Answer: `19`**
<img width="973" height="517" alt="image" src="https://github.com/user-attachments/assets/feab87c4-d79f-4020-93a2-497de5970026" />
<img width="255" height="150" alt="image" src="https://github.com/user-attachments/assets/f8710467-8c26-435a-9d5e-dc7b4a59187f" />
# Optimization Problem — Short Notes

## 1. Optimization Problem

A problem where we need to find the **best possible solution**.
or
An Optimization Problem is a problem where we need to find the best possible solution from a set of possible solutions.

* **Maximize** → make something largest
* **Minimize** → make something smallest

**Example:** Find the route with minimum distance.

---

## 2. Feasible Solution

A Feasible Solution is a solution that satisfies all constraints or rules of the problem.
```text
Capacity = 10 kg

8 kg  → Feasible ✅
12 kg → Not Feasible ❌
```

---

## 3. Optimal Solution

The **best feasible solution** according to the objective.
or
An Optimal Solution is the best feasible solution according to the objective .

```text
Costs:
A → 500
B → 300
C → 400

B → Optimal Solution
```

because `300` is the minimum.

---

## Easy Shortcut

```text
Optimization Problem → Find the best solution
Feasible Solution    → Satisfies all constraints
Optimal Solution     → Best among feasible solutions
```

> **Optimal Solution = Best Feasible Solution**


<img width="986" height="359" alt="image" src="https://github.com/user-attachments/assets/076fcb41-b995-4b6d-bf66-820da0af4cb5" />


# Define Dynamic Programming and explain its properties with example ?

#  Dynamic Programming

Dynamic Programming (DP) solves a problem by breaking it into smaller **subproblems** and **storing their results** to avoid repeated calculations.

> **DP = Solve + Store + Reuse**

## 1. Overlapping Subproblems

The **same subproblem appears multiple times**.

### Example: Fibonacci

```text
F(5)
├── F(4)
│   └── F(3)
└── F(3)
    └── F(2)
```

Here, `F(3)` is calculated more than once, so we store its result.

> **Overlapping Subproblems = Same subproblem occurs repeatedly.**

---

## 2. Optimal Substructure

The **optimal solution of a problem can be built from optimal solutions of smaller subproblems**.

### Example: Shortest Path

```text
A → B → C → D
```

If this is the shortest path from `A` to `D`, then `A → B → C` must also be the shortest path from `A` to `C`.

> **Optimal Substructure = Optimal solution contains optimal sub-solutions.**


# Backtracking

## Definition

**Backtracking** is an algorithmic technique where we try different choices one by one. If a choice does not work, we go back and try another choice.


### Basic Idea

```text
Choose
  ↓
Explore
  ↓
Valid?
 ├─ Yes → Continue
 └─ No  → Undo → Try another choice
Backtracking tries different choices and finds a solution that satisfies all given constraints or rules . it finds feasible solution.
```
# given arrary arr[4] = [2,1,4,3] n=4 m=5 find feasible solution sum of subset backtracking  draw tree and find  solution.
যদি প্রশ্ন হয় “Find any one subset whose sum is 5 ” → শুধু একটি solution পেলেই হবে। ✅

<img width="864" height="440" alt="image" src="https://github.com/user-attachments/assets/dd2ea21a-35c8-458f-9efc-a01b91e79a7e" />

<img width="1058" height="573" alt="image" src="https://github.com/user-attachments/assets/980a6e1b-5b19-4368-8d4c-70ed7c06a4a7" />
<img width="1139" height="674" alt="image" src="https://github.com/user-attachments/assets/1f4aa21c-6119-4b17-8db1-e9933eef4c4e" />
<img width="1090" height="674" alt="image" src="https://github.com/user-attachments/assets/55fc5d39-6a18-4cb6-979b-fc421252430e" />
যদি প্রশ্ন হয় “Find all subsets whose sum is 5 ” → সবগুলো solution বের করতে হবে। ✅

<img width="990" height="674" alt="image" src="https://github.com/user-attachments/assets/a9c1bf96-4b67-457a-86c3-862683ed63ed" />
<img width="994" height="668" alt="image" src="https://github.com/user-attachments/assets/2c600fed-1dd9-488c-ace1-79e8116969e9" />




