### Greedy Method, Algorithm Complexity
# Complexity of an Algorithm

**Algorithm Complexity** measures how much **time** and **memory** an algorithm needs as the input size increases.

There are two main types:

1. **Time Complexity** → Measures the amount of time/operations an algorithm takes.
2. **Space Complexity** → Measures the amount of extra memory an algorithm uses.

## Example

```text
Linear Search
Input size = n

Time Complexity  → O(n)
Space Complexity → O(1)
```

## In Short

```text
Algorithm Complexity
        ↓
 ┌───────────────┐
 │               │
Time           Space
O(n)           O(1)
```

**Complexity is usually expressed using Big-O notation: `O(...)`.**

<img width="1183" height="515" alt="image" src="https://github.com/user-attachments/assets/72fb262a-9429-4cce-9a3c-469cd1cdd692" />

<img width="666" height="406" alt="image" src="https://github.com/user-attachments/assets/177819b2-1d88-4b7b-bf6f-1cdb0b9447fb" />
# Asymptotic Notation

Asymptotic notation describes how an algorithm's time or space grows as the input size n increases.

It helps us compare algorithms **without depending on a specific machine, programming language, or exact execution time**.

---

## Main Types

| Notation            | Meaning                         | Example      |
| ------------------- | ------------------------------- | ------------ |
| **Big-O `O()`**     | Upper bound / worst-case growth | `O(n²)`      |
| **Big-Omega `Ω()`** | Lower bound / best-case growth  | `Ω(n)`       |
| **Big-Theta `Θ()`** | Tight bound / exact growth rate | `Θ(n log n)` |

---

## Example

Suppose an algorithm performs:

```text
3n² + 5n + 10 operations
```

For large `n`, the **dominant term** is `n²`.

Therefore:

```text
O(n²)
Θ(n²)
Ω(n²)
```

---

## Easy Way to Remember

```text
O()  → Upper Bound
Ω()  → Lower Bound
Θ()  → Tight Bound
```

**In short:** Asymptotic notation tells us **how an algorithm's performance grows when the input size becomes large**.
# Common Big-O Time Complexities

These are common **Time Complexity** notations that describe how an algorithm's operations grow as the input size `n` increases.
<img width="795" height="646" alt="image" src="https://github.com/user-attachments/assets/f5fa49af-4388-4557-943f-5876a116da8c" />

## 1. `O(1)` — Constant

The number of operations remains almost the same regardless of input size.

```java
arr[0];
```

```text
n = 10   → 1 operation
n = 1M   → 1 operation
```

**Very fast**

---

## 2. `O(log n)` — Logarithmic

The problem size is reduced by a factor each step.

**Example:** Binary Search

```text
n → n/2 → n/4 → n/8 → ...
```

**Very efficient for large `n`.**

---

## 3. `O(n)` — Linear

Each element is processed once.

**Example:** Linear Search

```text
n = 10   → ~10 operations
n = 100  → ~100 operations
```

If `n` doubles, operations also approximately double.

---

## 4. `O(n log n)` — Linearithmic

The algorithm performs approximately `n × log n` operations.

**Examples:**

* Merge Sort
* Heap Sort

```text
n × log n
```

Faster than `O(n²)` for large `n`.

---

## 5. `O(n²)` — Quadratic

Usually occurs with **nested loops**.

```java
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        // work
    }
}
```

```text
n × n = n²
```

**Example:** Bubble Sort

If `n` doubles, operations become approximately **4×**.

---

## 6. `O(n³)` — Cubic

Usually occurs with **three nested loops**.

```text
n × n × n = n³
```

**Example:** Some matrix algorithms.

If `n` doubles, operations become approximately **8×**.

---

## 7. `O(2ⁿ)` — Exponential

The number of operations grows very rapidly as `n` increases.

```text
n = 5  → 32
n = 10 → 1,024
n = 20 → 1,048,576
```

**Examples:**

* Some recursive subset problems
* Some recursive combination problems

Very expensive for large `n`.

---

## 8. `O(n!)` — Factorial

Grows even faster than `O(2ⁿ)`.

```text
n! = n × (n-1) × (n-2) × ... × 1
```

Example:

```text
5!  = 120
10! = 3,628,800
```

**Example:** Generating all possible permutations.

Extremely expensive for large `n`.

---

## Complexity Order

From **faster → slower**:

```text
O(1)
   ↓
O(log n)
   ↓
O(n)
   ↓
O(n log n)
   ↓
O(n²)
   ↓
O(n³)
   ↓
O(2ⁿ)
   ↓
O(n!)
```

> **Remember:** As `n` increases, complexities lower in this list generally grow much faster.

<img width="1227" height="564" alt="image" src="https://github.com/user-attachments/assets/2db7fafe-7444-48d7-be87-806a4a7d2026" />

