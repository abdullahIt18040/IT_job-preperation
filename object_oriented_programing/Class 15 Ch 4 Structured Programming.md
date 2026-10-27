# Structured Programming vs OOP

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



