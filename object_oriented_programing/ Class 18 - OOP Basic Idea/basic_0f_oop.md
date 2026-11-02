# Object-Oriented Programming (OOP)

## 1. What is OOP?

**OOP (Object-Oriented Programming)** is a programming paradigm based on the concept of classes and objects.
Paradigm
- বাংলা উচ্চারণ: প্যারাডাইম (প্যা-রা-ডাইম)
- Paradigm = A way or style of doing something.

বাংলায়: কোনো কাজ করার নির্দিষ্ট পদ্ধতি বা ধরণ।
It organizes a program into objects that contain data (attributes) and functions (methods).

OOP helps make programs:
- Reusable
- Maintainable
- Secure
- Modular
- Easy to manage

**Examples of OOP languages:** C++, Java, Python, C#.

## 2. What is a Class?

A **Class** is a blueprint or template for creating objects.

It defines the properties (data members) and behaviors (member functions) of objects.

**Example:** Student, Car, Employee.

```cpp
class Student {
public:
    string name;
    int age;

    void display() {
        cout << name << " " << age;
    }
};
```

## 3. What is an Object?

An **Object** is an instance of a class.

It represents a real-world entity and contains its own data.

**Example:** `s1` and `s2` are objects of the Student class.

```cpp
Student s1;
Student s2;
```
### Question: Does a class occupy memory when it is declared?

**Answer**: A class declaration itself does not allocate memory for its non-static instance data members. Memory for those members is allocated when an object is created.

## 4. Class and Object Example in C++

```cpp
#include <iostream>
using namespace std;

// Class
class Student {
public:
    string name;
    int age;

    void display() {
        cout << "Name: " << name << endl;
        cout << "Age: " << age << endl;
    }
};

int main() {

    // Creating objects
    Student s1;
    Student s2;

    // Assigning values
    s1.name = "Abdullah";
    s1.age = 27;

    s2.name = "Rahim";
    s2.age = 25;

    // Calling methods
    s1.display();
    s2.display();

    return 0;
}
```

**Output:**
```text
Name: Abdullah
Age: 27
Name: Rahim
Age: 25
```

## 5. Difference Between Class and Object

| Class | Object |
|---|---|
| A blueprint or template. | An instance of a class. |
| Defines properties and methods. | Has actual data and uses methods. |
| Logical concept. | Runtime entity. |
| when declar class no need memory | when Object initialized it allocate  memory. |
| Declared using `class` keyword. | Created using the class name. |
| Example: Student | Example: s1, s2 |

## 6. Important Terms

- **Data Members:** Variables declared inside a class.
- **Member Functions:** Functions declared inside a class.
- **Instance:** An object created from a class.
- **State:** The current data or values of an object.
- **Behavior:** The actions an object can perform.

## 7. Real-Life Example

Think about a house:

- Class = House blueprint.
- Object = Actual house built using that blueprint.

One class can create multiple objects, and each object can have different values.

## 8. Four Main Pillars of OOP

1. **Encapsulation:** Wrapping data and methods into a single unit (class).
2. **Inheritance:** Acquiring properties and methods from another class.
3. **Polymorphism:** One interface with different forms of behavior.
4. **Abstraction:** Hiding implementation details and showing essential features.

## 9. Important Points for Job Exams

1. OOP stands for Object-Oriented Programming.
2. OOP is based on classes and objects.
3. Class is a blueprint for creating objects.
4. Object is an instance of a class.
5. `class` is the keyword used to declare a class in C++.
6. One class can create multiple objects.
7. Four pillars of OOP are Encapsulation, Inheritance, Polymorphism, and Abstraction.
8. Java and C++ are object-oriented programming languages.

<img width="737" height="605" alt="image" src="https://github.com/user-attachments/assets/13934efc-0eb3-400a-af54-21de60f4b559" />

<img width="1200" height="655" alt="image" src="https://github.com/user-attachments/assets/37f65acb-24de-40ce-869f-949a8b1509a0" />
<img width="1080" height="622" alt="image" src="https://github.com/user-attachments/assets/382381e8-d5f7-4d3a-a6ca-6a32b08aae80" />
<img width="941" height="622" alt="image" src="https://github.com/user-attachments/assets/b5afeb7a-97e8-4530-91e6-a13f1db078e2" />
<img width="588" height="468" alt="image" src="https://github.com/user-attachments/assets/65e310a4-35f0-4eaa-91f9-011945f0bb6a" />
# Four Pillars of OOP (Object-Oriented Programming)

## 1. What is OOP?

**Object-Oriented Programming (OOP)** is a programming paradigm based on the concept of classes and objects. It models real-world entities as objects that contain data (attributes) and behavior (methods).

OOP helps developers build reusable, maintainable, secure, and flexible applications.

## 2. Four Pillars of OOP

The four fundamental pillars of Object-Oriented Programming are:

1. Inheritance
2. Polymorphism
3. Encapsulation
4. Abstraction

---

## 3. Inheritance

**Definition:**

Inheritance is a mechanism in which one class acquires the properties and methods of another class.

- Parent Class (Superclass): The class whose properties are inherited.
- Child Class (Subclass): The class that inherits properties from another class.

**Java Example:**

```java
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();

        dog.eat();  // Inherited method
        dog.bark();
    }
}
```

**Output:**

```text
Animal is eating
Dog is barking
```

**Benefits:**
- Code reusability
- Reduces code duplication
- Supports method overriding
- Improves code organization

**Types of Inheritance:**
1. Single Inheritance
2. Multilevel Inheritance
3. Hierarchical Inheritance
4. Multiple Inheritance (not directly supported through Java classes)
5. Hybrid Inheritance (possible through interfaces)

---
<img width="1196" height="650" alt="image" src="https://github.com/user-attachments/assets/dd2be8ab-e4c5-4ba7-8a16-abbcc801dfec" />
# Diamond Problem in Inheritance (OOP)

## 1. What is the Diamond Problem?

The **Diamond Problem** is an ambiguity problem that occurs in multiple inheritance when a derived class inherits the same base class through two or more different paths.

It is called the Diamond Problem because the inheritance structure resembles a diamond shape.

## 2. Diamond Problem Structure

```text
        A
       / \
      B   C
       \ /
        D
```

Explanation:

- Class A is the base (parent) class.
- Class B inherits from class A.
- Class C inherits from class A.
- Class D inherits from both B and C.
- As a result, class D receives two inheritance paths from class A.

## 3. Diamond Problem in C++

C++ supports multiple inheritance through classes, so the Diamond Problem can occur.

### Example: Without Virtual Inheritance

```cpp
#include <iostream>
using namespace std;

class A {
public:
    void display() {
        cout << "Class A" << endl;
    }
};

class B : public A {
};

class C : public A {
};

class D : public B, public C {
};

int main() {
    D obj;

    obj.display(); // Compilation Error

    return 0;
}
```

**Why does the compilation error occur?**

Class D inherits class A through two different paths:

1. D → B → A
2. D → C → A

Therefore, class D contains two separate copies of class A.

When we call:

```cpp
obj.display();
```

The compiler cannot determine which `display()` method should be called.

This creates an ambiguity problem.

We can resolve it explicitly using:

```cpp
obj.B::display();
obj.C::display();
```

However, this does not remove the duplicate base-class instances.

## 4. Solution: Virtual Inheritance in C++

We can solve the Diamond Problem using **Virtual Inheritance**.

Virtual inheritance ensures that only one shared instance of the common base class is inherited by the final derived class.

### Example: With Virtual Inheritance

```cpp
#include <iostream>
using namespace std;

class A {
public:
    void display() {
        cout << "Class A" << endl;
    }
};

class B : virtual public A {
};

class C : virtual public A {
};

class D : public B, public C {
};

int main() {
    D obj;

    obj.display();

    return 0;
}
```

**Output:**

```text
Class A
```

### How does it work?

- Class B virtually inherits class A.
- Class C virtually inherits class A.
- Class D inherits both B and C.
- Both inheritance paths share one common instance of class A.

Therefore, ambiguity is removed.

## 5. How Java Handles the Diamond Problem

Java does not support multiple inheritance through classes.

For example, the following code is invalid:

```java
class A {
}

class B extends A {
}

class C extends A {
}

// Invalid Java
class D extends B, C {
}
```

Java avoids this class-based Diamond Problem by allowing a class to extend only one class.

However, Java supports multiple inheritance through interfaces.

### Diamond Problem with Java Interfaces

```java
interface A {
    default void display() {
        System.out.println("Interface A");
    }
}

interface B extends A {
}

interface C extends A {
}

class D implements B, C {
}

public class Main {
    public static void main(String[] args) {
        D obj = new D();
        obj.display();
    }
}
```

**Output:**

```text
Interface A
```

In this example, both interfaces inherit the same default method from A, so there is no conflict.

If B and C independently override the same default method, class D must override it to resolve the conflict.

## 6. C++ vs Java: Diamond Problem

| Feature | C++ | Java |
|---|---|---|
| Multiple inheritance through classes | Supported | Not supported |
| Diamond Problem | Possible | Avoided for classes |
| Solution | Virtual inheritance | Interface method overriding |
| Multiple interfaces | Supported | Supported |
| Shared base-class instance | Virtual inheritance | Not applicable to class inheritance |

## 7. Advantages of Virtual Inheritance

- Prevents duplicate copies of a common base class.
- Resolves ambiguity in diamond-shaped inheritance.
- Allows multiple inheritance while sharing a common base-class instance.
- Improves memory efficiency in applicable inheritance structures.

## 8. Important Job Exam Questions (MCQ / Viva)

**Q1. What is the Diamond Problem?**

Answer: An ambiguity problem that occurs in multiple inheritance when a derived class inherits the same base class through multiple paths.

**Q2. Which OOP concept is associated with the Diamond Problem?**

Answer: Multiple Inheritance.

**Q3. Which programming language supports virtual inheritance?**

Answer: C++.

**Q4. How can we solve the Diamond Problem in C++?**

Answer: By using virtual inheritance.

**Q5. Does Java support multiple inheritance through classes?**

Answer: No.

**Q6. Why is it called the Diamond Problem?**

Answer: Because the inheritance structure resembles a diamond shape.

**Q7. What happens if virtual inheritance is not used in C++?**

Answer: The derived class may contain multiple copies of the common base class, resulting in ambiguity.

**Q8. Can Java interfaces support multiple inheritance?**

Answer: Yes, a Java class can implement multiple interfaces.

**Q9. How does Java resolve conflicting default methods from two interfaces?**

Answer: The implementing class must override the conflicting method.

**Q10. What is the purpose of the `virtual` keyword in C++ inheritance?**

Answer: It ensures that a shared virtual base class has only one instance in the most-derived object.

---

## 9. Quick Revision

| Topic | Key Point |
|---|---|
| Diamond Problem | Ambiguity in multiple inheritance |
| Main Cause | Same base class inherited through multiple paths |
| C++ Solution | Virtual Inheritance |
| Java Class Inheritance | Supports only single class inheritance |
| Java Multiple Inheritance | Supported through interfaces |
| C++ Keyword | `virtual` |

## 10. Conclusion

The Diamond Problem is a common issue in multiple inheritance. It occurs when a derived class inherits the same base class through multiple paths.

C++ solves this problem using virtual inheritance, whereas Java avoids multiple inheritance through classes and provides multiple inheritance through interfaces.

**Remember:**

- Diamond Problem → Ambiguity
- C++ → Virtual Inheritance
- Java → Multiple Interfaces

## 4. Polymorphism

**Definition:**

Polymorphism means **one name, many forms**.

It allows the same method or interface to perform different behaviors depending on the situation.

### Types of Polymorphism

**1. Compile-Time Polymorphism (Method Overloading)**

Multiple methods have the same name but different parameters.

```java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

**2. Runtime Polymorphism (Method Overriding)**

A child class provides its own implementation of a method inherited from its parent class.

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        animal.sound();
    }
}
```

**Output:**

```text
Dog barks
```
# Polymorphism, Method Overloading & Method Overriding in Java (OOP)

## 1. What is Polymorphism?

**Polymorphism** is one of the four fundamental pillars of Object-Oriented Programming (OOP).

The word Polymorphism comes from two Greek words:
- Poly = Many
- Morph = Forms

Therefore, Polymorphism means **One Name, Many Forms**.

In Java, polymorphism allows the same method or interface to behave differently depending on the situation.

### Real-Life Example

A person can have different roles:
- As a son
- As an employee
- As a father

The same person behaves differently depending on the role.

Similarly, in Java, one method can perform different operations depending on the parameters or actual object.

---

## 2. Types of Polymorphism

Java supports two main types of polymorphism:

1. Compile-Time Polymorphism (Static Polymorphism)
2. Runtime Polymorphism (Dynamic Polymorphism)

```text
                 Polymorphism
                      |
             +--------+--------+
             |                 |
       Compile-Time         Runtime
       Polymorphism       Polymorphism
             |                 |
        Overloading         Overriding
```

| Type | Mechanism | Binding |
|---|---|---|
| Compile-Time Polymorphism | Method Overloading | Static Binding |
| Runtime Polymorphism | Method Overriding | Dynamic Binding |

---

## 3. Compile-Time Polymorphism (Method Overloading)

### Definition

Method overloading occurs when multiple methods in the same class have the same name but different parameters.

Parameters can differ in:
- Number of parameters
- Type of parameters
- Order of parameters

Method overloading is an example of **Compile-Time Polymorphism** because the compiler determines which method to call based on the arguments.

### Java Example

```java
class Calculator {

    // Two parameters
    int add(int a, int b) {
        return a + b;
    }

    // Three parameters
    int add(int a, int b, int c) {
        return a + b + c;
    }

    // Different parameter types
    double add(double a, double b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {

        Calculator calculator = new Calculator();

        System.out.println(calculator.add(10, 20));
        System.out.println(calculator.add(10, 20, 30));
        System.out.println(calculator.add(10.5, 20.5));
    }
}
```

### Output

```text
30
60
31.0
```

### Rules of Method Overloading

1. Method names must be the same.
2. Parameters must be different in number, type, or order.
3. Changing only the return type is not sufficient.
4. Inheritance is not required.
5. Return types can differ if parameter lists differ.

**Important:** Java does not support method overloading based only on different return types.

---

## 4. Runtime Polymorphism (Method Overriding)

### Definition

Method overriding occurs when a child class provides its own implementation of a method already defined in its parent class.

Method overriding is an example of **Runtime Polymorphism**.

### Java Example

```java
class Animal {

    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {

        Animal animal = new Dog();

        animal.sound();
    }
}
```

### Output

```text
Dog barks
```

### How Does It Work?

```java
Animal animal = new Dog();
animal.sound();
```

- `Animal` → Reference type.
- `Dog` → Actual object type.
- Both classes have a `sound()` method.
- At runtime, Java executes the overridden method of the actual object (`Dog`).

This mechanism is called **Dynamic Method Dispatch**.

### Rules of Method Overriding

1. Inheritance is required.
2. Method name must be the same.
3. Parameter list must be the same.
4. Return type must be the same or covariant.
5. Access level cannot be more restrictive.
6. Private methods cannot be overridden.
7. Final methods cannot be overridden.
8. Static methods are hidden, not overridden.
9. The `@Override` annotation is recommended.

---

## 5. Difference Between Method Overloading and Overriding

| Feature | Method Overloading | Method Overriding |
|---|---|---|
| Polymorphism | Compile-Time | Runtime |
| Method Name | Same | Same |
| Parameters | Different | Same |
| Inheritance | Not required | Required |
| Return Type | Can differ if parameters differ | Same or covariant |
| Binding | Static Binding | Dynamic Binding |
| Purpose | Multiple ways to perform an operation | Change inherited behavior |
| Annotation | Not required | `@Override` recommended |

---

## 6. Static Binding vs Dynamic Binding

### Static Binding

Static binding means the method call is resolved at compile time.

- Commonly associated with method overloading.
- Also applies to static, private, and final methods.

### Dynamic Binding

Dynamic binding means the overridden instance method is selected at runtime based on the actual object.

- Associated with runtime polymorphism.
- Uses Dynamic Method Dispatch.

---

## 7. Real-Life Examples

### Method Overloading

A calculator provides an `add()` method:

```java
add(10, 20);
add(10, 20, 30);
add(10.5, 20.5);
```

Same method name, different parameters.

### Method Overriding

Different animals make different sounds:

| Animal | Sound |
|---|---|
| Dog | Bark |
| Cat | Meow |
| Cow | Moo |

Same method name (`sound()`), different implementations.

---

## 8. Important Job Exam Questions (MCQ / Viva)

**Q1. What is Polymorphism?**

Answer: Polymorphism means one name, many forms. It allows the same method or interface to behave differently in different situations.

**Q2. How many types of polymorphism are supported in Java?**

Answer: Two major types:
- Compile-Time Polymorphism
- Runtime Polymorphism

**Q3. Which type of polymorphism is method overloading?**

Answer: Compile-Time Polymorphism.

**Q4. Which type of polymorphism is method overriding?**

Answer: Runtime Polymorphism.

**Q5. Is inheritance required for method overloading?**

Answer: No.

**Q6. Is inheritance required for method overriding?**

Answer: Yes.

**Q7. Can we overload a method by changing only its return type?**

Answer: No.

**Q8. Which annotation is used for method overriding in Java?**

Answer: `@Override`.

**Q9. Which mechanism is responsible for runtime method overriding?**

Answer: Dynamic Method Dispatch.

**Q10. Can static methods be overridden in Java?**

Answer: No. They can be hidden, not overridden.

**Q11. Can private methods be overridden?**

Answer: No. Private methods are not inherited.

**Q12. Can final methods be overridden?**

Answer: No.

**Q13. What is Dynamic Method Dispatch?**

Answer: It is the mechanism by which an overridden method call is resolved at runtime based on the actual object type.

---

## 9. Quick Revision

| Concept | Remember |
|---|---|
| Polymorphism | One Name, Many Forms |
| Compile-Time Polymorphism | Method Overloading |
| Runtime Polymorphism | Method Overriding |
| Overloading | Same name, different parameters |
| Overriding | Same signature, different implementation |
| Overloading | Inheritance not required |
| Overriding | Inheritance required |
| Overloading | Static Binding |
| Overriding | Dynamic Binding |

---

## 10. Conclusion

Polymorphism is one of the four fundamental pillars of OOP. It makes Java applications more flexible, reusable, and extensible.

- **Polymorphism:** One name, many forms.
- **Method Overloading:** Same method name with different parameters.
- **Method Overriding:** Child class provides a different implementation of an inherited method.

### Memory Trick

```text
OOP
 |
 +-- Polymorphism
       |
       +-- Compile-Time → Overloading
       |
       +-- Runtime      → Overriding
```

**Polymorphism = Compile-Time Polymorphism + Runtime Polymorphism**

**Benefits:**
- Flexibility
- Code reusability
- Loose coupling
- Dynamic method dispatch

---

## 5. Encapsulation

**Definition:**

Encapsulation is the process of wrapping data (variables) and methods into a single unit (class) and restricting direct access to the data.

It is commonly implemented using private variables and public getter/setter methods.

**Java Example:**

```java
class Student {

    private String name;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

public class Main {
    public static void main(String[] args) {
        Student student = new Student();

        student.setName("Abdullah");

        System.out.println(student.getName());
    }
}
```

**Output:**

```text
Abdullah
```

**Benefits:**
- Data hiding
- Data protection
- Controlled access to data
- Improved maintainability

---

## 6. Abstraction

**Definition:**

Abstraction is the process of hiding implementation details and showing only essential functionality to the user.

In Java, abstraction is achieved through:
- Abstract Classes
- Interfaces

**Java Example:**

```java
abstract class Vehicle {

    abstract void start();

}

class Car extends Vehicle {

    @Override
    void start() {
        System.out.println("Car starts with a key");
    }
}

public class Main {
    public static void main(String[] args) {
        Vehicle vehicle = new Car();

        vehicle.start();
    }
}
```

**Output:**

```text
Car starts with a key
```

**Benefits:**
- Hides implementation complexity
- Improves code maintainability
- Provides security through controlled exposure
- Reduces implementation dependency

---

## 7. Comparison of Four Pillars of OOP

| Pillar | Main Concept | Java Mechanism |
|---|---|---|
| Inheritance | Code reusability | `extends` |
| Polymorphism | One name, many forms | Overloading, Overriding |
| Encapsulation | Data hiding | `private`, Getters/Setters |
| Abstraction | Implementation hiding | `abstract`, `interface` |

---

## 8. Real-Life Examples

| Pillar | Real-Life Example |
|---|---|
| Inheritance | A Dog inherits common characteristics from an Animal |
| Polymorphism | Different animals make different sounds |
| Encapsulation | A bank account controls access to its balance |
| Abstraction | Driving a car without knowing its internal engine mechanism |

---

## 9. Important Job Exam Questions (MCQ / Viva)

**Q1. How many fundamental pillars does OOP have?**

Answer: Four.

**Q2. Which OOP concept supports code reusability?**

Answer: Inheritance.

**Q3. What does polymorphism mean?**

Answer: One name, many forms.

**Q4. Which OOP concept provides data hiding?**

Answer: Encapsulation.

**Q5. Which concept hides implementation details?**

Answer: Abstraction.

**Q6. Which Java keyword is used for class inheritance?**

Answer: `extends`.

**Q7. Which keyword is used to implement an interface in Java?**

Answer: `implements`.

**Q8. Can Java support multiple inheritance through classes?**

Answer: No. Java supports multiple inheritance through interfaces.

**Q9. What are the two types of polymorphism?**

Answer:
- Compile-Time Polymorphism
- Runtime Polymorphism

**Q10. Which mechanism is used for runtime polymorphism in Java?**

Answer: Method Overriding.

**Q11. Can we create an object of an abstract class?**

Answer: No.

**Q12. Which access modifier is commonly used for data hiding?**

Answer: `private`.

---

## 10. Quick Revision

Remember these four concepts:

- **Inheritance** → Reusability
- **Polymorphism** → Many Forms
- **Encapsulation** → Data Hiding
- **Abstraction** → Implementation Hiding

## Conclusion

The four pillars of OOP provide the foundation for designing software using object-oriented principles. They make applications more reusable, maintainable, flexible, and easier to extend.

**OOP = Inheritance + Polymorphism + Encapsulation + Abstraction**

<img width="1206" height="505" alt="image" src="https://github.com/user-attachments/assets/bad200a7-c2c2-4a33-8cd3-2ebea44113e4" />
<img width="1221" height="668" alt="image" src="https://github.com/user-attachments/assets/33d0a668-0f3a-4909-b691-7d95c28d2af6" />

# Difference Between Class and Structure (C++)

## 1. Class

A **Class** is a user-defined data type that combines data members (variables) and member functions (methods) into a single unit.

```cpp
class Student {
    int id;  // Private by default
public:
    void display() {
        cout << id;
    }
};
```

## 2. Structure (Struct)

A **Structure** is a user-defined data type that groups different types of variables and functions into a single unit.

```cpp
struct Student {
    int id;  // Public by default
    string name;
};
```

## 3. Difference Between Class and Structure

| Feature | Class | Structure |
|---|---|---|
| Keyword | `class` | `struct` |
| Default Access Modifier | Private | Public |
| Default Inheritance | Private | Public |
| Data Members | Supported | Supported |
| Member Functions | Supported | Supported |
| Constructors | Supported | Supported |
| Inheritance | Supported | Supported |
| Polymorphism | Supported | Supported |

## 4. Important Job Exam Questions

**Q1. What is the default access modifier of a class in C++?**

Answer: Private.

**Q2. What is the default access modifier of a structure in C++?**

Answer: Public.

**Q3. Can a structure contain member functions in C++?**
## Class-এর ভিতরে যে function তৈরি করা হয়, তাকে Member Function বলে। এগুলো class-এর data members (variables) ব্যবহার এবং পরিবর্তন করতে পারে।
Answer: Yes.

**Q4. Can a structure support inheritance in C++?**

Answer: Yes.

**Q5. Does Java support C++-style structures?**

Answer: No.

## 5. Quick Revision

- Class → Private by default.
- Struct → Public by default.
- Class → Private inheritance by default.
- Struct → Public inheritance by default.

**Important:** In C++, both Class and Struct support Encapsulation, Inheritance, Polymorphism, Constructors, and Member Functions.

**Main Difference:** Default access modifier and default inheritance access.
