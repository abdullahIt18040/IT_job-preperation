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




