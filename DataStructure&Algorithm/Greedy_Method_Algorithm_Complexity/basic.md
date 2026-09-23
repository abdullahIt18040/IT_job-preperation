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
