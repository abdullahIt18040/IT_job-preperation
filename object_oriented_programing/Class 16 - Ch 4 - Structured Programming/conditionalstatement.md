# If-Else Statement in C

## Definition
An **if-else statement** is used to make decisions in a program. It executes one block of code if the condition is true; otherwise, it executes another block.

বাংলা: শর্ত সত্য হলে `if`-এর কোড চলে, আর শর্ত মিথ্যা হলে `else`-এর কোড চলে।

## Syntax

```c
if (condition) {
    // Executes if condition is true
} else {
    // Executes if condition is false
}
```

# Types of Conditional Statements in C

Conditional statements are used to make decisions in a C program.

## 1. `if` Statement
Executes code if a condition is true.

```c
if (age >= 18) {
    printf("Adult");
}
```

## 2. `if-else` Statement
Chooses between two options.

```c
if (n % 2 == 0) {
    printf("Even");
} else {
    printf("Odd");
}
```

## 3. `else-if` Ladder
Checks multiple conditions.

```c
if (marks >= 80) {
    printf("A+");
} else if (marks >= 60) {
    printf("A");
} else if (marks >= 40) {
    printf("Pass");
} else {
    printf("Fail");
}
```

## 4. Nested `if-else` Statement
Uses an `if-else` statement inside another `if` or `else` block.

```c
if (age >= 18) {
    if (age >= 60) {
        printf("Senior Citizen");
    } else {
        printf("Adult");
    }
} else {
    printf("Minor");
}
```
# Data Types Allowed in a Switch Statement in C
# Switch Statement in C

## Definition
A **switch statement** is a conditional statement that selects one block of code from multiple options based on the value of an expression.

বাংলা: একটি expression-এর মান অনুযায়ী একাধিক option থেকে একটি নির্দিষ্ট block of code চালানোর জন্য `switch` statement ব্যবহার করা হয়।

## Syntax

```c
switch (expression) {
    case value1:
        // Code
        break;

    case value2:
        // Code
        break;

    default:
        // Code if no case matches
}
```

## Example: Day of the Week

```c
#include <stdio.h>

int main() {
    int day = 2;

    switch (day) {
        case 1:
            printf("Saturday");
            break;

        case 2:
            printf("Sunday");
            break;

        case 3:
            printf("Monday");
            break;

        default:
            printf("Invalid day");
    }

    return 0;
}
```

**Output:**
```text
Sunday
```

## Important Keywords

- **`switch`**: Checks the expression's value.
- **`case`**: Defines a possible matching value.
- **`break`**: Exits the switch block.
- **`default`**: Executes when no case matches.

## Important Points

1. Each `case` value must be a unique constant.
2. The `break` statement prevents execution from continuing into the next case.
3. The `default` case is optional.
4. In C, `switch` expressions must have an integer type, including `char` and `enum` types. Floating-point values and strings cannot be used directly as switch expressions.

## Difference Between If-Else and Switch

| If-Else | Switch |
|---|---|
| Checks conditions or ranges | Matches an expression against constant case values |
| Supports relational operators like `>` and `<` | Does not directly support ranges |
| Suitable for complex conditions | Suitable for multiple fixed choices |

**Remember:** `switch` selects a matching `case`, `break` exits the switch, and `default` handles unmatched values.
## Definition
In C, a `switch` expression must have an **integer type**, such as `int`, `char`, or `enum`.

Floating-point values and strings cannot be used directly as `switch` expressions.

## 1. Allowed Data Types

### `int`
```c
int n = 2;

switch (n) {
    case 1:
        printf("One");
        break;
    case 2:
        printf("Two");
        break;
}
```
**Output:** `Two`

### `char`
```c
char grade = 'A';

switch (grade) {
    case 'A':
        printf("Excellent");
        break;
    case 'B':
        printf("Good");
        break;
}
```
**Output:** `Excellent`

### `enum`
```c
enum Day { SAT, SUN, MON };

enum Day day = SUN;

switch (day) {
    case SAT:
        printf("Saturday");
        break;
    case SUN:
        printf("Sunday");
        break;
    case MON:
        printf("Monday");
        break;
}
```
**Output:** `Sunday`

**Note:** An `enum` is a user-defined type containing named integer constants.

## 2. Not Allowed Data Types

### `float` and `double`
```c
float n = 2.5;

// Invalid in C
switch (n) {
    case 2:
        printf("Hello");
        break;
}
```
**Reason:** `float` and `double` are floating-point types, not integer types.

### String
```c
char name[] = "Mamun";

// Invalid in C
switch (name) {
    case "Mamun":
        printf("Hello");
        break;
}
```
**Reason:** A string in C is represented by a character array. It cannot be used directly as a `switch` expression.

**Alternative:** Use `strcmp()` to compare strings with `if-else`.

## 3. Summary Table

| Data Type | Allowed in `switch`? |
|---|---|
| `int` | Yes |
| `char` | Yes |
| `enum` | Yes |
| `float` | No |
| `double` | No |
| String | No |

## Important Points
- `switch` works with integer types.
- `char` is allowed because it is an integer type in C.
- `enum` values are integer constants.
- `case` labels must be constant expressions of an appropriate integer type.
- `break` exits the `switch` block.
- `default` executes when no case matches.

**Exam Note:** In C, a `switch` expression must have an integer type, including `char` and `enum`. Floating-point values and strings cannot be used directly as switch expressions.
<img width="895" height="558" alt="image" src="https://github.com/user-attachments/assets/cf1df47f-267a-479a-89f7-9991d914ea05" />
# Difference Between `if-else` and `switch` in C

## Definition

- **`if-else`:** Used to make decisions based on conditions.
- **`switch`:** Used to select one option by matching an expression against fixed case values.

## Differences

| `if-else` | `switch` |
|---|---|
| 1. Checks conditions. | 1. Matches values. |
| 2. Supports relational operators like `>`, `<`, `>=`, `<=`. | 2. Does not directly support relational conditions or ranges. |
| 3. Supports complex conditions using `&&`, `||`, etc. | 3. Compares an expression with constant `case` values. |
| 4. Can check ranges of values. | 4. Uses fixed `case` values. |
| 5. Can compare strings using functions like `strcmp()`. | 5. Cannot directly switch on strings in C. |
| 6. Does not require `break`. | 6. Usually uses `break` to prevent fall-through. |
| 7. `else` is optional. | 7. `default` is optional. |
| 8. Suitable for complex decision-making. | 8. Suitable for multiple fixed choices. |

## Example 1: `if-else`

```c
int n = 10;

if (n > 0) {
    printf("Positive");
} else {
    printf("Not positive");
}
```

**Output:** `Positive`

Here, `if-else` checks a condition: `n > 0`.

## Example 2: `switch`

```c
int n = 2;

switch (n) {
    case 1:
        printf("One");
        break;
    case 2:
        printf("Two");
        break;
    default:
        printf("Other");
}
```

**Output:** `Two`

Here, `switch` matches `n` with the fixed value `2`.

## Exam Note

**Use `if-else`** when checking conditions, ranges, or complex expressions.

**Use `switch`** when selecting from multiple fixed values.

বাংলায়: `if-else` শর্ত যাচাই করে, আর `switch` নির্দিষ্ট মানের সঙ্গে মিলিয়ে সিদ্ধান্ত নেয়।
<img width="631" height="493" alt="image" src="https://github.com/user-attachments/assets/cd88e45d-963e-4cb5-b0de-5ce6ce27b068" />
# `goto` Statement in C

## Definition
The `goto` statement is used to jump directly to a labeled statement in a program.

**বাংলা:** `goto` ব্যবহার করে প্রোগ্রামের এক স্থান থেকে অন্য নির্দিষ্ট স্থানে যাওয়া যায়।

## Syntax
```c
goto label;

label:
    // Code
```

## Example
```c
#include <stdio.h>

int main() {
    printf("Hello\n");

    goto end;

    printf("World\n");

    end:
        printf("End");

    return 0;
}
```

**Output:**
```text
Hello
End
```

## Explanation
- `goto end;` jumps to the `end` label.
- `printf("World\n");` is skipped.
- `end:` is the target label.

## Important Points
- `goto` jumps to a labeled statement.
- A label ends with a colon (`:`).
- The label must be inside the same function.
- Excessive use of `goto` makes code difficult to understand.

**Remember:** `goto` = Jump to a label.
# Loop in C

## Definition
A **loop** is used to execute a block of code repeatedly while a condition is true.

**বাংলা:** একই কোড বারবার চালানোর জন্য loop ব্যবহার করা হয়।

## Types of Loops in C

| Loop | Purpose |
|---|---|
| `for` | Repeats code a specified number of times |
| `while` | Repeats code while a condition is true |
| `do-while` | Executes code at least once, then checks the condition |

## 1. `for` Loop

**Syntax:**
```c
for (initialization; condition; update) {
    // Code
}
```

**Example:**
```c
for (int i = 1; i <= 5; i++) {
    printf("%d\n", i);
}
```

**Output:**
```text
1
2
3
4
5
```

## 2. `while` Loop

**Syntax:**
```c
while (condition) {
    // Code
}
```

**Example:**
```c
int i = 1;

while (i <= 5) {
    printf("%d\n", i);
    i++;
}
```

**Output:**
```text
1
2
3
4
5
```

## 3. `do-while` Loop

**Syntax:**
```c
do {
    // Code
} while (condition);
```

**Example:**
```c
int i = 1;

do {
    printf("%d\n", i);
    i++;
} while (i <= 5);
```

**Output:**
```text
1
2
3
4
5
```

## Difference Between Loops

| `for` | `while` | `do-while` |
|---|---|---|
| Condition is checked first | Condition is checked first | Condition is checked after execution |
| Suitable when repetitions are known | Suitable when repetitions depend on a condition | Executes at least once |

## Important Points
- `break` stops the loop.
- `continue` skips the current iteration and moves to the next one.
- An infinite loop continues running without stopping.
- `do-while` always executes its body at least once.

**Remember:** A loop repeats code and reduces code duplication.
<img width="926" height="662" alt="image" src="https://github.com/user-attachments/assets/3c8f9415-73c7-4054-9aec-bc1486cd61d1" />

# Difference Between `while` and `do-while` Loop in C

## Definition

- **`while` loop:** Checks the condition first, then executes the code if the condition is true.
- **`do-while` loop:** Executes the code first, then checks the condition.

## Differences

| `while` Loop | `do-while` Loop |
|---|---|
| 1. Entry-controlled loop. | 1. Exit-controlled loop. |
| 2. Checks the condition before execution. | 2. Checks the condition after execution. |
| 3. May execute zero times. | 3. Executes at least once. |
| 4. No semicolon after the condition's closing `)`. | 4. Requires a semicolon after `while (condition);`. |
| 5. Used when the condition must be checked first. | 5. Used when the code must execute at least once. |

## Example 1: `while` Loop

```c
int i = 1;

while (i <= 3) {
    printf("%d\n", i);
    i++;
}
```

**Output:**
```text
1
2
3
```

## Example 2: `do-while` Loop

```c
int i = 1;

do {
    printf("%d\n", i);
    i++;
} while (i <= 3);
```

**Output:**
```text
1
2
3
```

## Important Example: Condition Is False

**`while` loop:**
```c
int i = 5;

while (i < 3) {
    printf("Hello");
}
```

Output: No output.

**`do-while` loop:**
```c
int i = 5;

do {
    printf("Hello");
} while (i < 3);
```

Output:
```text
Hello
```

**Remember:** `while` checks first; `do-while` executes first and checks afterward.
# Difference Between `break` and `continue` in C

## Definition

- **`break`:** Stops the loop completely.
- **`continue`:** Skips the remaining code of the current iteration and moves to the next iteration.

বাংলা:
- `break` = সম্পূর্ণ loop বন্ধ করে।
- `continue` = বর্তমান iteration বাদ দিয়ে পরের iteration-এ যায়।

## Differences

| `break` | `continue` |
|---|---|
| 1. Terminates the loop. | 1. Skips the current iteration. |
| 2. Control moves outside the loop. | 2. Control moves to the next iteration. |
| 3. Stops further iterations. | 3. The loop continues with the next iteration. |
| 4. Used in loops and `switch`. | 4. Used in loops. |

## Example 1: `break`

```c
#include <stdio.h>

int main() {
    for (int i = 1; i <= 5; i++) {
        if (i == 3) {
            break;
        }
        printf("%d\n", i);
    }
    return 0;
}
```

**Output:**
```text
1
2
```

**Explanation:** When `i == 3`, `break` stops the loop completely.

## Example 2: `continue`

```c
#include <stdio.h>

int main() {
    for (int i = 1; i <= 5; i++) {
        if (i == 3) {
            continue;
        }
        printf("%d\n", i);
    }
    return 0;
}
```

**Output:**
```text
1
2
4
5
```

**Explanation:** When `i == 3`, `continue` skips printing `3`, but the loop continues.

## Remember

- `break` → **Stop the loop.**
- `continue` → **Skip the current iteration.**
- # Parameter in C

## Definition
A **parameter** is a variable declared in a function to receive a value when the function is called.

**বাংলা:** Function-এর মধ্যে যে variable value গ্রহণ করে, তাকে parameter বলে।

## Example

```c
#include <stdio.h>

void add(int a, int b) {
    printf("%d", a + b);
}

int main() {
    add(10, 20);
    return 0;
}
```

**Output:**
```text
30
```

## Explanation

- `a` and `b` are parameters.
- `10` and `20` are arguments.
- `add(10, 20)` is a function call.

## Difference Between Parameter and Argument

| Parameter | Argument |
|---|---|
| Variable declared in a function definition | Value or expression passed during a function call |
| Receives the supplied value | Supplies the value |
| Example: `int a` | Example: `10` |

## Types of Parameters

1. **Formal Parameter:** Variable declared in the function definition.
2. **Actual Argument:** Value or expression supplied in the function call.

**Remember:** Parameter = Receiving variable; Argument = Supplied value.
# Call by Value and Call by Reference in C

## 1. Call by Value

### Definition
**Call by Value** means passing a copy of a variable's value to a function.

বাংলা: Variable-এর value-এর একটি কপি function-এ পাঠানো হয়। তাই function-এর ভিতরে পরিবর্তন করলে original variable পরিবর্তন হয় না।

### Example

```c
#include <stdio.h>

void change(int x) {
    x = 100;
}

int main() {
    int a = 10;

    change(a);

    printf("%d", a);

    return 0;
}
```

**Output:**
```text
10
```

### Explanation
1. `a = 10` — The original variable contains `10`.
2. `change(a)` — A copy of `a` is passed to `x`.
3. `x = 100` — Only `x` changes.
4. `a` remains `10`.

| Variable | Value |
|---|---:|
| `a` (original) | 10 |
| `x` (copy after change) | 100 |

---

## 2. Call by Reference

### Definition
**Call by Reference** means accessing the original variable through a reference so that changes affect the original variable.

বাংলা: Original variable-কে সরাসরি পরিবর্তন করার জন্য তার reference বা address ব্যবহার করা হয়।

**Important:** C does not support true call by reference directly. We can achieve the same effect using pointers.

### Example in C (Using Pointers)

```c
#include <stdio.h>

void change(int *x) {
    *x = 100;
}

int main() {
    int a = 10;

    change(&a);

    printf("%d", a);

    return 0;
}
```

**Output:**
```text
100
```

### Explanation
1. `a = 10` — The original variable contains `10`.
2. `change(&a)` — The address of `a` is passed to the function.
3. `int *x` — The pointer `x` receives that address.
4. `*x = 100` — The value at that address changes to `100`.
5. Therefore, `a` becomes `100`.

| Expression | Meaning |
|---|---|
| `&a` | Address of variable `a` |
| `int *x` | Pointer variable that stores an address |
| `*x` | Value at the address stored in `x` |

---

## 3. Difference Between Call by Value and Call by Reference
<img width="636" height="581" alt="image" src="https://github.com/user-attachments/assets/31df3109-8fe1-42ff-b46c-bd47047d0a33" />
<img width="671" height="564" alt="image" src="https://github.com/user-attachments/assets/c45e3057-6b25-4d0c-a4db-c4e4cb6995cf" />


| Call by Value | Call by Reference (Using Pointers in C) |
|---|---|
| Passes a copy of the value. | Passes the variable's address by value. |
| Original variable remains unchanged when the parameter changes. | Original variable can be changed through the pointer. |
| Uses ordinary parameters. | Uses pointer parameters. |
| Function call: `change(a)` | Function call: `change(&a)` |
| Example output: `10` | Example output: `100` |

## Important Points
- C always passes function arguments by value.
- Call by Value passes an ordinary value.
- Pointer-based modification passes an address as a pointer value.
- `&` gets a variable's address.
- `*` accesses the value at the stored address.

## Remember
- **Call by Value:** Changes affect the copy.
- **Pointer-based reference:** Changes through the pointer affect the original variable.
  <img width="811" height="545" alt="image" src="https://github.com/user-attachments/assets/0e0feff6-9b83-44f0-a977-213d5f35f1e0" />
  <img width="1013" height="543" alt="image" src="https://github.com/user-attachments/assets/9d1b79d9-c2b1-4906-92f9-9ecf0c9ffa21" />
  <img width="1077" height="505" alt="image" src="https://github.com/user-attachments/assets/3aacde15-822f-4cc1-b936-369ead8ee889" />
  <img width="1018" height="476" alt="image" src="https://github.com/user-attachments/assets/49dd83d4-f726-4bc8-a0c5-527f215f2925" />


# Initial Values of Data Types in C

## Definition
The initial value of a variable depends on where it is declared and whether an initial value is assigned.

## Initial Value Table

| Data Type | Local Variable (Uninitialized) | Global Variable | Static Variable |
|---|---|---|---|
| `int` | Indeterminate | `0` | `0` |
| `float` | Indeterminate | `0.0` | `0.0` |
| `char` | Indeterminate | `'\0'` | `'\0'` |
| `double` | Indeterminate | `0.0` | `0.0` |

## Example 1: Global Variables

```c
#include <stdio.h>

int a;
float b;
char c;
double d;

int main() {
    printf("%d\n", a);
    printf("%f\n", b);
    printf("%d\n", c);
    printf("%f\n", d);

    return 0;
}
```

**Output:**
```text
0
0.000000
0
0.000000
```

## Example 2: Static Variables

```c
#include <stdio.h>

int main() {
    static int a;
    static float b;
    static char c;
    static double d;

    printf("%d\n", a);
    printf("%f\n", b);
    printf("%d\n", c);
    printf("%f\n", d);

    return 0;
}
```

**Output:**
```text
0
0.000000
0
0.000000
```

## Important Points

- **Local variable:** An uninitialized local variable has an indeterminate value. Reading it may cause undefined behavior.
- **Global variable:** Automatically initialized to zero.
- **Static variable:** Automatically initialized to zero.
- `'\0'` is the null character, with numeric value `0`.
- `printf("%f", b)` prints a `float` value; `float` is promoted to `double` in a variadic function call.
- `printf("%f", d)` prints a `double` value.

## Remember

- Local uninitialized variable → Indeterminate value
- Global variable → Zero-initialized
- Static variable → Zero-initialized

**Exam Note:** In C, variables with static storage duration, including global and static variables, are initialized to zero by default. Uninitialized automatic local variables have indeterminate values.
