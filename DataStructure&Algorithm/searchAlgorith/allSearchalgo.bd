# Linear Search

## 1. What is Linear Search?

**Linear Search** is a simple searching algorithm that checks each element **one by one** from the beginning until the target element is found or the array ends.

> **Linear Search = Check elements sequentially, one by one.**

It is also called **Sequential Search**.

---

## 2. Example

Given:

```text
Array:
[10, 25, 30, 45, 60, 75]

Target = 45
```

Linear Search checks:

```text
10 → 25 → 30 → 45
```

`45` is found at index `3`.

```text
Output: Index 3
```

---

## 3. How Linear Search Works

Suppose:

```text
arr = [10, 25, 30, 45, 60]
target = 45
```

Steps:

```text
Step 1 → Compare 10 with 45 → Not Equal
Step 2 → Compare 25 with 45 → Not Equal
Step 3 → Compare 30 with 45 → Not Equal
Step 4 → Compare 45 with 45 → Found
```

Therefore:

```text
Index = 3
```

---

## 4. Algorithm

```text
LinearSearch(arr, target)

1. Start from index 0
2. Compare arr[i] with target
3. If arr[i] == target
      return i
4. Continue until the array ends
5. If target is not found
      return -1
```

---

## 5. Java Implementation

```java
public static int linearSearch(int[] arr, int target) {

    for (int i = 0; i < arr.length; i++) {

        if (arr[i] == target) {
            return i;
        }
    }

    return -1;
}
```

### Example

```java
int[] arr = {10, 25, 30, 45, 60};

int index = linearSearch(arr, 45);

System.out.println(index);
```

Output:

```text
3
```

---

## 6. Time Complexity

| Case         | Complexity | Explanation                       |
| ------------ | ---------- | --------------------------------- |
| Best Case    | **O(1)**   | Target is at the first position   |
| Average Case | **O(n)**   | Target is somewhere in the middle |
| Worst Case   | **O(n)**   | Target is at the end or absent    |

### Best Case

```text
[45, 10, 20, 30, 40]

Target = 45
```

Only one comparison:

```text
O(1)
```

### Worst Case

```text
[10, 20, 30, 40, 45]

Target = 100
```

Every element is checked:

```text
O(n)
```

---

## 7. Space Complexity

Linear Search uses only a few extra variables.

```text
Auxiliary Space = O(1)
```

Therefore:

```text
Time:
Best    → O(1)
Average → O(n)
Worst   → O(n)

Space:
O(1)
```

---

## 8. Does Linear Search Require a Sorted Array?

**No.**

Linear Search works on both:

```text
Sorted Array
Unsorted Array
```

Example:

```text
[50, 10, 80, 20, 40]
```

Target:

```text
20
```

Linear Search can still find it.

> **Important:** Unlike Binary Search, Linear Search does **not require sorted data**.

---

## 9. Linear Search vs Binary Search

| Feature                  | Linear Search | Binary Search      |
| ------------------------ | ------------- | ------------------ |
| Method                   | Sequential    | Divide and Conquer |
| Sorted data required?    | ❌ No          | ✅ Yes              |
| Best Case                | O(1)          | O(1)               |
| Average Case             | O(n)          | O(log n)           |
| Worst Case               | O(n)          | O(log n)           |
| Easy to implement        | ✅ Yes         | More complex       |
| Works with unsorted data | ✅ Yes         | ❌ No               |

---

## 10. When to Use Linear Search?

Linear Search is useful when:

* Data is **unsorted**
* Dataset is small
* Simplicity is important
* Data structure does not support efficient random access
* Only a few searches are required

Example:

```text
Small list → Linear Search
```

---

## 11. Important Properties

```text
Linear Search
     ↓
Sequential checking
     ↓
One element at a time
     ↓
Sorted data NOT required
     ↓
Best = O(1)
     ↓
Worst = O(n)
     ↓
Space = O(1)
```

---

## 12. MCQ Traps

### Q1. What is the worst-case time complexity of Linear Search?

**Answer:**

```text
O(n)
```

---

### Q2. Does Linear Search require a sorted array?

**Answer:**

```text
No
```

---

### Q3. What is the best-case complexity?

**Answer:**

```text
O(1)
```

When the target is the **first element**.

---

### Q4. What is the space complexity?

**Answer:**

```text
O(1)
```

---

### Q5. Linear Search is also known as?

**Answer:**

```text
Sequential Search
```

---

### Q6. If the target is not present, how many elements may be checked?

**Answer:**

```text
All n elements
```

Therefore:

```text
O(n)
```
# Binary Search

## 1. What is Binary Search?

**Binary Search** is an efficient searching algorithm that repeatedly divides a **sorted** search space into two halves.

> **Binary Search = Divide the search space into half repeatedly.**

It follows the **Divide and Conquer** technique.

---

## 2. Important Requirement

The most important condition for Binary Search:

> **The data must be sorted** for standard binary search.

Example:

```text
[10, 20, 30, 40, 50, 60, 70]
```

This is sorted in ascending order.

---

## 3. How Binary Search Works

Suppose:

```text
Array = [10, 20, 30, 40, 50, 60, 70]

Target = 60
```

### Step 1

```text
low = 0
high = 6
```

Calculate middle:

```text
mid = low + (high - low) / 2
    = 0 + (6 - 0) / 2
    = 3
```

```text
arr[mid] = 40
```

Compare:

```text
60 > 40
```

Therefore, ignore the left half.

```text
[10, 20, 30, 40] | [50, 60, 70]
                    ↑
                 Search here
```

---

### Step 2

Now:

```text
low = 4
high = 6
```

```text
mid = 4 + (6 - 4) / 2
    = 5
```

```text
arr[5] = 60
```

Target found.

```text
Index = 5
```

---

## 4. Basic Algorithm

```text
BinarySearch(arr, target)

1. Set low = 0
2. Set high = n - 1

3. While low <= high:

      mid = low + (high - low) / 2

      If arr[mid] == target:
          return mid

      Else if arr[mid] < target:
          low = mid + 1

      Else:
          high = mid - 1

4. Return -1
```

---

## 5. Java Implementation — Iterative

```java
public static int binarySearch(int[] arr, int target) {

    int low = 0;
    int high = arr.length - 1;

    while (low <= high) {

        int mid = low + (high - low) / 2;

        if (arr[mid] == target) {
            return mid;
        }

        if (arr[mid] < target) {
            low = mid + 1;
        } else {
            high = mid - 1;
        }
    }

    return -1;
}
```

### Example

```java
int[] arr = {10, 20, 30, 40, 50, 60, 70};

int index = binarySearch(arr, 60);

System.out.println(index);
```

Output:

```text
5
```

---

# 6. Why `low + (high - low) / 2`?

You may see:

```java
int mid = (low + high) / 2;
```

This works in many cases, but `low + (high - low) / 2` is commonly preferred because it avoids integer overflow when `low + high` exceeds the integer range.

Preferred:

```java
int mid = low + (high - low) / 2;
```

> **MCQ/Interview Tip:** Both calculate the middle mathematically, but the second form is safer for integer overflow.

---

# 7. Time Complexity

| Case         | Complexity   |
| ------------ | ------------ |
| Best Case    | **O(1)**     |
| Average Case | **O(log n)** |
| Worst Case   | **O(log n)** |

### Best Case

Target is exactly at the middle:

```text
[10, 20, 30, 40, 50]

Target = 30
```

Only one comparison:

```text
O(1)
```

### Worst Case

The search space is repeatedly divided:

```text
n
↓
n/2
↓
n/4
↓
n/8
↓
...
↓
1
```

Number of divisions:

```text
log₂ n
```

Therefore:

```text
O(log n)
```

---

# 8. Space Complexity

### Iterative Binary Search

```text
Auxiliary Space = O(1)
```

Because only a few variables are used:

```text
low
high
mid
```

### Recursive Binary Search

Recursive implementation uses the call stack:

```text
Space = O(log n)
```

Therefore:

| Implementation | Space        |
| -------------- | ------------ |
| Iterative      | **O(1)**     |
| Recursive      | **O(log n)** |

---

# 9. Recursive Binary Search

```java
public static int binarySearch(
        int[] arr, int low, int high, int target) {

    if (low > high) {
        return -1;
    }

    int mid = low + (high - low) / 2;

    if (arr[mid] == target) {
        return mid;
    }

    if (arr[mid] < target) {
        return binarySearch(arr, mid + 1, high, target);
    }

    return binarySearch(arr, low, mid - 1, target);
}
```

Call:

```java
int index = binarySearch(arr, 0, arr.length - 1, 60);
```

---

# 10. Binary Search Example

Given:

```text
[5, 10, 15, 20, 25, 30, 35]
```

Target:

```text
25
```

### First

```text
low = 0
high = 6
mid = 3
arr[mid] = 20
```

Since:

```text
25 > 20
```

Search right side.

```text
[25, 30, 35]
 ↑
```

### Second

```text
low = 4
high = 6
mid = 5
arr[mid] = 30
```

Since:

```text
25 < 30
```

Search left.

```text
[25]
 ↑
```

Target found.

```text
Index = 4
```

---

# 11. Binary Search vs Linear Search

| Feature              | Linear Search  | Binary Search           |
| -------------------- | -------------- | ----------------------- |
| Searching method     | Sequential     | Divide and Conquer      |
| Sorted data required | ❌ No           | ✅ Yes                   |
| Best Case            | O(1)           | O(1)                    |
| Average Case         | O(n)           | O(log n)                |
| Worst Case           | O(n)           | O(log n)                |
| Iterative Space      | O(1)           | O(1)                    |
| Easy to implement    | ✅              | Relatively more complex |
| Large sorted data    | Less efficient | More efficient          |

---

# 12. When Should You Use Binary Search?

Binary Search is useful when:

* Data is **sorted**
* Dataset is large
* Many searches are required
* Fast searching is needed
* Random access is available, such as an array

Example:

```text
Sorted Array + Large Data
          ↓
    Binary Search
          ↓
       O(log n)
```

---

# 13. Important Limitation

Binary Search requires a suitable ordered search space.

For a normal array:

```text
Sorted Array
      ↓
Binary Search
```

For an unsorted array:

```text
Unsorted Array
      ↓
Binary Search ❌
```

You generally need to sort first:

```text
Unsorted
   ↓
Sort
   ↓
Binary Search
```

But remember:

> If you only need one search, sorting first may not be worthwhile because sorting itself costs time.

---

# 14. MCQ Traps

### Q1. What is the worst-case time complexity of Binary Search?

```text
O(log n)
```

---

### Q2. What is required for standard Binary Search?

```text
Sorted data
```

---

### Q3. Best-case complexity?

```text
O(1)
```

When the target is found at the first middle position.

---

### Q4. Iterative Binary Search space complexity?

```text
O(1)
```

---

### Q5. Recursive Binary Search space complexity?

```text
O(log n)
```

Because of the recursion call stack.

---

### Q6. Binary Search uses which technique?

```text
Divide and Conquer
```

---

### Q7. What happens if `arr[mid] < target`?

Search the **right half**:

```java
low = mid + 1;
```

---

### Q8. What happens if `arr[mid] > target`?

Search the **left half**:

```java
high = mid - 1;
```

---

# 15. Quick Revision

```text
