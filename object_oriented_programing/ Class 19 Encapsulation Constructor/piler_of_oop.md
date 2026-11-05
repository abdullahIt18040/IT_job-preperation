
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

# Encapsulation in Java (OOP)

## 1. What is Encapsulation?

Encapsulation is one of the four main pillars of Object-Oriented Programming (OOP).

**Definition:** Encapsulation is the process of wrapping data (variables) and methods into a single unit (class) and restricting direct access to the data.

**In Simple Words:** Encapsulation means binding data and methods together and protecting data from direct external access.

## 2. How to Achieve Encapsulation?

We can achieve encapsulation in Java by:

1. Declaring class variables as `private`.
2. Providing `public` getter and setter methods to access and modify private variables.

## 3. Java Example

```java
class Student {

    // Private variables (Data Hiding)
    private String name;
    private int age;

    // Getter method
    public String getName() {
        return name;
    }

    // Setter method
    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        }
    }
}

public class Main {
    public static void main(String[] args) {

        Student student = new Student();

        student.setName("Abdullah");
        student.setAge(25);

        System.out.println(student.getName());
        System.out.println(student.getAge());
    }
}
```

## 4. Why Do We Use Encapsulation?

1. **Data Hiding:** Prevents direct access to private variables.
2. **Data Security:** Protects data from unauthorized modification.
3. **Validation:** Allows validation before updating data.
4. **Maintainability:** Makes code easier to maintain.
5. **Flexibility:** Allows internal implementation to change without affecting external code.

## 5. Real-Life Example

**ATM Machine:**

- Users cannot directly access the bank database.
- Users interact with the ATM through buttons and a screen.
- The ATM validates the PIN before allowing transactions.
- Users can withdraw money only when the required conditions are satisfied.

This is similar to encapsulation.

## 6. Encapsulation vs Data Hiding

| Encapsulation | Data Hiding |
|---|---|
| Wrapping data and methods into a single unit. | Restricting direct access to data. |
| Achieved through classes. | Achieved using access modifiers like `private`. |
| Provides a way to organize and control data. | Protects internal data from direct access. |

**Note:** Data hiding is an important part of encapsulation, but they are not the same.

<img width="1370" height="499" alt="image" src="https://github.com/user-attachments/assets/64b15fc9-ffb0-4bdf-b805-2f431d778705" />
# Bank Account Program Using Encapsulation in Java

**Problem:** Write a Java program to represent a Bank Account using the concept of Encapsulation.

## 1. Requirements

Create a `BankAccount` class with the following:

1. Data members:
   - Account holder's name
   - Account number
   - Account balance

2. Member functions:
   - `deposit()` – Deposit money into the account.
   - `withdraw()` – Withdraw money if sufficient balance is available.
   - `display()` – Display account details.

3. Demonstrate encapsulation by keeping all data members private and providing public methods for controlled access.

## 2. Java Implementation

```java
class BankAccount {

    // Private data members (Data Hiding)
    private String accountHolderName;
    private String accountNumber;
    private double balance;

    // Constructor
    public BankAccount(String name, String accNumber, double initialBalance) {
        this.accountHolderName = name;
        this.accountNumber = accNumber;
        this.balance = initialBalance;
    }

    // Deposit money
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposit successful!");
        } else {
            System.out.println("Invalid deposit amount!");
        }
    }

    // Withdraw money
    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawal successful!");
        } else {
            System.out.println("Insufficient balance or invalid amount!");
        }
    }

    // Display account details
    public void display() {
        System.out.println("Account Holder: " + accountHolderName);
        System.out.println("Account Number: " + accountNumber);
        System.out.println("Balance: " + balance);
    }
}

// Main class
public class Main {
    public static void main(String[] args) {

        BankAccount account = new BankAccount(
            "Abdullah",
            "123456789",
            5000
        );

        // Display initial details
        account.display();

        // Deposit money
        account.deposit(2000);

        // Withdraw money
        account.withdraw(1500);

        // Display updated details
        System.out.println("\nAfter Transactions:");
        account.display();
    }
}
```

## 3. Output

```text
Account Holder: Abdullah
Account Number: 123456789
Balance: 5000.0

Deposit successful!
Withdrawal successful!

After Transactions:
Account Holder: Abdullah
Account Number: 123456789
Balance: 5500.0
```

## 4. Code Explanation

### A. Private Data Members

```java
private String accountHolderName;
private String accountNumber;
private double balance;
```

- All variables are declared as `private`.
- They cannot be accessed directly from outside the `BankAccount` class.
- This concept is called **Data Hiding**.

### B. Constructor

```java
public BankAccount(String name, String accNumber, double initialBalance) {
    this.accountHolderName = name;
    this.accountNumber = accNumber;
    this.balance = initialBalance;
}
```

The constructor initializes account information when an object is created.

### C. deposit() Method

```java
public void deposit(double amount) {
    if (amount > 0) {
        balance += amount;
    }
}
```

Adds the deposit amount to the current account balance.

### D. withdraw() Method

```java
public void withdraw(double amount) {
    if (amount > 0 && amount <= balance) {
        balance -= amount;
    }
}
```

Withdraws money only if the amount is valid and sufficient balance is available.

### E. display() Method

Displays the account holder's name, account number, and current balance.

## 5. How Does This Program Demonstrate Encapsulation?

| Concept | Implementation |
|---|---|
| Data Hiding | Private variables |
| Data Binding | Variables and methods inside one class |
| Controlled Access | Public methods |
| Data Validation | Deposit and withdraw conditions |
| Data Protection | Prevents direct external modification |


# Abstraction in Java (OOP)

## 1. What is Abstraction?

Abstraction is one of the four main pillars of Object-Oriented Programming (OOP).

**Definition:** Abstraction is the process of hiding implementation details and showing only essential features to the user.

**In Simple Words:** Abstraction means showing WHAT to do instead of HOW to do it.

**বাংলায়:** Abstraction হলো কোনো কিছুর ভিতরে কীভাবে কাজ হচ্ছে (Implementation Details), তা লুকিয়ে রেখে ব্যবহারকারীকে শুধু প্রয়োজনীয় Functionality দেখানো।

**Main Purpose:** Hiding implementation complexity.

## 2. Real-Life Example

**ATM Machine:**

- We enter our PIN to withdraw money.
- We do not know how the ATM communicates with the bank database.
- We only use the necessary functionalities.

This is an example of abstraction.

**Car:**

- We press the accelerator to increase speed.
- We do not need to know the internal engine implementation.

## 3. How to Achieve Abstraction in Java?

Java supports abstraction mainly through:

1. Abstract Class
2. Interface

---

## 4. Abstraction Using Abstract Class

An abstract class is declared using the `abstract` keyword.

It can contain:
- Abstract methods (without method body).
- Concrete methods (with method body).
- Variables and constructors.

### Java Example

```java
// Abstract class
abstract class Animal {

    // Abstract method
    abstract void sound();

    // Concrete method
    void eat() {
        System.out.println("Animal is eating");
    }
}

// Child class
class Dog extends Animal {

    // Implementing abstract method
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

// Main class
public class Main {

    public static void main(String[] args) {

        Dog dog = new Dog();

        dog.sound();
        dog.eat();
    }
}
```

### Output

```text
Dog barks
Animal is eating
```

### Explanation in Bangla

**Step 1: Abstract Class**

```java
abstract class Animal {
    abstract void sound();
}
```

- `abstract` keyword দিয়ে abstract class তৈরি করা হয়।
- Abstract method-এর কোনো body থাকে না।
- Abstract class-এর সরাসরি object তৈরি করা যায় না।

**Step 2: Child Class**

```java
class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}
```

- Dog class, Animal class inherit করেছে।
- Dog class `sound()` method-এর implementation দিয়েছে।

**Remember:** Parent class শুধু বলে দেয় কী কাজ করতে হবে, আর Child class নির্ধারণ করে কীভাবে কাজটি করতে হবে।

---

## 5. Abstraction Using Interface

An interface is another way to achieve abstraction in Java.

**Definition:** An interface is a blueprint of a class that defines a contract that implementing classes must follow.

**সহজ বাংলায়:** Interface হলো একটি Blueprint বা Contract। এখানে কী কী method থাকতে হবে তা define করা হয়। যে class interface implement করবে, তাকে abstract method-গুলোর implementation দিতে হবে।

### Java Example

```java
// Interface
interface Vehicle {

    // Abstract method
    void start();

    void stop();
}

// Implementing class
class Car implements Vehicle {

    @Override
    public void start() {
        System.out.println("Car is starting");
    }

    @Override
    public void stop() {
        System.out.println("Car is stopping");
    }
}

// Main class
public class Main {

    public static void main(String[] args) {

        Car car = new Car();

        car.start();
        car.stop();
    }
}
```

### Output

```text
Car is starting
Car is stopping
```

### Explanation in Bangla

**Step 1: Create Interface**

```java
interface Vehicle {
    void start();
    void stop();
}
```

- `interface` keyword দিয়ে interface তৈরি করা হয়।
- এখানে `start()` এবং `stop()` method declare করা হয়েছে।
- Interface-এর সাধারণ abstract method-এর body থাকে না।

**Step 2: Implement Interface**

```java
class Car implements Vehicle {
    
    @Override
    public void start() {
        System.out.println("Car is starting");
    }

    @Override
    public void stop() {
        System.out.println("Car is stopping");
    }
}
```

- `implements` keyword দিয়ে interface implement করা হয়।
- Car class-কে interface-এর abstract methods implement করতে হয়েছে।
- Interface-এর abstract methods implicitly `public abstract` হয়। তাই implementation method অবশ্যই `public` হতে হবে।

**Remember:**
- `extends` is used for class inheritance.
- `implements` is used for interface implementation.

---

## 6. Important Features of Interface

1. Interface is declared using the `interface` keyword.
2. A class implements an interface using `implements`.
3. A class can implement multiple interfaces.
4. Interface cannot be instantiated directly.
5. Interface fields are implicitly `public static final`.
6. Abstract methods are implicitly `public abstract`.
7. Interfaces can also contain `default`, `static`, and `private` methods (with method bodies).
8. An interface does not have a constructor.

### Multiple Interface Example

```java
interface Printable {
    void print();
}

interface Showable {
    void show();
}

class Document implements Printable, Showable {

    @Override
    public void print() {
        System.out.println("Printing document");
    }

    @Override
    public void show() {
        System.out.println("Showing document");
    }
}
```

A single class can implement multiple interfaces.

---

## 7. Abstract Class vs Interface

| Abstract Class | Interface |
|---|---|
| Declared using `abstract class`. | Declared using `interface`. |
| Can have abstract and concrete methods. | Can have abstract, default, static and private methods. |
| Can have instance variables. | Fields are implicitly `public static final`. |
| Can have constructors. | Cannot have constructors. |
| A class can extend only one class. | A class can implement multiple interfaces. |
| Uses `extends`. | Uses `implements`. |

---

## 8. Encapsulation vs Abstraction

| Encapsulation | Abstraction |
|---|---|
| Hides data and controls access. | Hides implementation details. |
| Focuses on data protection. | Focuses on reducing complexity. |
| Uses private variables and public methods. | Uses abstract classes and interfaces. |
| Example: Bank Account. | Example: ATM Machine. |

---

## 9. Important Interview & Exam Questions

**Q1. What is abstraction?**

Answer: Abstraction is the process of hiding implementation details and showing only essential functionality.

**Q2. How can we achieve abstraction in Java?**

Answer: Using abstract classes and interfaces.

**Q3. Can we create an object of an abstract class?**

Answer: No.

**Q4. Can an abstract class have a constructor?**

Answer: Yes.

**Q5. Can an abstract class contain concrete methods?**

Answer: Yes.

**Q6. Can we create an object of an interface?**

Answer: No.

**Q7. Can a class implement multiple interfaces?**

Answer: Yes.

**Q8. What is the difference between extends and implements?**

Answer:
- `extends` is used for class inheritance and interface inheritance.
- `implements` is used when a class implements an interface.

**Q9. Can an interface contain a constructor?**

Answer: No.

**Q10. Can an interface have a method with a body?**

Answer: Yes. Interfaces can have default, static, and private methods with implementations.

**Q11. What happens if a class does not implement all abstract methods of an interface?**

Answer: The class must be declared abstract; otherwise, a compilation error occurs.

**Q12. Can an interface extend another interface?**

Answer: Yes. An interface can extend one or multiple interfaces.

---

## 10. Key Points to Remember

- Abstraction hides implementation details.
- Abstraction shows WHAT to do, not HOW to do it.
- Java achieves abstraction through abstract classes and interfaces.
- Abstract classes can contain abstract and concrete methods.
- Interfaces support multiple inheritance of type.
- `extends` is used for inheritance.
- `implements` is used for interface implementation.
- Abstract classes and interfaces cannot be instantiated directly.

### One-Line Definitions

**Abstraction:** Hiding implementation details and exposing essential functionality.

**Abstract Class:** A class declared with the `abstract` keyword that can contain abstract and concrete methods.

**Interface:** A contract that defines methods and behaviors that implementing classes agree to provide.

**Final Exam Tip:** Remember these three concepts:

1. Encapsulation = Data Hiding.
2. Abstraction = Implementation Hiding.
3. Inheritance = Code Reusability.
   # Why Do We Use Abstraction in Java?

Abstraction is used to hide unnecessary implementation details and expose only essential functionality to the user.

### Main Reasons for Using Abstraction

1. **Reduce Complexity:** Users don't need to understand internal implementation details.
2. **Code Security:** Hides internal implementation from external users.
3. **Code Reusability:** Common functionality can be defined in an abstract class or interface and reused by child classes.
4. **Maintainability:** Internal implementation can be changed without affecting external users.
5. **Flexibility:** Different classes can provide different implementations of the same method.
6. **Loose Coupling:** Code can depend on interfaces rather than specific implementations.

## Practical Example: Payment System

Suppose we are developing an online shopping application.

Customers can pay using:
- Credit Card
- Bkash
- PayPal

All payment methods perform the same task: `pay()`.

However, their internal payment processes are different.

We can use an interface to achieve abstraction.

### Java Code

```java
// Interface
interface Payment {

    void pay(double amount);
}

// Credit Card Payment
class CreditCard implements Payment {

    @Override
    public void pay(double amount) {
        System.out.println(
            "Paid " + amount + " TK using Credit Card"
        );
    }
}

// Bkash Payment
class Bkash implements Payment {

    @Override
    public void pay(double amount) {
        System.out.println(
            "Paid " + amount + " TK using Bkash"
        );
    }
}

// Main class
public class Main {

    public static void main(String[] args) {

        Payment payment;

        // Credit Card Payment
        payment = new CreditCard();
        payment.pay(1000);

        // Bkash Payment
        payment = new Bkash();
        payment.pay(2000);
    }
}
```

### Output

```text
Paid 1000.0 TK using Credit Card
Paid 2000.0 TK using Bkash
```

### Explanation in Bangla

**Step 1: Create an Interface**

```java
interface Payment {
    void pay(double amount);
}
```

এখানে `Payment` interface শুধু বলে দিয়েছে payment করার জন্য `pay()` method থাকতে হবে।

কিন্তু কীভাবে payment হবে, সেটা বলে দেয়নি।

**Step 2: Different Implementations**

```java
class CreditCard implements Payment {
    public void pay(double amount) {
        // Credit card payment logic
    }
}
```

```java
class Bkash implements Payment {
    public void pay(double amount) {
        // Bkash payment logic
    }
}
```

এখানে দুইটি class একই `pay()` method implement করেছে, কিন্তু তাদের implementation আলাদা।

**Step 3: Using Payment Interface**

```java
Payment payment;

payment = new CreditCard();
payment.pay(1000);

payment = new Bkash();
payment.pay(2000);
```

এখানে main method জানে শুধু `pay()` method call করতে হবে।

কিন্তু Credit Card বা Bkash-এর ভিতরে কীভাবে payment process হচ্ছে, সেটা জানার প্রয়োজন নেই।

এটাই Abstraction-এর মূল ধারণা।

## Benefits of Abstraction in This Example

| Benefit | Explanation |
|---|---|
| Reduce Complexity | Main method does not need payment implementation details. |
| Flexibility | We can add new payment methods easily. |
| Maintainability | Payment logic can change independently. |
| Loose Coupling | Main code depends on the Payment interface. |
| Reusability | Different payment classes follow the same contract. |

### Without Abstraction vs With Abstraction

**Without Abstraction:**

Main application needs to know the internal implementation of every payment method.

**With Abstraction:**

Main application only calls `pay()`. Each payment class handles its own implementation.

---

## Final Exam Notes

**Why do we use Abstraction?**

We use abstraction to:
1. Hide implementation details.
2. Reduce code complexity.
3. Improve maintainability.
4. Provide flexibility.
5. Achieve loose coupling.

**One-Line Interview Answer:**

We use abstraction to hide implementation complexity and expose only essential functionality, making software easier to use, maintain, and extend.

**Remember:**

- Abstraction = What to do, not how to do it.
- Encapsulation = Protecting data through controlled access.
- Inheritance = Reusing existing class properties and methods.
- Polymorphism = One interface, many forms.

  <img width="481" height="121" alt="image" src="https://github.com/user-attachments/assets/a936f563-6b26-44f9-a7a9-3cad752230d5" />

# How Abstraction Supports Code Reusability in Java

## 1. How Does Abstraction Help in Code Reusability?

Abstraction supports code reusability by defining common methods and contracts in abstract classes or interfaces that multiple classes can reuse.

**In Simple Words:** Abstraction allows multiple classes to follow the same common structure without defining the contract again and again.

**বাংলায়:**

ধরো, আমাদের তিন ধরনের Payment System আছে:

- Bkash
- Nagad
- Rocket

সব Payment System-এ `pay()` method প্রয়োজন।

আমরা প্রতিটি class-এর জন্য আলাদা design না করে একটি common Interface তৈরি করতে পারি।

তারপর সব Payment class সেই Interface implement করতে পারবে।

এভাবে common structure বা contract reuse করা যায়।

## 2. Java Example Using Abstraction

### Step 1: Create an Interface

```java
// Common interface
interface Payment {
    void pay(double amount);
}
```

Here, we define a common contract using the `Payment` interface.

All payment classes must provide their own implementation of the `pay()` method.

### Step 2: Implement the Interface

```java
// Bkash implementation
class Bkash implements Payment {

    @Override
    public void pay(double amount) {
        System.out.println("Bkash payment: " + amount);
    }
}

// Nagad implementation
class Nagad implements Payment {

    @Override
    public void pay(double amount) {
        System.out.println("Nagad payment: " + amount);
    }
}

// Rocket implementation
class Rocket implements Payment {

    @Override
    public void pay(double amount) {
        System.out.println("Rocket payment: " + amount);
    }
}
```

Here, three different classes implement the same `Payment` interface.

Each class provides its own implementation of the `pay()` method.

### Step 3: Reuse the Common Interface

```java
public class Main {

    // Reusable method
    public static void processPayment(Payment payment) {
        payment.pay(1000);
    }

    public static void main(String[] args) {

        processPayment(new Bkash());

        processPayment(new Nagad());

        processPayment(new Rocket());
    }
}
```

### Output

```text
Bkash payment: 1000.0
Nagad payment: 1000.0
Rocket payment: 1000.0
```

## 3. How Does Code Reusability Happen Here?

1. We create the `Payment` interface once.
2. Multiple classes implement the same interface.
3. Every class follows the same contract.
4. We write `processPayment()` only once.
5. The same method works with Bkash, Nagad, and Rocket.

**Important:** Interface reuses a common contract, not necessarily the actual method implementation. Each implementing class provides its own implementation.

## 4. Diagram

```text
              Payment (Interface)
                      |
             -------------------
             |        |        |
           Bkash    Nagad    Rocket
             |        |        |
           pay()    pay()    pay()
```

All classes follow the same Payment contract but have different implementations.

## 5. Abstraction vs Inheritance in Code Reusability

| Abstraction | Inheritance |
|---|---|
| Reuses common contracts and design. | Reuses existing properties and method implementations. |
| Uses interfaces and abstract classes. | Uses `extends`. |
| Focuses on what a class should do. | Focuses on reusing existing code. |
| Supports flexible implementations. | Reduces code duplication. |

## 6. Benefits of Abstraction for Code Reusability

1. **Code Reusability:** Multiple classes can follow the same common contract.
2. **Flexibility:** New payment methods can be added easily.
3. **Maintainability:** Changes in implementation do not require changes to the common contract.
4. **Loose Coupling:** Classes depend on an abstraction rather than a specific implementation.
5. **Extensibility:** New classes can implement the existing interface.



## QUestion 
<img width="1081" height="336" alt="image" src="https://github.com/user-attachments/assets/be74a7f4-bdb9-47df-baeb-c07b0eda613a" />


# Abstract Method in Java

## 1. What is an Abstract Method?

An **abstract method** is a method that is declared without a body (implementation).

- It only declares what a method should do.
- The child class provides the actual implementation.
- It is declared using the `abstract` keyword.

### Syntax

```java
abstract returnType methodName();
```

Example:

```java
abstract void calculateBill();
```

## 2. Abstract Method with Inheritance

Suppose we have a `Customer` parent class and two child classes: `Residential` and `Commercial`.

Both customers need to calculate electricity bills, but their calculation rules are different.

- Residential: 6 TK per unit.
- Commercial: 10 TK per unit.

Instead of implementing the calculation in the parent class, we can declare `calculateBill()` as an abstract method.

### Complete Java Program

```java
// Abstract Parent Class
abstract class Customer {

    int customerId;
    int customerUtility;

    Customer(int customerId, int customerUtility) {
        this.customerId = customerId;
        this.customerUtility = customerUtility;
    }

    // Abstract Method
    abstract void calculateBill();
}

// Residential Child Class
class Residential extends Customer {

    Residential(int id, int units) {
        super(id, units);
    }

    @Override
    void calculateBill() {
        int bill = customerUtility * 6;

        System.out.println("Residential Bill: " + bill + " TK");
    }
}

// Commercial Child Class
class Commercial extends Customer {

    Commercial(int id, int units) {
        super(id, units);
    }

    @Override
    void calculateBill() {
        int bill = customerUtility * 10;

        System.out.println("Commercial Bill: " + bill + " TK");
    }
}

// Main Class
public class Main {

    public static void main(String[] args) {

        Customer c1 = new Residential(101, 100);
        Customer c2 = new Commercial(102, 100);

        c1.calculateBill();
        c2.calculateBill();
    }
}
```

### Output

```text
Residential Bill: 600 TK
Commercial Bill: 1000 TK
```

## 3. How Does It Work?

1. `Customer` is an abstract parent class.
2. `calculateBill()` is declared as an abstract method without a body.
3. `Residential` inherits the `Customer` class and implements `calculateBill()` at 6 TK per unit.
4. `Commercial` inherits the `Customer` class and implements `calculateBill()` at 10 TK per unit.
5. In the `main()` method, both child objects call the same method but produce different results.

<img width="888" height="424" alt="image" src="https://github.com/user-attachments/assets/b55eeef5-6c5e-4281-8c2b-407b9877ecd3" />
<img width="1366" height="770" alt="image" src="https://github.com/user-attachments/assets/4ee0b3f0-43f4-4ea5-8f1a-a8c47b516b84" />

# Interface in Java

## 1. What is an Interface?

An **interface** in Java is a blueprint or contract for a class that defines what functionality a class must provide.

- Declared using the `interface` keyword.
- A class implements an interface using the `implements` keyword.
- Supports abstraction.
- Supports multiple inheritance of type.
- Helps achieve loose coupling.

**Easy Bangla Explanation:**

Interface হলো একটি contract বা চুক্তি। এটি বলে দেয় একটি class-এ কোন কোন method থাকতে হবে, কিন্তু abstract method-এর ক্ষেত্রে কীভাবে কাজ করবে তা বলে দেয় না।

## 2. Syntax of Interface

```java
interface InterfaceName {
    void methodName();
}
```

Implementing an interface:

```java
class MyClass implements InterfaceName {

    @Override
    public void methodName() {
        // Implementation
    }
}
```

## 3. Example of Interface

Suppose we have a `Vehicle` interface. Both Car and Bike implement this interface.

```java
// Interface
interface Vehicle {

    void start();
    void stop();
}

// Car Class
class Car implements Vehicle {

    @Override
    public void start() {
        System.out.println("Car is starting");
    }

    @Override
    public void stop() {
        System.out.println("Car is stopping");
    }
}

// Bike Class
class Bike implements Vehicle {

    @Override
    public void start() {
        System.out.println("Bike is starting");
    }

    @Override
    public void stop() {
        System.out.println("Bike is stopping");
    }
}

// Main Class
public class Main {

    public static void main(String[] args) {

        Vehicle v1 = new Car();
        Vehicle v2 = new Bike();

        v1.start();
        v1.stop();

        v2.start();
        v2.stop();
    }
}
```

### Output

```text
Car is starting
Car is stopping
Bike is starting
Bike is stopping
```

## 4. Why Do We Use Interface?

### 1. Abstraction

Hide implementation details and expose only necessary functionality.

Example: A Vehicle interface declares `start()`, but Car and Bike implement it differently.

### 2. Loose Coupling

Loose coupling means reducing dependency between classes.

Instead of depending on a specific implementation, we depend on an interface.

```java
Vehicle vehicle = new Car();
```

We can easily change the implementation:

```java
Vehicle vehicle = new Bike();
```

The code that uses the Vehicle interface does not need to depend directly on Car or Bike.

### 3. Code Reusability

Different classes can implement the same interface and follow a common contract.

Example: Car, Bike and Bus can all implement Vehicle.

### 4. Multiple Inheritance

Java does not support multiple inheritance using classes.

But a class can implement multiple interfaces.

**Syntax:**

```java
class ChildClass implements Interface1, Interface2 {
    // Implementation
}
```

### Example: Multiple Inheritance Using Interface

```java
interface Camera {
    void takePhoto();
}

interface MusicPlayer {
    void playMusic();
}

class Smartphone implements Camera, MusicPlayer {

    @Override
    public void takePhoto() {
        System.out.println("Taking Photo");
    }

    @Override
    public void playMusic() {
        System.out.println("Playing Music");
    }
}
```

Here, Smartphone implements two interfaces: Camera and MusicPlayer.

## 5. Same Method in Multiple Interfaces

What happens if two interfaces contain the same abstract method?

**Answer:** No problem! The implementing class only needs one implementation.

```java
interface A {
    void show();
}

interface B {
    void show();
}

class C implements A, B {

    @Override
    public void show() {
        System.out.println("Hello from Class C");
    }
}
```

One `show()` method satisfies both interfaces.

### What if Both Interfaces Have the Same Default Method?

Java creates a conflict because both interfaces provide their own implementation.

The implementing class must override the method.

```java
interface A {
    default void show() {
        System.out.println("Interface A");
    }
}

interface B {
    default void show() {
        System.out.println("Interface B");
    }
}

class C implements A, B {

    @Override
    public void show() {
        A.super.show();
        B.super.show();

        System.out.println("Class C");
    }
}
```

**Output:**

```text
Interface A
Interface B
Class C
```

- `A.super.show()` calls the default method of interface A.
- `B.super.show()` calls the default method of interface B.

**Important:**

| Situation | Result |
|---|---|
| Same abstract method in two interfaces | One implementation is enough |
| Same default method in two interfaces | Must override and resolve conflict |
| Same static method in two interfaces | No overriding conflict; call using interface name |

## 6. Important Rules of Interface in Java

1. An interface is declared using the `interface` keyword.
2. A class implements an interface using `implements`.
3. Interface variables are implicitly `public static final`.
4. Abstract methods are implicitly `public abstract`.
5. Implemented abstract methods must be declared `public`.
6. We cannot create an object of an interface.
7. An interface can extend multiple interfaces.
8. A class can implement multiple interfaces.
9. An interface can contain `default` and `static` methods (Java 8).
10. An interface can contain private methods (Java 9).
11. An interface cannot have a constructor.

## 7. Interface vs Abstract Class

| Interface | Abstract Class |
|---|---|
| Uses `interface` keyword | Uses `abstract class` |
| A class uses `implements` | A class uses `extends` |
| Supports multiple interface implementation | A class can extend only one class |
| No constructors | Can have constructors |
| Variables are implicitly public static final | Can have instance variables |
| Supports abstract and default methods | Supports abstract and normal methods |
| Cannot have instance fields | Can have instance fields |

## 8. When Should We Use Interface vs Abstract Class?

**Use Interface when:**

- Different or unrelated classes need to follow the same contract.
- Multiple inheritance of type is required.
- You want loose coupling.
- You want to define common behavior without forcing a shared parent class.

**Use Abstract Class when:**

- Related classes share common properties and state.
- You need constructors.
- You want to provide common code to child classes.
- You need both abstract and normal methods.

## 9. Important Interview & Exam Questions

**Q1. Can a class implement multiple interfaces?**

Yes.

**Q2. Can an interface extend another interface?**

Yes. An interface can extend multiple interfaces.

**Q3. Can we create an object of an interface?**

No. But we can create an interface reference.

```java
Vehicle v = new Car();
```

**Q4. Are interface variables final?**

Yes. They are implicitly `public static final`.

**Q5. Can an interface have a constructor?**

No.

**Q6. Does Java support multiple inheritance?**

Yes, through interfaces (multiple inheritance of type).

**Q7. What happens if two interfaces have the same abstract method?**

One implementation in the implementing class is enough.

**Q8. What happens if two interfaces have the same default method?**

The implementing class must override the method to resolve the conflict.

**Q9. Can an interface contain a normal method?**

Yes. It can contain default, static and private methods with implementations.

## 10. Important Keywords

| Keyword | Meaning |
|---|---|
| `interface` | Declares an interface |
| `implements` | Implements an interface |
| `extends` | Inherits an interface |
| `default` | Defines a default method |
| `static` | Defines a static method |
| `private` | Defines a private helper method |
| `@Override` | Indicates method overriding |

## 11. Remember for Exams

- **Interface = Contract**
- **implements = Implement an interface**
- **extends = Inherit an interface**
- **Abstraction = Hiding implementation details**
- **Loose Coupling = Depend on abstraction, not concrete implementation**
- **Multiple Inheritance = Implement multiple interfaces**
- **Same Abstract Method = One implementation is enough**
- **Same Default Method = Must override to resolve conflict**

### Easy Bangla Explanation

ধরো, একটি `Vehicle` interface বলছে প্রত্যেক Vehicle-এর `start()` এবং `stop()` method থাকতে হবে।

Car, Bike এবং Bus প্রত্যেকে নিজের মতো করে method দুটি implement করবে।

আবার একটি class একসাথে একাধিক interface implement করতে পারে।

অর্থাৎ, Interface শুধু নিয়ম বা contract তৈরি করে দেয়, আর implementing class সেই নিয়ম অনুযায়ী কাজ করে।
