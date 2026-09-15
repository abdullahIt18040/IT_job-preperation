<img width="1223" height="644" alt="image" src="https://github.com/user-attachments/assets/5ab960b4-7afd-4d05-9ef0-b14deabd8be4" />
### infix to prefix (same priority eksate thakte perbe) 

<img width="1173" height="663" alt="image" src="https://github.com/user-attachments/assets/a8947ef2-9975-4708-b831-b4e6761ec372" />



<img width="1172" height="467" alt="image" src="https://github.com/user-attachments/assets/d7553d95-3f7b-430c-9cfa-80ba409b3eb3" />
<img width="422" height="163" alt="image" src="https://github.com/user-attachments/assets/be4111aa-6dfb-403c-bc83-b171614c0c49" />
<img width="1183" height="634" alt="image" src="https://github.com/user-attachments/assets/7552242f-c751-43ca-a2df-088b59fff0c7" />
<img width="1207" height="530" alt="image" src="https://github.com/user-attachments/assets/662d56a6-ac3f-4467-8cbb-7b79b384cb62" />
<img width="1104" height="225" alt="image" src="https://github.com/user-attachments/assets/3b46f7bb-6789-440c-abec-715aff095219" />




# Expression Notations

There are three common ways to write an expression:

1. **Infix**
2. **Prefix**
3. **Postfix**

---

## 1. Infix Notation

In **Infix notation**, the operator is written **between operands**.

### Format

```text
Operand Operator Operand
```

### Example

```text
A + B
A - B
A * B
A / B
```

Example:

```text
A + B * C
```

Here `+` and `*` are operators, and `A`, `B`, `C` are operands.

### Key Point

> **Operator is between operands.**

---

# 2. Prefix Notation

In **Prefix notation**, the operator is written **before the operands**.

It is also called **Polish Notation**.

### Format

```text
Operator Operand Operand
```

### Example

Infix:

```text
A + B
```

Prefix:

```text
+ A B
```

Another example:

```text
A + B * C
```

Prefix:

```text
+ A * B C
```

### Key Point

> **Operator comes before operands.**

---

# 3. Postfix Notation

In **Postfix notation**, the operator is written **after the operands**.

It is also called **Reverse Polish Notation (RPN)**.

### Format

```text
Operand Operand Operator
```

### Example

Infix:

```text
A + B
```

Postfix:

```text
A B +
```

Another example:

```text
A + B * C
```

Postfix:

```text
A B C * +
```

### Key Point

> **Operator comes after operands.**

---

# 4. Comparison

| Notation    | Operator Position | Example |
| ----------- | ----------------- | ------- |
| **Infix**   | Between operands  | `A + B` |
| **Prefix**  | Before operands   | `+ A B` |
| **Postfix** | After operands    | `A B +` |

### Easy Memory Trick

```text
Infix   → A + B
Prefix  → + A B
Postfix → A B +
```

---

# 5. Operator Precedence

When converting Infix to Postfix, operator precedence is important.

```text
Highest
   ↓
^
* / %
+ -
   ↓
Lowest
```

### Precedence Table

| Operator | Precedence |
| -------- | ---------- |
| `^`      | Highest    |
| `* / %`  | Medium     |
| `+ -`    | Lowest     |

Parentheses have special priority:

```text
( )
```

---

# 6. Infix to Postfix

To convert **Infix → Postfix**, we use:

> **Stack + Operator Precedence**

### Basic Rules

1. **Operand** → Add directly to output.
2. **`(`** → Push into Stack.
3. **`)`** → Pop operators until `(` is found.
4. **Operator** → Compare precedence.
5. At the end → Pop all remaining operators.

---

## Example 1

Convert:

```text
A + B
```

### Step-by-step

```text
A → Output

+ → Stack

B → Output

End → Pop +
```

Result:

```text
Infix:
A + B

Postfix:
A B +
```

---

# 7. Example 2

Convert:

```text
A + B * C
```

### Step-by-step

| Token | Stack | Output      |
| ----- | ----- | ----------- |
| `A`   | —     | `A`         |
| `+`   | `+`   | `A`         |
| `B`   | `+`   | `A B`       |
| `*`   | `+ *` | `A B`       |
| `C`   | `+ *` | `A B C`     |
| End   | —     | `A B C * +` |

### Answer

```text
A + B * C
      ↓
A B C * +
```

Because:

```text
* has higher precedence than +
```

So `B * C` is processed first.

---

# 8. Example 3 — Parentheses

Convert:

```text
(A + B) * C
```

### Step-by-step

| Token | Stack | Output      |
| ----- | ----- | ----------- |
| `(`   | `(`   | —           |
| `A`   | `(`   | `A`         |
| `+`   | `( +` | `A`         |
| `B`   | `( +` | `A B`       |
| `)`   | —     | `A B +`     |
| `*`   | `*`   | `A B +`     |
| `C`   | `*`   | `A B + C`   |
| End   | —     | `A B + C *` |

### Answer

```text
Infix:
(A + B) * C

Postfix:
A B + C *
```

---

# 9. Important Example

Convert:

```text
A + B * C - D
```

Because:

```text
* > + and -
```

Postfix:

```text
A B C * + D -
```

---

# 10. Parentheses Rules

### Opening Parenthesis

```text
(
```

Push into Stack.

### Closing Parenthesis

```text
)
```

Pop until `(` is found.

Then remove `(`.

Parentheses are **not included in the final Postfix expression**.

---

# 11. Infix → Postfix Shortcut

```text
Operand
   ↓
Output

(
   ↓
Push

)
   ↓
Pop until (

Operator
   ↓
Check precedence
   ↓
Push/Pop

End
   ↓
Pop all operators
```

---

# 12. Exam Important Points

* **Infix** → Operator between operands.
* **Prefix** → Operator before operands.
* **Postfix** → Operator after operands.
* Prefix is also called **Polish Notation**.
* Postfix is also called **Reverse Polish Notation (RPN)**.
* **Infix → Postfix** uses a **Stack**.
* Operator precedence: `^ > * / % > + -`.
* Parentheses are removed in Postfix.
* Postfix evaluation also uses a **Stack**.

# Infix to Prefix

## 1. What is Infix?

In **Infix notation**, the operator is written **between operands**.

```text
A + B
A + B * C
(A + B) * C
```

Example:

```text
A + B
```

Here, `+` is between `A` and `B`.

---

## 2. What is Prefix?

In **Prefix notation**, the operator is written **before operands**.

Prefix is also called **Polish Notation**.

```text
+ A B
* + A B C
```

Example:

```text
Infix:   A + B

Prefix:  + A B
```

---

# 3. Infix to Prefix Conversion

### Main Logic

To convert **Infix → Prefix**:

```text
1. Reverse the Infix expression
2. Swap '(' with ')' and ')' with '('
3. Convert the reversed expression to Postfix
4. Reverse the Postfix expression
5. The result is Prefix
```

### Formula

```text
Infix
  ↓
Reverse
  ↓
Swap Brackets
  ↓
Infix → Postfix
  ↓
Reverse
  ↓
Prefix
```

### Easy Memory Trick

> **Reverse → Swap → Postfix → Reverse = Prefix**

---

# 4. Operator Precedence

During conversion, operator precedence is important.

| Operator | Precedence |
| -------- | ---------: |
| `^`      |    Highest |
| `* / %`  |     Medium |
| `+ -`    |     Lowest |

```text
^ > * / % > + -
```

---

# 5. Parentheses Rule

When reversing the expression, swap the parentheses:

```text
( → )
) → (
```

Example:

```text
(A + B)
```

After reverse:

```text
) B + A (
```

After swapping brackets:

```text
( B + A )
```

---

# 6. Example 1

### Infix

```text
A + B * C
```

### Step 1: Reverse

```text
C * B + A
```

### Step 2: Swap Brackets

No brackets.

```text
C * B + A
```

### Step 3: Convert to Postfix

```text
C B * A +
```

### Step 4: Reverse Postfix

```text
+ A * B C
```

### Final Prefix

```text
+A*BC
```

Therefore:

```text
Infix:   A + B * C
Prefix:  + A * B C
```

---

# 7. Example 2

### Infix

```text
(A + B) * C
```

### Step 1: Reverse

```text
C * ) B + A (
```

### Step 2: Swap Brackets

```text
C * ( B + A )
```

### Step 3: Convert to Postfix

```text
C B A + *
```

### Step 4: Reverse Postfix

```text
* + A B C
```

### Final Prefix

```text
*+ABC
```

Therefore:

```text
Infix:   (A + B) * C
Prefix:  * + A B C
```

---

# 8. Example 3

### Infix

```text
A + B * C - D
```

### Step 1: Reverse

```text
D - C * B + A
```

### Step 2: Convert to Postfix

```text
D C B * - A +
```

### Step 3: Reverse Postfix

```text
+ A - * B C D
```

### Final Prefix

```text
+A-*BCD
```

Therefore:

```text
Infix:   A + B * C - D
Prefix:  + A - * B C D
```

---

# 9. Example with Multiple Operators

### Infix

```text
(A + B) * (C - D)
```

### Reverse

```text
) D - C ( * ) B + A (
```

### Swap Brackets

```text
( D - C ) * ( B + A )
```

### Postfix

```text
D C - B A + *
```

### Reverse

```text
* + A B - C D
```

### Prefix

```text
*+AB-CD
```

---

# 10. Why Do We Reverse Twice?

### First Reverse

We reverse the Infix expression so that we can process it from the opposite direction.

```text
A + B * C
```

becomes:

```text
C * B + A
```

### Second Reverse

After converting the reversed expression to Postfix, we reverse the result to obtain Prefix.

```text
Postfix:
C B * A +

Reverse:
+ A * B C
```

So:

```text
Reverse → Postfix → Reverse = Prefix
```

---

# 11. Important Rules

```text
1. Reverse the expression.
2. Swap '(' and ')'.
3. Apply operator precedence.
4. Convert to Postfix.
5. Reverse the Postfix result.
```

### Final Rule

```text
Reverse
   ↓
Swap Brackets
   ↓
Postfix
   ↓
Reverse
   ↓
Prefix
```

---

# 12. Infix vs Prefix vs Postfix

| Notation    | Operator Position | Example |
| ----------- | ----------------- | ------- |
| **Infix**   | Between operands  | `A + B` |
| **Prefix**  | Before operands   | `+ A B` |
| **Postfix** | After operands    | `A B +` |

### Example

```text
Infix:    A + B * C

Prefix:   + A * B C

Postfix:  A B C * +
```

---

# 13. Exam Shortcut

For MCQ/Written exams, remember:

> **Infix → Prefix = Reverse + Swap Brackets + Postfix + Reverse**

```text
R → S → P → R
```

Where:

```text
R = Reverse
S = Swap Brackets
P = Postfix
R = Reverse
```

### Complexity

For an expression containing `n` symbols:

```text
Time Complexity:  O(n)
Space Complexity: O(n)
```

The stack is used during the conversion.

