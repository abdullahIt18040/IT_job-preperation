# programing
<img width="765" height="428" alt="image" src="https://github.com/user-attachments/assets/f9987993-e399-42b1-b845-24ad8b419521" />
# Pre-increment and Post-increment in C

## 1. Pre-increment (`++a`)

Pre-increment increases the value by 1 **before using the value**.

```c
int a = 5;
int b = ++a;

printf("%d\n", a); // 6
printf("%d\n", b); // 6
```

**Explanation:** First, `a` becomes `6`. Then the updated value is assigned to `b`.

## 2. Post-increment (`a++`)

Post-increment uses the **current value first**, then increases the value by 1.

```c
int a = 5;
int b = a++;

printf("%d\n", a); // 6
printf("%d\n", b); // 5
```

**Explanation:** First, the old value `5` is assigned to `b`. Then `a` becomes `6`.

## Difference Between Pre-increment and Post-increment

| Pre-increment (`++a`) | Post-increment (`a++`) |
|---|---|
| Increases the value first. | Uses the current value first. |
| Then uses the updated value. | Then increases the value. |
| `b = ++a;` | `b = a++;` |

## Easy Trick to Remember

- `++a` → Increment first, use later.
- `a++` → Use first, increment later.

<img width="1223" height="454" alt="image" src="https://github.com/user-attachments/assets/140eeb76-1110-4fd8-847c-74ed01cfc219" />
# Pre-increment and Post-increment in C

## Example: Multiple Increment Operators

```c
int a = 10, b = 10;
printf("%d%d%d%d", a++, a++, ++a, a);
```

### Important Note

In C, the evaluation order of function arguments is not specified. Modifying `a` multiple times in the same `printf()` call without proper sequencing causes **undefined behavior**.

Therefore, the output is **unpredictable**. Do not assume a specific output in an exam.

## Correct Example

```c
int a = 10;

printf("%d ", a++);
printf("%d ", a++);
printf("%d ", ++a);
printf("%d", a);
```

**Output:**
```text
10 11 13 13
```

### Explanation

1. `a++` prints `10`, then `a` becomes `11`.
2. `a++` prints `11`, then `a` becomes `12`.
3. `++a` first makes `a = 13`, then prints `13`.
4. `a` is now `13`, so it prints `13`.

### Remember

- `a++` → Use the current value, then increment.
- `++a` → Increment first, then use the updated value.
- Multiple modifications of the same variable in one C expression can cause undefined behavior.

<img width="887" height="548" alt="image" src="https://github.com/user-attachments/assets/61dad048-e764-4ab7-b49d-aa2d0e1ec269" />
<img width="664" height="518" alt="image" src="https://github.com/user-attachments/assets/8d579271-a35d-4543-ab1c-2e4936ca9a81" />

## implement stack using 2 queue 
<img width="488" height="253" alt="image" src="https://github.com/user-attachments/assets/abc53084-2521-4963-bc6a-c198f9600a7e" />

<img width="560" height="733" alt="image" src="https://github.com/user-attachments/assets/dea1e2f6-c963-4177-a9f7-854769df0c98" />
<img width="560" height="733" alt="image" src="https://github.com/user-attachments/assets/3d69658d-665e-4249-999a-26eda3ffb770" />
<img width="1421" height="791" alt="image" src="https://github.com/user-attachments/assets/e209f336-c2dd-4781-996b-8a87c71f1080" />
<img width="532" height="712" alt="image" src="https://github.com/user-attachments/assets/0789cb49-e715-4bf8-9d40-38c6219357e8" />
<img width="1028" height="512" alt="image" src="https://github.com/user-attachments/assets/4058b2c3-44d6-4eda-a00d-85128c10a461" />
## find Source IP and Destinatioin iP 
<img width="1039" height="389" alt="image" src="https://github.com/user-attachments/assets/f8adb209-44d3-45b7-ad35-8a3f438a31a1" />
# Number Programs in C++

## 1. Strong Number
**Definition:** A number whose sum of factorials of its digits equals the original number.

**Example:**
\[
145 = 1!+4!+5! = 1+24+120 = 145
\]

```cpp
int n = 145, temp = n, sum = 0;

while (temp > 0) {
    int digit = temp % 10, fact = 1;

    for (int i = 1; i <= digit; i++)
        fact *= i;

    sum += fact;
    temp /= 10;
}

if (sum == n) cout << "Strong Number";
```
Examples: `1, 2, 145, 40585`

---

## 2. Armstrong Number
**Definition:** A number whose sum of digits raised to the power of total digits equals the original number.

**Example:**
\[
153 = 1^3+5^3+3^3 = 153
\]

```cpp
int n = 153, temp = n, sum = 0;
int count = 0, x = n;

do {
    count++;
    x /= 10;
} while (x != 0);

do {
    int digit = temp % 10, power = 1;

    for (int i = 1; i <= count; i++)
        power *= digit;

    sum += power;
    temp /= 10;
} while (temp != 0);

if (sum == n) cout << "Armstrong Number";
```
Examples: `0, 1, 153, 370, 371, 407`

---

## 3. Perfect Number
**Definition:** A number equal to the sum of its proper divisors (excluding itself).

**Example:**
\[
6 = 1+2+3
\]

```cpp
int n = 6, sum = 0;

for (int i = 1; i < n; i++) {
    if (n % i == 0)
        sum += i;
}

if (sum == n && n > 0)
    cout << "Perfect Number";
```
Examples: `6, 28, 496, 8128`

---

## 4. Neon Number
**Definition:** A number whose sum of the digits of its square equals the original number.

**Example:**
\[
9^2 = 81
\]
\[
8+1 = 9
\]

```cpp
int n = 9, square = n * n, sum = 0;

while (square > 0) {
    sum += square % 10;
    square /= 10;
}

if (sum == n) cout << "Neon Number";
```
Examples: `0, 1, 9`

---

## 5. Automorphic Number
**Definition:** A number whose square ends with the same digits as the original number.

**Example:**
\[
25^2 = 625
\]
\[
625 \% 100 = 25
\]

```cpp
int n = 25, square = n * n;
int temp = n, divisor = 1;

while (temp > 0) {
    divisor *= 10;
    temp /= 10;
}

if (square % divisor == n)
    cout << "Automorphic Number";
```
Examples: `0, 1, 5, 6, 25, 76, 376, 625`

---

## 6. Quick Revision

| Number | Condition | Example |
|---|---|---|
| Strong | Sum of digit factorials = Number | 145 |
| Armstrong | Sum of digit powers = Number | 153 |
| Perfect | Sum of proper divisors = Number | 6 |
| Neon | Sum of square's digits = Number | 9 |
| Automorphic | Square ends with original number | 25 |

## 7. Important C++ Expressions

| Expression | Meaning |
|---|---|
| `n % 10` | Extract last digit |
| `n / 10` | Remove last digit |
| `n % i == 0` | Check divisor |
| `fact *= i` | Calculate factorial |
| `power *= digit` | Calculate power |
| `n * n` | Calculate square |
| `square % divisor` | Extract ending digits |

### Remember for Job Exams

- Strong → Factorial (!)
- Armstrong → Power (^)
- Perfect → Proper Divisors (+)
- Neon → Square's digit sum
- Automorphic → Square ends with original number

**These number programs are important for C/C++ programming, viva and Assistant Programmer / Programmer recruitment exams.**

![Uploading image.png…]()

