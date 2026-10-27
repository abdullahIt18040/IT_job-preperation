<img width="815" height="566" alt="image" src="https://github.com/user-attachments/assets/ad6d5644-eca0-487f-969e-68450ca09db7" /># Structured Programming vs OOP
<img width="996" height="505" alt="image" src="https://github.com/user-attachments/assets/3032c44d-ea86-4841-8d40-d76b6a247de6" />
<img width="965" height="508" alt="image" src="https://github.com/user-attachments/assets/896242e9-5d01-4aa6-98a6-59dcc0b3d1f6" />

## 1. Structured Programming
<img width="875" height="459" alt="image" src="https://github.com/user-attachments/assets/3d6b7069-a09a-4d56-999d-49378de7845e" />
<img width="1005" height="546" alt="image" src="https://github.com/user-attachments/assets/9cabe79b-8f4b-43f6-b97e-e7f1a2fc582a" />

**Definition:** Structured Programming is a programming method that divides a program into small functions.

**বাংলা:** প্রোগ্রামকে ছোট ছোট Function-এ ভাগ করে লেখাকে Structured Programming বলে।

**Example:** C

```c
int add(int a, int b) {
    return a + b;
}
```

**Features:**
- Focuses on functions.
- Generally follows a top-down approach.
- Easy to understand and debug.

## 2. Object-Oriented Programming (OOP)

**Definition:** OOP is a programming method based on classes and objects.

**বাংলা:** Class ও Object ব্যবহার করে প্রোগ্রাম লেখাকে OOP বলে।

**Example:** Java

```java
class Student {
    String name;

    void study() {
        System.out.println("Studying");
    }
}
```

**Features:**
- Focuses on classes and objects.
- Combines data and methods.
- Supports code reuse.
- Helps manage large programs.

## 3. Differences

| Structured Programming | OOP |
|---|---|
| Focuses on functions | Focuses on objects |
| Generally top-down | Generally bottom-up |
| Data and functions are usually separate | Data and methods can be combined |
| Example: C | Example: Java, C++ |

## 4. Four Pillars of OOP

1. **Encapsulation:** Combining data and methods.
2. **Inheritance:** Reusing features of another class.
3. **Polymorphism:** One interface, different behaviors.
4. **Abstraction:** Hiding implementation details.

## Exam Note

**Remember:**
- Structured Programming = Functions
- OOP = Classes + Objects
- C = Procedural programming example
- Java = Object-oriented programming example


# Variable in Programming

## Definition
A **variable** A variable is a name used to store data in a program.
## Syntax (Java)
```java
dataType variableName = value;
```

Example:
```java
int age = 25;
String name = "Abdullah";
double salary = 25000.50;
```

## Types of Variables in Java
# Local and Global Variables in C

## 1. Local Variable
A **local variable** is declared inside a function and can be used only within its scope.

**বাংলা:** Function-এর ভিতরে declare করা variable হলো Local Variable।

```c
void test() {
    int a = 10; // Local variable
}
```

## 2. Global Variable
A **global variable** is declared outside all functions and we can access it entire or throughout the program .

**বাংলা:** সব function-এর বাইরে declare করা variable হলো Global Variable।

```c
int a = 10; // Global variable

void test() {
    printf("%d", a);
}
```

## Difference

| Local Variable | Global Variable |
|---|---|
| Declared inside a function or block | Declared outside all functions |
| Limited to its scope | Accessible throughout its scope |
| No automatic default value | Automatically initialized to `0` if not explicitly initialized (for arithmetic types) |
| Usually exists while its block executes | Exists for the entire program execution |

**Remember:**
- Local = Inside a function/block.
- Global = Outside all functions.
### 1. Local Variable
- Declared inside a method, constructor, or block.
- Must be initialized before use.

```java
void display() {
    int age = 25;
    System.out.println(age);
}
```

### 2. Instance Variable
- Declared inside a class but outside methods.
- Each object has its own instance variable.

```java
class Student {
    String name;
}
```

### 3. Static (Class) Variable
- Declared using the `static` keyword.
- Shared by all objects of the class.

```java
class Student {
    static String university = "MBSTU";
}
```

## Variable Declaration vs Initialization

```java
int age;       // Declaration
age = 25;      // Initialization
```

Both can be done together:

```java
int age = 25;
```

## Rules for Naming Variables
<img width="930" height="494" alt="image" src="https://github.com/user-attachments/assets/b8ba5bf0-7ff2-4283-8e0e-b8ad424da0a8" />

- Must not start with a digit.
- Cannot contain spaces.
- Cannot use Java reserved keywords.
- only  Can contain letters, digits, `_`, and `$`.
- - Cannot contain - ,&,% etc hypen.
- Java variable names are case-sensitive (`age` and `Age` are different).
- Use camelCase by convention.

# Operator in Programming
# Operator in Programming

## Definition
An **operator** is a symbol used to perform an operation on data.

**বাংলা:** Operator হলো কোনো কাজ করার প্রতীক।
<img width="867" height="538" alt="image" src="https://github.com/user-attachments/assets/adfba9c2-0ef5-4d1b-98e6-24bf2e065c21" />

Example:
```java
int sum = 10 + 5;
```
Here, `+` is an operator used for addition.

## Types of Operators

1. **Arithmetic:** `+`, `-`, `*`, `/`, `%`
2. **Relational:** `==`, `!=`, `>`, `<`, `>=`, `<=`
3. **Logical:** `&&`, `||`, `!`
4. **Assignment:** `=`, `+=`, `-=`
5. **Unary:** `++`, `--`
6. **Bitwise:** `&`, `|`, `^`, `~`, `<<`, `>>`, `>>>`

### Bitwise Operators

Bitwise operators perform operations on the individual bits of numbers.

Example in Java:
```java
int a = 5;  // Binary: 0101
int b = 3;  // Binary: 0011

System.out.println(a & b);  // 1
System.out.println(a | b);  // 7
System.out.println(a ^ b);  // 6
```

- `&` — Bitwise AND
- `|` — Bitwise OR
- `^` — Bitwise XOR
- `~` — Bitwise NOT
- `<<` — Left shift
- `>>` — Signed right shift
- `>>>` — Unsigned right shift
<img width="635" height="407" alt="image" src="https://github.com/user-attachments/assets/94f5813a-6c3d-41b5-9ee6-b2d18b44ebd3" />
<img width="1013" height="537" alt="image" src="https://github.com/user-attachments/assets/a1d52b11-8c5a-49d2-9e73-e3902ff4710b" />
<img width="862" height="523" alt="image" src="https://github.com/user-attachments/assets/4e1ff402-bd30-410e-8e39-faf311d70581" />

# Difference Between `a++` and `++a`
++a ,pre inrement
a++ ,post increment.
- `a++` → Use first, then increase by 1.
- `++a` → Increase by 1, then use.

### Example

```java
int a = 5;

System.out.println(a++); // 5
System.out.println(++a); // 7
```

**বাংলা:**
- `a++` → আগে ব্যবহার, পরে বাড়ে।
- `++a` → আগে বাড়ে, পরে ব্যবহার।


<img width="633" height="413" alt="image" src="https://github.com/user-attachments/assets/fafd9027-2c34-4b80-9977-ffa73c9b3003" />
<img width="622" height="427" alt="image" src="https://github.com/user-attachments/assets/63a15315-6426-4607-9d5f-a9ba5da0ee98" />
<img width="761" height="475" alt="image" src="https://github.com/user-attachments/assets/097e2ea2-97a7-4852-ae0e-39cde10db6c4" />
# Types of Data Types in Java

## 1. Basic (Primitive) Data Types
Built-in data types provided by Java.

Examples: `int`, `float`, `double`, `char`, `boolean`, `byte`, `short`, `long`

```java
int age = 25;
char grade = 'A';
```

## 2. User-Defined Data Types
Data types created by the programmer.

Examples: `class`, `interface`, `enum`, `record`

```java
class Student {
    String name;
}
```

## 3. Derived Data Types
Data types formed using other data types or reference types.

Examples: Arrays and Classes.

```java
int[] numbers = {1, 2, 3};
```

**বাংলায় মনে রাখো:**
- **Basic:** Java-তে আগে থেকেই আছে।
- **User-defined:** Programmer তৈরি করে।
- **Derived:** অন্য data type ব্যবহার করে তৈরি বা গঠন করা হয়।

<img width="1007" height="452" alt="image" src="https://github.com/user-attachments/assets/770a78b9-ed02-416f-aa94-8a36a950112c" />

<img width="620" height="383" alt="image" src="https://github.com/user-attachments/assets/1c8f577f-fc49-4798-b373-eec063040ee9" />
# Basic Data Types in Java

**Definition:** Basic data types store simple values.

**বাংলা:** Basic data type দিয়ে সাধারণ ডেটা রাখা হয়।

| Data Type | Example | Use |
|---|---|---|
| `byte` | `byte a = 10;` | Small integer |
| `short` | `short a = 100;` | Integer |
| `int` | `int age = 25;` | Integer |
| `long` | `long n = 1000L;` | Large integer |
| `float` | `float x = 2.5f;` | Decimal |
| `double` | `double x = 5.25;` | Decimal |
| `char` | `char c = 'A';` | Single character |
| `boolean` | `boolean b = true;` | True or false |

**Remember:** Java has **8 primitive data types**.
# User-Defined Data Types in Java

**Definition:** User-defined data types are created by programmers.

**বাংলা:** Programmer নিজের প্রয়োজন অনুযায়ী যে data type তৈরি করে, তাকে User-Defined Data Type বলে।
<img width="815" height="566" alt="image" src="https://github.com/user-attachments/assets/1b366f01-dfe1-497b-a9fb-31c0eb7b1c0e" />
# Union in C

## Definition
A **union** is a user-defined data type where all members share the same memory location.

**বাংলা:** Union-এ সব member একই memory ব্যবহার করে।

## Example

```c
#include <stdio.h>

union Data {
    int a;
    float b;
};

int main() {
    union Data d;
    d.a = 10;

    printf("%d", d.a);
    return 0;
}
```

**Output:**
```text
10
```

## Key Points
- All members share the same memory.
- Only one member's stored value should be relied on at a time.
- Union size is generally the size of its largest member, adjusted for alignment.
- It saves memory compared with a structure that stores all members separately.

## Union vs Structure

| Union | Structure |
|---|---|
| Shares memory among members | Each member has separate storage |
| Stores one member's value reliably at a time | Can store values in all members simultaneously |
| Usually uses less memory | Usually uses more memory |

**Remember:** `union` = shared memory.
## Examples

1. **Class**
2. **Interface**
3. **Enum**
4. **Record**

### Example

```java
class Student {
    String name;
    int age;
}
```

Here, `Student` is a user-defined type.

**Remember:** A programmer creates user-defined data types.
# Derived Data Types

**Definition:** Derived data types are formed using other data types.

**বাংলা:** অন্য data type ব্যবহার করে যে data type তৈরি করা হয়, তাকে Derived Data Type বলে।

## Examples in Java

1. **Array**
```java
int[] numbers = {10, 20, 30};
```

2. **Class**
```java
class Student {
    int age;
}
```

3. **Interface**
```java
interface Animal {
    void sound();
}
```

**Remember:** Array, class, and interface are reference types in Java. “Derived data type” is a general programming term, not an official Java category.
# Pointer in C

## Definition
A **pointer** is a variable that stores the memory address of another variable.

**বাংলা:** Pointer হলো এমন একটি variable, যা অন্য variable-এর memory address রাখে।

<img width="918" height="485" alt="image" src="https://github.com/user-attachments/assets/9f29a238-99b2-4941-a274-6b9ecbe5d020" />
## Example

```c
int a = 10;
int *p = &a;
```

- `a` → stores value `10`.
- `&a` → gives the address of `a`.
- `p` → stores the address of `a`.
- `*p` → accesses the value `10`.

## Remember
- `&` → Address of a variable.
- `*` → Pointer declaration or accessing the value at an address.

**Note:** Java does not support explicit pointers like C/C++. Java uses references instead.

# Enum in C

## Definition
An **enum** is a user-defined data type that contains a set of named integer constants.

**বাংলা:** Enum হলো কিছু নির্দিষ্ট integer value-কে নাম দেওয়ার পদ্ধতি।

## Example

```c
#include <stdio.h>

enum Day {
    SUN, MON, TUE, WED
};

int main() {
    enum Day today = MON;
    printf("%d", today);
    return 0;
}
```

**Output:**
```text
1
```

## Key Points
- `enum` means enumeration.
- By default, the first value is `0`.
- Each next value increases by `1`.
- You can assign custom integer values.

## Example with Custom Values

```c
enum Status {
    FAIL = 0,
    PASS = 1
};
```

**Remember:** `enum` gives names to integer constants.
# Function in C

## Definition
A **function** is a block of code that performs a specific task.

**বাংলা:** Function হলো কোডের একটি অংশ, যা নির্দিষ্ট কাজ করে।
<img width="1045" height="482" alt="image" src="https://github.com/user-attachments/assets/db593471-e4d2-4803-9949-c0edf27860a8" />

## Example

```c
#include <stdio.h>

void greet() {
    printf("Hello!");
}

int main() {
    greet();
    return 0;
}
```

**Output:**
```text
Hello!
```

## Types of Functions
1. **Library Function:** `printf()`, `scanf()`, `strlen()`
2. **User-Defined Function:** Created by the programmer.

**Remember:** A function helps reuse code and avoid repetition.
<img width="1034" height="509" alt="image" src="https://github.com/user-attachments/assets/1e3aedd3-41d5-4a23-8383-3b59a4cd73b7" />
<img width="926" height="474" alt="image" src="https://github.com/user-attachments/assets/e3466677-d811-4c62-9fb0-b165590ae3c1" />
<img width="925" height="576" alt="image" src="https://github.com/user-attachments/assets/f67ca04c-8c6d-4277-bc0c-1921b6a45202" />
<img width="946" height="491" alt="image" src="https://github.com/user-attachments/assets/191f3248-72de-4b23-a543-1f2340ad87f7" />
<img width="928" height="518" alt="image" src="https://github.com/user-attachments/assets/d2d822a5-8a39-4653-b572-9af9e38177c6" />
<img width="1035" height="550" alt="image" src="https://github.com/user-attachments/assets/35d791d7-8a6c-4a59-ab5a-656fe54a50a0" />

<img width="787" height="295" alt="image" src="https://github.com/user-attachments/assets/0d4e5a56-9ede-47dc-acf6-f67a558e77eb" />


<img width="966" height="463" alt="image" src="https://github.com/user-attachments/assets/d5be62c7-dd11-450a-87ef-f53c573f2438" />


