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
