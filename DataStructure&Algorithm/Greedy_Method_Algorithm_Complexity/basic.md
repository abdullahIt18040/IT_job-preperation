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
<img width="926" height="560" alt="image" src="https://github.com/user-attachments/assets/301ea563-e123-4c0d-83da-d868bcb4675a" />
## fibonacce serise or sum 1 t0 n using recursion 
time complextity O (2^n)
<img width="734" height="419" alt="image" src="https://github.com/user-attachments/assets/f4b06c04-1a0f-468f-85ca-35ae0e335b14" />
<img width="990" height="569" alt="image" src="https://github.com/user-attachments/assets/520a8b81-ddf3-4a91-becf-0b46f4f8f530" />
## time complextity 
<img width="1007" height="463" alt="image" src="https://github.com/user-attachments/assets/3883fbbf-3588-4fc6-aff5-cc510a952b8d" />

<img width="1058" height="436" alt="image" src="https://github.com/user-attachments/assets/1046c7c8-5019-48ab-b4fc-0816d3ecfb61" />
<img width="1065" height="468" alt="image" src="https://github.com/user-attachments/assets/23bf2f90-0a1a-406e-baaf-06157d5cce29" />
<img width="334" height="387" alt="image" src="https://github.com/user-attachments/assets/fbddbd57-7100-4849-8b8c-3a264a4e4d38" />

<img width="1154" height="505" alt="image" src="https://github.com/user-attachments/assets/67e5a7a1-8666-44e3-be06-7f9bcf53580e" />

# Greedy Algorithm

A **Greedy Algorithm** makes the **best possible choice at each step** with the hope of getting the overall optimal solution.

## Advantages

1. **Simple and Easy to Understand**

   * The logic is usually straightforward.

2. **Easy to Implement**

   * Generally requires less code and simpler logic.

3. **Fast Execution**

   * Greedy algorithms often have good time complexity.

4. **Uses Less Memory**

   * Usually does not require storing many possible solutions.

5. **Works Well for Some Optimization Problems**

   * Especially when the problem has:

     * **Greedy Choice Property**
     * **Optimal Substructure**

### Examples

* Kruskal's Algorithm
* Prim's Algorithm
* Dijkstra's Algorithm
* Huffman Coding
* Activity Selection

---

## Disadvantages

1. **Does Not Always Give the Optimal Solution**

   * A locally best choice may lead to a globally non-optimal solution.

2. **Choices Are Usually Not Reconsidered**

   * Once a choice is made, the algorithm generally does not change it.

3. **Requires Greedy Choice Property**

   * It works correctly only when making the local best choice can lead to an optimal solution.

4. **Proof of Correctness Can Be Difficult**

   * A mathematical proof may be required to show that the greedy approach produces an optimal solution.

---

## Key Idea

```text
Greedy Algorithm
       ↓
Choose the best option NOW
       ↓
Continue step by step
       ↓
Hope for the optimal solution
```

## Greedy vs Dynamic Programming

```text
Greedy
   → Makes the best choice at the current step

Dynamic Programming
   → Solves and compares subproblems
   → Stores previous results
```

### Key Point

> **Greedy Algorithm → Best choice at the current step**
>
> **It does not always guarantee the globally optimal solution.**
soltuion
 <img width="960" height="568" alt="image" src="https://github.com/user-attachments/assets/76d8929a-2e27-47d8-b05b-46ad556d7f60" />
> needs 2 coines.
<img width="1104" height="518" alt="image" src="https://github.com/user-attachments/assets/a0ed75b2-84dd-4f81-9a56-542aa1303200" />

Fraction knapsack probelem  unit price = total value / total weight then which value maximun it choose after then take less expensive value and so on
<img width="1115" height="451" alt="image" src="https://github.com/user-attachments/assets/2006c23f-626a-4b16-a490-dc8d095d9ea9" />
<img width="839" height="631" alt="image" src="https://github.com/user-attachments/assets/3c62cc82-028c-408c-8d6c-f4b7fb324e50" />
## Huffman coding Algorithm
<img width="1202" height="610" alt="image" src="https://github.com/user-attachments/assets/1f6da70a-f8b6-4b75-82bc-0b2e4efd8a7a" />
solution:
<img width="1202" height="610" alt="image" src="https://github.com/user-attachments/assets/65609e27-7654-4169-9226-d18a0ac913a8" />
![Uploading image.png…]()
