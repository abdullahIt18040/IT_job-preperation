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
