### Space Complexity 
```
Example 1: Array input হিসেবে দেওয়া আছে

ধরি:

int sum(int[] arr, int n) {

    int sum = 0;       // 1 variable
    for (int i = 0; i < n; i++) {  // 1 variable
        sum = sum + arr[i];
    }

    return sum;
}

ধরি input:

arr = [10, 20, 30, 40, 50]

এখানে arr-এর memory আমরা algorithm-এর তৈরি করা extra memory হিসেবে ধরছি না।

কারণ:

arr → আগে থেকেই input হিসেবে দেওয়া

Algorithm শুধু দুইটি ছোট variable ব্যবহার করছে:

sum → O(1)
i   → O(1)

তাই:

$$ \boxed{\text{Auxiliary Space}=O(1)} $$
Example 2: নতুন Array তৈরি করলে

এখন code পরিবর্তন করি:

int[] doubleArray(int[] arr, int n) {

    int[] result = new int[n];

    for (int i = 0; i < n; i++) {
        result[i] = arr[i] * 2;
    }

    return result;
}

এখানে:

arr    → input array
result → নতুন array

result-এ nটি element আছে।

তাই:

$$ \text{Extra Space}=O(n) $$

অর্থাৎ:

$$ \boxed{\text{Auxiliary Space}=O(n)} $$
Example 3: শুধু কয়েকটি variable
int findMax(int[] arr, int n) {

    int max = arr[0];

    for (int i = 1; i < n; i++) {

        if (arr[i] > max) {
            max = arr[i];
        }
    }

    return max;
}

এখানে input:

arr = [5, 8, 2, 10, 3]

Algorithm নতুন কোনো array তৈরি করছে না।

শুধু:

max → constant space
i   → constant space

তাই:

$$ \boxed{\text{Auxiliary Space}=O(1)} $$

যদিও input array-এর size n।

Example 4: নতুন array তৈরি করলে
int[] copyArray(int[] arr, int n) {

    int[] copy = new int[n];

    for (int i = 0; i < n; i++) {
        copy[i] = arr[i];
    }

    return copy;
}

এখানে:

Input:
arr → n elements

Extra:
copy → n elements

তাই:

$$ \boxed{O(n)} $$
সবচেয়ে সহজভাবে মনে রাখুন
Case 1 — Input Array
int sum(int[] arr, int n)

arr input, নতুন করে বানানো হয়নি।

Input Space → O(n)
Auxiliary Space → O(1)
Case 2 — নতুন Array
int[] result = new int[n];

Algorithm নিজেই n size-এর নতুন array বানাচ্ছে।

Input Space → O(n)
Auxiliary Space → O(n)
⭐ Space Complexity বনাম Auxiliary Space

এটা এভাবে মনে রাখুন:

                 Total Space
                     │
          ┌──────────┴──────────┐
          ↓                     ↓
     Input Space          Auxiliary Space
      O(n)                  O(1)

যেমন:

int sum(int[] arr, int n) {
    int sum = 0;
    for(int i = 0; i < n; i++) {
        sum += arr[i];
    }
    return sum;
}

এখানে:

arr = Input Space       → O(n)
sum, i = Extra Space   → O(1)

তাই যদি প্রশ্ন করে:

"What is the auxiliary space complexity?"

উত্তর:

$$ \boxed{O(1)} $$

আর যদি input space-সহ total space ধরতে বলে:

$$ \boxed{O(n)} $$
🔥 Exam Trick

Input array-এর memory সাধারণত Auxiliary Space-এর মধ্যে ধরা হয় না।

তাই int[] arr শুধু input হিসেবে থাকলে, এবং নতুন কোনো n-size data structure তৈরি না করলে → Auxiliary Space = O(1)।
```
