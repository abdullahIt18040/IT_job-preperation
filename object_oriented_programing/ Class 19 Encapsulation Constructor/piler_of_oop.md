
# `this` and `super` Keywords in Java

## 1. What is `this` Keyword?

**Definition:** The `this` keyword refers to the current object of a class.

In simple words, `this` means **নিজের object (Current Object)**.

### Example: Access Instance Variables

```java
class Student {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    void display() {
        System.out.println(this.id);
        System.out.println(this.name);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student(101, "Abdullah");
        s1.display();
    }
}
```

**Output:**
```text
101
Abdullah
```

### Explanation

```java
this.id = id;
```

- `this.id` → Instance variable of the current object.
- `id` → Constructor parameter.
- `this.id = id` → Assigns the parameter value to the instance variable.

**বাংলায়:** যখন class variable এবং constructor parameter-এর নাম একই হয়, তখন তাদের আলাদা করে বোঝানোর জন্য `this` ব্যবহার করি।

### Uses of `this` Keyword

1. To access current class instance variables.
2. To call current class methods.
3. To call current class constructor using `this()`.
4. To pass the current object as an argument.
5. To return the current object from a method.

---
<img width="1013" height="367" alt="image" src="https://github.com/user-attachments/assets/074634f0-4133-4449-9249-d26db479d928" />

## 2. What is `super` Keyword?

**Definition:** The `super` keyword refers to the immediate parent class.

In simple words, `super` means **Parent Class**.

### Example 1: Access Parent Class Variable

```java
class Animal {
    String name = "Animal";
}

class Dog extends Animal {
    String name = "Dog";

    void display() {
        System.out.println(this.name);
        System.out.println(super.name);
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.display();
    }
}
```

**Output:**
```text
Dog
Animal
```

### Explanation

- `this.name` → Dog class's own variable.
- `super.name` → Animal class's variable.

**বাংলায়:** Child class এবং Parent class-এ একই নামের variable থাকলে `super` দিয়ে Parent class-এর variable access করতে পারি।

### Example 2: Call Parent Class Method

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }

    void display() {
        super.sound();
        sound();
    }
}
```

**Output:**
```text
Animal makes sound
Dog barks
```

- `super.sound()` → Calls Parent class method.
- `sound()` → Calls current class method.

### Example 3: Call Parent Class Constructor

```java
class Animal {
    Animal() {
        System.out.println("Animal Constructor");
    }
}

class Dog extends Animal {
    Dog() {
        super();
        System.out.println("Dog Constructor");
    }
}
```

**Output:**
```text
Animal Constructor
Dog Constructor
```

**Explanation:**

- `super()` calls the immediate parent class constructor.
- Parent constructor executes before child constructor.

---

## 3. Difference Between `this` and `super`

| `this` | `super` |
|---|---|
| Refers to the current object. | Refers to the immediate parent class. |
| Accesses current class variables. | Accesses parent class variables. |
| Calls current class methods. | Calls parent class methods. |
| `this()` calls current class constructor. | `super()` calls parent class constructor. |
| Used within a class to refer to itself. | Used in a child class to access parent members. |

---

## 4. Important Points for Job Exams

1. `this` refers to the current object.
2. `super` refers to the immediate parent class.
3. `this()` calls the current class constructor.
4. `super()` calls the parent class constructor.
5. `this()` must be the first statement in a constructor.
6. `super()` must be the first statement in a constructor.
7. We cannot explicitly use both `this()` and `super()` in the same constructor.
8. `this` and `super` cannot be used directly inside static methods.
9. Java automatically inserts `super()` if no constructor invocation is explicitly provided and a no-argument parent constructor is accessible.

---

## 5. Easy Way to Remember

- **`this` = আমি (Current Object)**
- **`super` = আমার Parent (Parent Class)**

```text
        Animal (Parent Class)
               |
               |
          Dog (Child Class)
```

Inside the Dog class:

- `this` → Dog object.
- `super` → Animal parent-class members.

---

## 6. Quick Revision

| Keyword | Meaning |
|---|---|
| `this` | Current Object |
| `super` | Immediate Parent Class |
| `this.variable` | Current class variable |
| `super.variable` | Parent class variable |
| `this.method()` | Current class method |
| `super.method()` | Parent class method |
| `this()` | Current class constructor |
| `super()` | Parent class constructor |

**Remember:** `this` means current object, and `super` means immediate parent class.
# Constructor in Java

## 1. What is a Constructor?

**Definition:** A constructor is a special member of a class that is automatically called when an object is created. It is used to initialize an object.

**বাংলায়:** Constructor হলো class-এর একটি special member, যা object তৈরি হওয়ার সময় automatically execute হয় এবং object-এর initial value set করতে ব্যবহৃত হয়।

### Example

```java
class Student {
    int id;
    String name;

    // Constructor
    Student() {
        id = 101;
        name = "Abdullah";
    }

    void display() {
        System.out.println(id);
        System.out.println(name);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();
        s1.display();
    }
}
```

**Output:**
```text
101
Abdullah
```

### How Does a Constructor Work?

```java
Student s1 = new Student();
```

1. `new` creates a new object.
2. Constructor is automatically called.
3. Constructor code is executed.
4. Instance variables are initialized.

---

## 2. Rules of Constructor

1. Constructor name must be the same as the class name.
2. Constructor has no return type, not even `void`.
3. Constructor is automatically called during object creation.
4. Constructors cannot be inherited.
5. Constructors can be overloaded.
6. Constructors cannot be `static`, `final`, or `abstract`.
7. If no constructor is declared, the Java compiler provides a default constructor.
8. Constructors cannot be overridden.

---

## 3. Types of Constructors

### A. Default Constructor

**Definition:** If a programmer does not declare any constructor, the Java compiler automatically provides a default constructor.

```java
class Student {
    int id;
    String name;
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();

        System.out.println(s1.id);
        System.out.println(s1.name);
    }
}
```

**Output:**
```text
0
null
```

**Note:** Java provides default values to instance variables. A default constructor initializes them with their default values.

### B. No-Argument Constructor

**Definition:** A constructor that does not accept any parameters is called a no-argument constructor.

```java
class Student {
    int id;

    Student() {
        id = 101;
    }
}
```

**Note:** A programmer can explicitly create a no-argument constructor. It is not necessarily a compiler-provided default constructor.

### C. Parameterized Constructor

**Definition:** A constructor that accepts parameters is called a parameterized constructor.

```java
class Student {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    void display() {
        System.out.println(id);
        System.out.println(name);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student(101, "Abdullah");
        Student s2 = new Student(102, "Mamun");

        s1.display();
        s2.display();
    }
}
```

**Output:**
```text
101
Abdullah
102
Mamun
```

**Explanation:**
- `this.id` → Instance variable.
- `id` → Constructor parameter.
- `this.id = id` → Assigns the parameter value to the instance variable.

---

## 4. Constructor Overloading

**Definition:** When a class contains multiple constructors with different parameter lists, it is called constructor overloading.

```java
class Student {
    int id;
    String name;

    Student() {
        id = 0;
        name = "Unknown";
    }

    Student(int id) {
        this.id = id;
    }

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }
}
```

**Here:**
- `Student()` → No-argument constructor.
- `Student(int id)` → One-parameter constructor.
- `Student(int id, String name)` → Two-parameter constructor.

---

## 5. Difference Between Constructor and Method

| Constructor | Method |
|---|---|
| Initializes an object. | Performs a specific task. |
| Name must match the class name. | Can have any valid name. |
| Has no return type. | Must have a return type, including `void`. |
| Automatically called during object creation. | Called explicitly or by other code. |
| Cannot be inherited. | Can be inherited. |
| Can be overloaded. | Can be overloaded and overridden (when applicable). |

---

## 6. `this()` and `super()` in Constructor

### A. `this()`

**Definition:** `this()` is used to call another constructor of the same class.

```java
class Student {

    Student() {
        this(101);
        System.out.println("Default Constructor");
    }

    Student(int id) {
        System.out.println("ID: " + id);
    }
}
```

**Output:**
```text
ID: 101
Default Constructor
```

### B. `super()`

**Definition:** `super()` is used to call the immediate parent class constructor.

```java
class Animal {
    Animal() {
        System.out.println("Animal Constructor");
    }
}

class Dog extends Animal {
    Dog() {
        super();
        System.out.println("Dog Constructor");
    }
}
```

**Output:**
```text
Animal Constructor
Dog Constructor
```

**Important:**
- `this()` calls the current class constructor.
- `super()` calls the parent class constructor.
- Both must be the first statement in a constructor when explicitly used.
- Both cannot be explicitly used together in the same constructor.
- If no constructor invocation is specified, Java implicitly inserts `super()` when an accessible no-argument parent constructor exists.

---

## 7. Important Job Exam Points

1. A constructor has no return type.
2. Constructor name must be the same as the class name.
3. Constructors can be overloaded.
4. Constructors cannot be overridden.
5. Constructors cannot be inherited.
6. Abstract classes can have constructors.
7. Interfaces cannot have constructors.
8. Private constructors are allowed in Java.
9. If a programmer declares any constructor, Java does not automatically provide the default constructor.
10. Constructors execute during object creation.
11. Constructors cannot be static, final, or abstract.
12. A constructor can call another constructor using `this()` or `super()`.

---

## 8. Quick Revision

| Term | Meaning |
|---|---|
| Constructor | Initializes an object |
| Default Constructor | Compiler-provided constructor when none is declared |
| No-Argument Constructor | Constructor without parameters |
| Parameterized Constructor | Constructor with parameters |
| Constructor Overloading | Multiple constructors with different parameter lists |
| `this()` | Calls another constructor in the same class |
| `super()` | Calls the immediate parent class constructor |

### Remember

- Constructor = Object Initialization.
- `this()` = Current Class Constructor.
- `super()` = Parent Class Constructor.
- Constructor Overloading = Multiple constructors in one class.
