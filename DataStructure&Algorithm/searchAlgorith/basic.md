# In-Place, Internal, External & Stable Sorting

These are important sorting concepts for **IT Government Job, Bank IT, Programmer, Assistant Programmer, and ICT/MIS exams**.

---

# 1. In-Place Sorting

## Definition

An **In-Place Sorting Algorithm** sorts the data using **very little extra memory**, usually **O(1) auxiliary space**.

> **In-Place = Sort mostly inside the original array without requiring another array of size O(n).**

### Example

```text
Original:
[5, 2, 8, 1, 3]

After sorting:
[1, 2, 3, 5, 8]
```

The original array itself is modified.

---

## Common In-Place Sorting Algorithms

| Algorithm      | In-Place?                       |
| -------------- | ------------------------------- |
| Bubble Sort    | ✅ Yes                           |
| Selection Sort | ✅ Yes                           |
| Insertion Sort | ✅ Yes                           |
| Quick Sort     | ✅ Usually*                      |
| Heap Sort      | ✅ Yes                           |
| Merge Sort     | ❌ Standard array implementation |

> **Quick Sort:** Usually considered in-place because partitioning uses O(1) auxiliary array space, but recursion requires O(log n) stack space on average. Definitions of "in-place" can vary.

---

## Important: In-Place ≠ Stable

These are **different properties**.

For example:

```text
Insertion Sort
→ In-Place ✅
→ Stable ✅
```

But:

```text
Heap Sort
→ In-Place ✅
→ Stable ❌
```

So an algorithm can be:

* In-place + Stable
* In-place + Unstable
* Not in-place + Stable

---

# 2. Internal Sorting

## Definition

**Internal Sorting** means the **entire dataset being sorted fits into the main memory (RAM)**.

```text
Data
 ↓
RAM
 ↓
Sorting
 ↓
Sorted Data
```

The CPU can directly access the complete dataset in memory.

### Examples

```text
Bubble Sort
Insertion Sort
Selection Sort
Quick Sort
Merge Sort
Heap Sort
```

These algorithms can perform internal sorting when the complete dataset fits in RAM.

---

# 3. External Sorting

## Definition

**External Sorting** is used when the dataset is **too large to fit into main memory (RAM)**.

The data is stored partly or mainly on external storage such as:

```text
SSD
HDD
External Storage
```

The algorithm processes data in chunks and combines the sorted chunks.

```text
Huge Dataset
     ↓
Doesn't fit in RAM
     ↓
Divide into chunks
     ↓
Sort chunks in RAM
     ↓
Store sorted chunks
     ↓
Merge sorted chunks
     ↓
Final Sorted Data
```

---

## Example

Suppose:

```text
Dataset = 500 GB
RAM     = 16 GB
```

The entire dataset cannot fit into RAM.

So we can:

```text
500 GB
 ↓
Chunks
 ↓
Sort each chunk
 ↓
Store sorted chunks
 ↓
Merge chunks
```

A common technique is:

> **External Merge Sort**

---

# 4. Internal vs External Sorting

| Feature      | Internal Sorting       | External Sorting       |
| ------------ | ---------------------- | ---------------------- |
| Dataset size | Fits in RAM            | Too large for RAM      |
| Main storage | RAM                    | RAM + External Storage |
| Disk I/O     | Usually less important | Very important         |
| Example      | Quick Sort             | External Merge Sort    |
| Used for     | Smaller datasets       | Huge datasets          |

### Easy Memory Trick

```text
Internal = Inside RAM
External = Outside RAM
```

---

# 5. Stable Sorting

## Definition

A **Stable Sorting Algorithm** preserves the **relative order of elements having equal keys**.

> **Stable = Equal-key elements keep their original relative order.**

---

## Example

Suppose:

```text
Name    Marks
A       80
B       70
C       80
D       60
```

Before sorting:

```text
80 → A → C
```

After stable sorting by Marks:

```text
60 → D
70 → B
80 → A
80 → C
```

The order of equal `80` marks remains:

```text
A → C
```

Therefore, the sorting is **Stable**.

---

# 6. Unstable Sorting

If sorting changes the relative order of equal-key elements:

```text
Before:
A → C

After:
C → A
```

Then the algorithm is **Unstable**.

---

# 7. Common Stable Sorting Algorithms

| Algorithm      | Stable?      |
| -------------- | ------------ |
| Bubble Sort    | ✅ Yes        |
| Insertion Sort | ✅ Yes        |
| Merge Sort     | ✅ Yes        |
| Selection Sort | ❌ Usually No |
| Quick Sort     | ❌ Usually No |
| Heap Sort      | ❌ No         |

> Stability can depend on the implementation. The table represents common/standard implementations.

---

# 8. In-Place vs Stable

These two concepts are often confused.

### In-Place

Question:

> **How much extra memory does the algorithm need?**

### Stable

Question:

> **Does it preserve the order of equal elements?**

Example:

```text
Insertion Sort
In-Place → ✅
Stable   → ✅
```

Example:

```text
Heap Sort
In-Place → ✅
Stable   → ❌
```

Example:

```text
Merge Sort
In-Place → ❌ (standard array implementation)
Stable   → ✅
```

---

# 9. Important Comparison Table

| Algorithm      |  In-Place |    Stable |       Typical Time |
| -------------- | --------: | --------: | -----------------: |
| Bubble Sort    |         ✅ |         ✅ |              O(n²) |
| Selection Sort |         ✅ |         ❌ |              O(n²) |
| Insertion Sort |         ✅ |         ✅ |              O(n²) |
| Merge Sort     |         ❌ |         ✅ |         O(n log n) |
| Quick Sort     | ✅ Usually | ❌ Usually | O(n log n) average |
| Heap Sort      |         ✅ |         ❌ |         O(n log n) |

> **Note:** "In-place" and "stable" are independent properties.

---

# 10. Internal vs External — Important Example

### Case 1

```text
Array = 100 MB
RAM = 16 GB
```

The complete dataset can fit in RAM.

```text
→ Internal Sorting
```

### Case 2

```text
Dataset = 500 GB
RAM = 16 GB
```

The complete dataset cannot fit in RAM.

```text
→ External Sorting
```

---

# 11. External Merge Sort

External Merge Sort is especially important for **very large datasets**.

### Basic Process

```text
Huge File
    ↓
Split into smaller chunks
    ↓
Load chunk into RAM
    ↓
Sort chunk
    ↓
Write sorted chunk to disk
    ↓
Repeat
    ↓
Merge sorted chunks
    ↓
Final sorted file
```

### Example

```text
Input:
[Large File]

       ↓

Chunk 1 → Sort → File 1
Chunk 2 → Sort → File 2
Chunk 3 → Sort → File 3
Chunk 4 → Sort → File 4

       ↓

Merge File 1 + File 2 + File 3 + File 4

       ↓

Sorted File
```

---

# 12. MCQ Traps

### Q1. What does In-Place Sorting mean?

**Answer:**

> Sorting using very little extra memory, commonly O(1) auxiliary space.

---

### Q2. Which is an In-Place sorting algorithm?

Examples:

```text
Bubble Sort
Selection Sort
Insertion Sort
Heap Sort
```

---

### Q3. Which standard sorting algorithm is generally NOT in-place because it uses O(n) auxiliary array space?

```text
Merge Sort
```

---

### Q4. What does Stable Sorting mean?

**Answer:**

> Equal-key elements maintain their original relative order.

---

### Q5. Which is a stable sorting algorithm?

```text
Merge Sort
Insertion Sort
Bubble Sort
```

---

### Q6. Which sorting technique is suitable when the dataset is larger than RAM?

```text
External Sorting
```

---

### Q7. A dataset completely fits into RAM. Which type of sorting?

```text
Internal Sorting
```

---

### Q8. A 500 GB file needs to be sorted but RAM is only 16 GB. Which technique?

```text
External Sorting
```

A common solution:

```text
External Merge Sort
```

---

# 13. Quick Revision

```text
IN-PLACE
↓
Uses very little extra memory
↓
Usually O(1) auxiliary space
```

```text
INTERNAL SORTING
↓
Entire dataset fits in RAM
```

```text
EXTERNAL SORTING
↓
Dataset does NOT fit in RAM
↓
Uses external storage
↓
External Merge Sort is common
```

```text
STABLE SORTING
↓
Equal keys
↓
Original relative order preserved
```

---

# 14. One-Minute Exam Revision

| Concept      | Remember                               |
| ------------ | -------------------------------------- |
| **In-Place** | Low extra memory                       |
| **Internal** | Data fits in RAM                       |
| **External** | Data does not fit in RAM               |
| **Stable**   | Equal elements preserve relative order |

### 🔥 Most Important

```text
In-Place  → Memory
Stable    → Equal elements' order
Internal  → RAM
External  → External storage
```

> **Shortcut:**
> **In-Place asks "How much extra memory?"**
> **Stable asks "What happens to equal elements?"**
> **Internal/External asks "Does the whole data fit in RAM?"**
