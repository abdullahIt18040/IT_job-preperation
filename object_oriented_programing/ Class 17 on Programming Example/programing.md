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

![Uploading image.png…]()

