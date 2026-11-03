
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
