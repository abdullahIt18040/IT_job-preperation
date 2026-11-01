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

