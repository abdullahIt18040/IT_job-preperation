## insertion sort 
## Question : 3rd iteration element postion show . 

<img width="736" height="385" alt="image" src="https://github.com/user-attachments/assets/a29955c1-140d-45fb-9863-5550d4091f1b" />
# Insertion Sort

## 1. What is Insertion Sort?

**Insertion Sort** is a simple sorting algorithm that builds the sorted array **one element at a time**.

It works similar to arranging playing cards in your hand.

### Main Idea

> Pick one element (`key`) and insert it into its correct position in the already sorted portion.

---

# 2. Example

Given:

```text
[5, 3, 4, 1, 2]
```

Initially, the first element is considered sorted:

```text
[5] | [3, 4, 1, 2]
 ↑
Sorted
```

Take `3` as `key`:

```text
[5 | 3]
```

Since `5 > 3`, shift `5` to the right:

```text
[5, 5]
```

Insert `3`:

```text
[3, 5]
```

Now:

```text
[3, 5] | [4, 1, 2]
```

Take `4` as `key`:

```text
[3, 5 | 4]
```

`5 > 4`, so shift `5`:

```text
[3, 5, 5]
```

Insert `4`:

```text
[3, 4, 5]
```

Continue the same process.

Final result:

```text
[1, 2, 3, 4, 5]
```

---

# 3. Algorithm

```text
INSERTION_SORT(A, n)

1. For i = 1 to n - 1

2.     key = A[i]

3.     j = i - 1

4.     While j >= 0 AND A[j] > key

5.         A[j + 1] = A[j]

6.         j = j - 1

7.     A[j + 1] = key
```

---

# 4. Algorithm Explanation

### Step 1: Start from index 1

```text
i = 1
```

Why not index `0`?

Because a single element is already considered sorted.

```text
[5] | [3, 4, 1, 2]
 ↑
Sorted portion
```

---

### Step 2: Select the key

```text
key = A[i]
```

The `key` is the element we want to insert into the sorted portion.

Example:

```text
[3, 5] | 4
          ↑
         key
```

---

### Step 3: Compare with previous elements

```text
j = i - 1
```

Compare:

```text
A[j] > key
```

If the previous element is greater than `key`, shift it one position to the right.

---

### Step 4: Shift larger elements

```text
A[j + 1] = A[j]
```

Example:

```text
[3, 5, 4]

5 > 4
```

Shift `5`:

```text
[3, 5, 5]
```

---

### Step 5: Insert the key

After finding the correct position:

```text
A[j + 1] = key
```

Result:

```text
[3, 4, 5]
```

---

# 5. Java Implementation

```java
public static void insertionSort(int[] arr) {

    for (int i = 1; i < arr.length; i++) {

        int key = arr[i];
        int j = i - 1;

        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }

        arr[j + 1] = key;
    }
}
```

---

# 6. Complexity

| Case         | Time Complexity |
| ------------ | --------------: |
| Best Case    |        **O(n)** |
| Average Case |       **O(n²)** |
| Worst Case   |       **O(n²)** |

### Space Complexity

```text
O(1)
```

Insertion Sort is an **in-place sorting algorithm**.

---

# 7. Best Case

Already sorted array:

```text
[1, 2, 3, 4, 5]
```

Very few comparisons are required.

```text
Time = O(n)
```

---

# 8. Worst Case

Reverse sorted array:

```text
[5, 4, 3, 2, 1]
```

Many elements need to be shifted.

```text
Time = O(n²)
```

---

# 9. Important Properties

| Property     | Insertion Sort |
| ------------ | -------------- |
| Best Case    | O(n)           |
| Average Case | O(n²)          |
| Worst Case   | O(n²)          |
| Space        | O(1)           |
| In-place     | Yes            |
| Stable       | Yes            |
| Adaptive     | Yes            |

---

# 10. Easy Memory Trick

```text
Insertion Sort:

1. Pick key
2. Compare with left side
3. Shift larger elements
4. Insert key
```

### Key Formula

```text
key = A[i]

while (j >= 0 && A[j] > key)
    shift A[j] right

insert key
```

> **Insertion Sort = Pick → Compare → Shift → Insert**
## Question 4 th  iteration array elemet show 
# Bubble Sort

## 1. What is Bubble Sort?

**Bubble Sort** is a simple sorting algorithm that repeatedly compares **adjacent elements** and swaps them if they are in the wrong order.

> **Idea:** Compare → Swap → Repeat

## 2. Example

```text
[5, 3, 8, 4, 2]

Pass 1:
[3, 5, 4, 2, 8]

Pass 2:
[3, 4, 2, 5, 8]

Pass 3:
[3, 2, 4, 5, 8]

Pass 4:
[2, 3, 4, 5, 8]
```

The **largest element moves to the end** after each pass.

## 3. Algorithm

```text
BUBBLE_SORT(A, n)

for i = 0 to n-2
    for j = 0 to n-i-2
        if A[j] > A[j+1]
            swap(A[j], A[j+1])
```

## 4. Java

```java
public static void bubbleSort(int[] arr) {
    for (int i = 0; i < arr.length - 1; i++) {
        for (int j = 0; j < arr.length - i - 1; j++) {

            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
```

## 5. Complexity

| Case    | Time  |
| ------- | ----- |
| Best    | O(n)  |
| Average | O(n²) |
| Worst   | O(n²) |

**Space:** O(1)
**Stable:** Yes
**In-place:** Yes

## 6. Key Point

> **Bubble Sort:** Compare adjacent elements and swap them if they are in the wrong order.

**Memory Trick:**
`Compare → Swap → Largest goes to the end`

## Best Case — O(n)
```
Occurs when the array is already sorted.
Worst Case — O(n²)

Occurs when the array is reverse sorted.

```

### Selection sort .
find Minimum number ,
<img width="657" height="632" alt="image" src="https://github.com/user-attachments/assets/2c5b8d5b-24fe-48e0-b860-211582845b18" />

<img width="1139" height="677" alt="image" src="https://github.com/user-attachments/assets/c6b3f877-5c5a-4083-90bd-f12b1bf1ad83" />
# Selection Sort

## 1. What is Selection Sort?

**Selection Sort** repeatedly finds the **smallest element** from the unsorted part and places it at the beginning.

> **Idea:** Find Minimum → Swap → Repeat

## 2. Example

```text
[5, 3, 8, 4, 2]

Find minimum → 2
Swap 2 with 5

[2, 3, 8, 4, 5]

Find minimum → 3
Already in correct position

[2, 3, 8, 4, 5]

Find minimum → 4
Swap 4 with 8

[2, 3, 4, 8, 5]

Find minimum → 5
Swap 5 with 8

[2, 3, 4, 5, 8]
```

## 3. Algorithm

```text
SELECTION_SORT(A, n)

for i = 0 to n-2
    minIndex = i

    for j = i+1 to n-1
        if A[j] < A[minIndex]
            minIndex = j

    swap(A[i], A[minIndex])
```

## 4. Java

```java
public static void selectionSort(int[] arr) {
    for (int i = 0; i < arr.length - 1; i++) {

        int minIndex = i;

        for (int j = i + 1; j < arr.length; j++) {
            if (arr[j] < arr[minIndex]) {
                minIndex = j;
            }
        }

        int temp = arr[i];
        arr[i] = arr[minIndex];
        arr[minIndex] = temp;
    }
}
```

## 5. Complexity

| Case    | Time  |
| ------- | ----- |
| Best    | O(n²) |
| Average | O(n²) |
| Worst   | O(n²) |

**Space:** O(1)
**In-place:** Yes
**Stable:** No (standard implementation)

## 6. Key Point

> **Selection Sort always searches for the minimum element and puts it in its correct position.**

### Memory Trick

**Find Minimum → Swap → Sorted Part Grows**
### Merge Sort 
rule : privot left side  always small and right will be greater .
<img width="943" height="648" alt="image" src="https://github.com/user-attachments/assets/80529cbe-f4bd-4cf6-bb8b-4ebe38e2520d" />
<img width="466" height="657" alt="image" src="https://github.com/user-attachments/assets/f97e1811-4284-4dff-9fb7-d7e4db2d1e6e" />
<img width="378" height="665" alt="image" src="https://github.com/user-attachments/assets/9f614b7f-f73b-4621-ada2-72f13dd2b043" />
<img width="646" height="614" alt="image" src="https://github.com/user-attachments/assets/5ce61d2a-cecf-47f6-b45d-7ac55da55a13" />
### time complexity :
best case O (nlogn) when privot select always middle .
worst case O (n^2) when rivot select alwayas high or low value 
<img width="721" height="671" alt="image" src="https://github.com/user-attachments/assets/ec8260e6-6650-479f-b8a9-7cff986dc2ba" />
# Quick Sort

## 1. What is Quick Sort?

**Quick Sort** is a **divide-and-conquer** sorting algorithm.

It selects a **pivot**, partitions the array around the pivot, and recursively sorts the left and right parts.

> **Idea:** Choose Pivot → Partition → Recursively Sort

## 2. Example

```text
Array:
[5, 3, 8, 4, 2]

Pivot = 4

Smaller than 4 → [3, 2]
Pivot           → [4]
Greater than 4  → [5, 8]

[3, 2] [4] [5, 8]

Sort left:
[2, 3]

Sort right:
[5, 8]

Final:
[2, 3, 4, 5, 8]
```

## 3. Algorithm

```text
QUICK_SORT(A, low, high)

if low < high
    pivotIndex = PARTITION(A, low, high)

    QUICK_SORT(A, low, pivotIndex - 1)
    QUICK_SORT(A, pivotIndex + 1, high)
```

## 4. Partition

```text
PARTITION(A, low, high)

pivot = A[high]
i = low - 1

for j = low to high - 1
    if A[j] <= pivot
        i++
        swap(A[i], A[j])

swap(A[i + 1], A[high])

return i + 1
```

## 5. Java

```java
public static void quickSort(int[] arr, int low, int high) {
    if (low < high) {
        int pivotIndex = partition(arr, low, high);

        quickSort(arr, low, pivotIndex - 1);
        quickSort(arr, pivotIndex + 1, high);
    }
}

private static int partition(int[] arr, int low, int high) {
    int pivot = arr[high];
    int i = low - 1;

    for (int j = low; j < high; j++) {
        if (arr[j] <= pivot) {
            i++;

            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
    }

    int temp = arr[i + 1];
    arr[i + 1] = arr[high];
    arr[high] = temp;

    return i + 1;
}
```

## 6. Complexity

| Case    | Time       |
| ------- | ---------- |
| Best    | O(n log n) |
| Average | O(n log n) |
| Worst   | O(n²)      |

**Space:** O(log n) average recursion stack
**In-place:** Yes
**Stable:** No

## 7. When Does Worst Case Occur?

Worst case occurs when the pivot repeatedly creates **highly unbalanced partitions**.

Example:

```text
[1, 2, 3, 4, 5, 6, 7]

Pivot = 7
[1,2,3,4,5,6] | 7

Pivot = 6
[1,2,3,4,5] | 6

Pivot = 5
[1,2,3,4] | 5
```

This gives:

```text
O(n²)
```

## 8. Key Point

> **Quick Sort = Pivot + Partition + Recursion**

### Memory Trick

**Choose → Partition → Left/Right → Repeat**


### Merge Sort 
<img width="1199" height="675" alt="image" src="https://github.com/user-attachments/assets/781aa30f-999c-4508-9aef-6424f717d511" />
<img width="1324" height="749" alt="image" src="https://github.com/user-attachments/assets/9ee691ad-85ad-4bef-9f5e-eeb7d0683f1b" />
<img width="1220" height="734" alt="image" src="https://github.com/user-attachments/assets/0a9e37e7-6714-49df-a9ad-9853ee42f15d" />
## Merge Sort Algorithm:
<img width="632" height="586" alt="image" src="https://github.com/user-attachments/assets/d16d3eaf-f0d8-4db5-9e9a-6a47031a38c8" />
# Merge Sort — IT Government Job Preparation

## 1. What is Merge Sort?

**Merge Sort** is a **Divide and Conquer** sorting algorithm.

It works in three main steps:

```text
Divide → Conquer → Merge
```

### Basic Idea

1. Divide the array into two halves.
2. Recursively sort both halves.
3. Merge the two sorted halves.

---

## 2. Example

Given:

```text
[38, 27, 43, 3, 9, 82, 10]
```

### Step 1 — Divide

```text
[38, 27, 43, 3]    [9, 82, 10]
```

Again:

```text
[38, 27] [43, 3]    [9, 82] [10]
```

Again:

```text
[38] [27] [43] [3]    [9] [82] [10]
```

Now every part contains one element.

---

## 3. Step 2 — Merge

Merge sorted elements:

```text
[38] + [27]
→ [27, 38]
```

```text
[43] + [3]
→ [3, 43]
```

Then:

```text
[27, 38] + [3, 43]
→ [3, 27, 38, 43]
```

Similarly:

```text
[9] + [82]
→ [9, 82]
```

Finally:

```text
[3, 27, 38, 43] + [9, 10, 82]
→ [3, 9, 10, 27, 38, 43, 82]
```

### Final Result

```text
[3, 9, 10, 27, 38, 43, 82]
```

---

## 4. Merge Sort Visualization

---

# 5. Divide and Conquer

Merge Sort follows:

```text
Divide
   ↓
Conquer
   ↓
Combine
```

### Divide

Split the array into smaller subarrays.

### Conquer

Recursively sort the smaller arrays.

### Combine

Merge the sorted arrays.

---

# 6. Why Does Merge Sort Stop?

The recursion stops when the subarray contains:

```text
1 element
```

A single element is already sorted.

Base condition:

```java
if (left >= right) {
    return;
}
```

---

# 7. Java Implementation

```java
public static void mergeSort(int[] arr, int left, int right) {

    if (left >= right) {
        return;
    }

    int mid = left + (right - left) / 2;

    mergeSort(arr, left, mid);
    mergeSort(arr, mid + 1, right);

    merge(arr, left, mid, right);
}
```

### Merge Function

```java
public static void merge(int[] arr, int left, int mid, int right) {

    int n1 = mid - left + 1;
    int n2 = right - mid;

    int[] L = new int[n1];
    int[] R = new int[n2];

    for (int i = 0; i < n1; i++) {
        L[i] = arr[left + i];
    }

    for (int j = 0; j < n2; j++) {
        R[j] = arr[mid + 1 + j];
    }

    int i = 0;
    int j = 0;
    int k = left;

    while (i < n1 && j < n2) {

        if (L[i] <= R[j]) {
            arr[k++] = L[i++];
        } else {
            arr[k++] = R[j++];
        }
    }

    while (i < n1) {
        arr[k++] = L[i++];
    }

    while (j < n2) {
        arr[k++] = R[j++];
    }
}
```

Call:

```java
mergeSort(arr, 0, arr.length - 1);
```

---

# 8. How Merge Works

Suppose:

```text
Left  = [10, 30, 50]
Right = [20, 40, 60]
```

Compare the first elements:

```text
10 < 20
```

Take `10`.

```text
[10]
```

Then:

```text
30 > 20
```

Take `20`.

```text
[10, 20]
```

Then:

```text
30 < 40
```

Take `30`.

Continue until both arrays are merged.

Final:

```text
[10, 20, 30, 40, 50, 60]
```

---

# 9. Merge Sort Complexity

| Case         | Time Complexity |
| ------------ | --------------: |
| Best Case    |      O(n log n) |
| Average Case |      O(n log n) |
| Worst Case   |      O(n log n) |

### Important Exam Fact

> Merge Sort has **O(n log n)** time complexity in best, average and worst cases.

---

# 10. Space Complexity

Typical array-based Merge Sort requires an auxiliary array:

```text
O(n)
```

So:

```text
Time  → O(n log n)
Space → O(n)
```

There is also recursion-stack space of approximately `O(log n)`; the dominant auxiliary space for the standard implementation is `O(n)`.

---

# 11. Is Merge Sort Stable?

Yes.

**Merge Sort is a stable sorting algorithm** when implemented appropriately.

Stable means:

> Equal elements maintain their original relative order.

Example:

```text
A(5)  B(5)
```

After stable sorting:

```text
A(5)  B(5)
```

Their relative order remains unchanged.

### Important MCQ

```text
Merge Sort → Stable
```

---

# 12. Is Merge Sort In-Place?

Standard array-based Merge Sort is generally considered:

```text
Not In-Place
```

because it requires extra memory for merging.

Typical auxiliary space:

```text
O(n)
```

---

# 13. Merge Sort Properties

| Property        | Merge Sort                 |
| --------------- | -------------------------- |
| Technique       | Divide and Conquer         |
| Best Case       | O(n log n)                 |
| Average Case    | O(n log n)                 |
| Worst Case      | O(n log n)                 |
| Extra Space     | O(n)                       |
| Stable          | Yes                        |
| In-Place        | No, standard array version |
| Recursive       | Usually                    |
| Comparison Sort | Yes                        |

---

# 14. Merge Sort vs Bubble Sort

| Feature                         | Merge Sort       | Bubble Sort       |
| ------------------------------- | ---------------- | ----------------- |
| Technique                       | Divide & Conquer | Repeated swapping |
| Best                            | O(n log n)       | O(n)*             |
| Average                         | O(n log n)       | O(n²)             |
| Worst                           | O(n log n)       | O(n²)             |
| Stable                          | Yes              | Yes               |
| Extra Space                     | O(n)             | O(1)              |
| Generally Faster for Large Data | Yes              | No                |

`*` Bubble Sort can have O(n) best case with an optimized implementation when the array is already sorted.

---

# 15. Merge Sort vs Quick Sort

| Feature              | Merge Sort       | Quick Sort                                 |
| -------------------- | ---------------- | ------------------------------------------ |
| Technique            | Divide & Conquer | Divide & Conquer                           |
| Best                 | O(n log n)       | O(n log n)                                 |
| Average              | O(n log n)       | O(n log n)                                 |
| Worst                | O(n log n)       | O(n²)                                      |
| Stable               | Yes              | Usually No                                 |
| Extra Space          | O(n)             | Typically O(log n) average recursion stack |
| Worst-case Guarantee | Yes              | No, with basic implementation              |

### Important

> Merge Sort guarantees **O(n log n)** worst-case time.

---

# 16. Why Merge Sort is O(n log n)?

The array is divided approximately in half at each level.

Number of levels:

```text
log₂ n
```

At each level, merging all elements costs:

```text
O(n)
```

Therefore:

```text
O(n) × O(log n)
```

Result:

```text
O(n log n)
```

---

# 17. Recurrence Relation

Merge Sort recurrence:

```text
T(n) = 2T(n/2) + O(n)
```

Therefore:

```text
T(n) = O(n log n)
```

### Government Job MCQ Point

If you see:

```text
T(n) = 2T(n/2) + O(n)
```

the answer is:

```text
O(n log n)
```

---

# 18. Merge Sort Example

Input:

```text
[8, 3, 5, 4, 7, 6, 1, 2]
```

### Divide

```text
[8, 3, 5, 4] [7, 6, 1, 2]
```

```text
[8, 3] [5, 4] [7, 6] [1, 2]
```

```text
[8] [3] [5] [4] [7] [6] [1] [2]
```

### Merge

```text
[3, 8] [4, 5] [6, 7] [1, 2]
```

Then:

```text
[3, 4, 5, 8] [1, 2, 6, 7]
```

Finally:

```text
[1, 2, 3, 4, 5, 6, 7, 8]
```

---

# 19. Important Government Job MCQ Questions

### Q1. Merge Sort is based on which technique?

```text
Divide and Conquer
```

---

### Q2. Best-case time complexity?

```text
O(n log n)
```

---

### Q3. Average-case time complexity?

```text
O(n log n)
```

---

### Q4. Worst-case time complexity?

```text
O(n log n)
```

---

### Q5. Is Merge Sort stable?

```text
Yes
```

---

### Q6. Standard array-based Merge Sort requires extra space of?

```text
O(n)
```

---

### Q7. Is standard Merge Sort in-place?

```text
No
```

---

### Q8. What is the recurrence relation?

```text
T(n) = 2T(n/2) + O(n)
```

---

### Q9. What is the recursion depth?

```text
O(log n)
```

---

### Q10. What is the main operation during the combine phase?

```text
Merging two sorted arrays
```

---

### Q11. What is the base case?

```text
Subarray contains one element
```

---

### Q12. Which sorting algorithm guarantees O(n log n) worst-case time?

```text
Merge Sort
```

---

### Q13. Which sorting algorithm is stable?

```text
Merge Sort
```

---

### Q14. Merge Sort belongs to which category?

```text
Comparison-based sorting algorithm
```

---

### Q15. What happens if the array is already sorted?

Merge Sort still generally performs:

```text
O(n log n)
```

work in the standard implementation.

---

# 20. Important MCQ Traps

## Trap 1

Do not say:

```text
Merge Sort → O(n²)
```

Correct:

```text
Best    → O(n log n)
Average → O(n log n)
Worst   → O(n log n)
```

---

## Trap 2

Merge Sort is **not** normally an in-place sorting algorithm for arrays.

```text
Extra Space → O(n)
```

---

## Trap 3

Merge Sort is stable.

```text
Merge Sort → Stable
Quick Sort → Usually Not Stable
```

---

## Trap 4

Merge Sort uses:

```text
Divide
+
Recursive Sort
+
Merge
```

---

## Trap 5

Already sorted input does not make standard Merge Sort:

```text
O(n)
```

It remains approximately:

```text
O(n log n)
```

---

# 21. Advantages of Merge Sort

* Guaranteed `O(n log n)` worst-case time
* Stable sorting algorithm
* Good for large datasets
* Works well with linked lists
* Suitable for external sorting
* Predictable performance
* Easy to implement recursively

---

# 22. Disadvantages of Merge Sort

* Requires extra memory for standard array implementation
* More memory usage than in-place algorithms such as Heap Sort
* Recursive implementation adds call-stack overhead
* For small arrays, simpler algorithms can sometimes be preferable

---

# 23. Merge Sort and Linked List

Merge Sort is particularly suitable for Linked Lists because:

* Linked Lists do not provide efficient random access.
* Splitting and merging can be performed through node references.
* Merging sorted linked lists can be done without shifting elements.

### Important

> Merge Sort is commonly preferred for sorting Linked Lists.

---

# 24. Sorting Algorithm Comparison

| Algorithm      |       Best |    Average |      Worst | Stable     |
| -------------- | ---------: | ---------: | ---------: | ---------- |
| Bubble Sort    |      O(n)* |      O(n²) |      O(n²) | Yes        |
| Selection Sort |      O(n²) |      O(n²) |      O(n²) | Usually No |
| Insertion Sort |       O(n) |      O(n²) |      O(n²) | Yes        |
| Merge Sort     | O(n log n) | O(n log n) | O(n log n) | Yes        |
| Quick Sort     | O(n log n) | O(n log n) |      O(n²) | Usually No |
| Heap Sort      | O(n log n) | O(n log n) | O(n log n) | No         |

`*` With an optimized Bubble Sort that detects no swaps.

---

# 25. Key Terms

```text
Divide and Conquer
Recursion
Merge
Sorted Subarray
Stable Sort
O(n log n)
O(n) Auxiliary Space
```

---

# 26. One-Minute Revision

```text
MERGE SORT
│
├── Divide and Conquer
│
├── Divide
│   └── Split array into halves
│
├── Conquer
│   └── Recursively sort
│
├── Combine
│   └── Merge sorted halves
│
├── Best    → O(n log n)
├── Average → O(n log n)
├── Worst   → O(n log n)
│
├── Space   → O(n)
├── Stable  → Yes
├── Standard Array Version
│   └── Not In-Place
│
└── Recurrence
    └── T(n) = 2T(n/2) + O(n)
```

---


---


### Most Important MCQ Line

> **Merge Sort is a stable Divide-and-Conquer sorting algorithm with O(n log n) best, average, and worst-case time complexity and O(n) auxiliary space for the standard array implementation.**
# Stable Sorting

## 1. What is Stable Sorting?

A **Stable Sorting Algorithm** preserves the **relative order of elements having equal keys/values**.

> **Stable Sort = Equal keys → Original relative order remains unchanged.**

---

## 2. Simple Example

Consider the following students:

```text
Name    Marks
A       80
B       70
C       80
D       60
```

Sort by `Marks` in ascending order:

```text
D  60
B  70
A  80
C  80
```

Before sorting, the order of students with `80` marks was:

```text
A → C
```

After sorting:

```text
A → C
```

The relative order is preserved.

Therefore, the sorting is **Stable**.

---

## 3. Unstable Sorting

If after sorting the result becomes:

```text
D  60
B  70
C  80
A  80
```

Then the order changed:

```text
Before:  A → C
After:   C → A
```

Therefore, the sorting is **Unstable**.

---

## 4. Stable vs Unstable

| Feature        | Stable Sort             | Unstable Sort    |
| -------------- | ----------------------- | ---------------- |
| Equal elements | Preserve original order | May change order |
| Relative order | Preserved               | Not guaranteed   |
| Example        | Merge Sort              | Quick Sort       |
| Important for  | Multi-level sorting     | General sorting  |

---

## 5. Common Sorting Algorithms

| Algorithm      | Stable?      |
| -------------- | ------------ |
| Bubble Sort    | ✅ Yes        |
| Insertion Sort | ✅ Yes        |
| Merge Sort     | ✅ Yes        |
| Selection Sort | ❌ Usually No |
| Quick Sort     | ❌ Usually No |
| Heap Sort      | ❌ No         |

> **Important:** Stability can depend on the specific implementation. The table shows the standard/common implementations.

---

## 6. Real-Life Example

Suppose employees are initially sorted by joining date:

```text
Rahim   2020
Karim   2021
Hasan   2020
```

Now sort by `Year`:

```text
Rahim   2020
Hasan   2020
Karim   2021
```

For the same year (`2020`):

```text
Rahim → Hasan
```

is preserved.

This is **Stable Sorting**.

---

## 7. Why is Stability Important?

Stability is useful when sorting data by **multiple fields**.

Example:

### First sort by Name

```text
A → B → C
```

Then sort by Department.

If the second sorting algorithm is stable, the previous ordering among employees in the same department is preserved.

This is useful in:

* Student records
* Employee records
* Database records
* Multi-level sorting
* Data processing

---

## 8. MCQ Trap

### Question:

What does a stable sorting algorithm guarantee?

**Answer:**

> It preserves the relative order of elements with equal keys.

### Remember:

```text
Stable ≠ Always same complete array order

Stable = Equal-key elements keep their relative order
```

---

## 9. One-Minute Revision

```text
Stable Sort
     ↓
Equal keys
     ↓
Original relative order preserved
```

### Common Stable Algorithms

```text
Bubble Sort
Insertion Sort
Merge Sort
```

### Common Unstable Algorithms

```text
Selection Sort
Quick Sort
Heap Sort
```

### Most Important Definition

> **Stable sorting preserves the relative order of equal elements.**







