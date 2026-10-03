# Error Detection in Computer Networks

## What is an Error?

An **error** occurs when the data received by the receiver is different from the data sent by the sender.

During transmission, **noise** can change the binary bits:

```text
0 → 1
1 → 0
```

As a result, the transmitted data may become **corrupted**.

To detect these errors, **error-detection codes** are added to the original data.

> **Error Detection:** The process of detecting whether an error occurred during data transmission.

---

## Types of Errors

There are mainly **three types of transmission errors**:

1. Single-Bit Error
2. Multiple-Bit Error
3. Burst Error

---

## 1. Single-Bit Error

A **single-bit error** occurs when **only one bit** of the transmitted data is changed.

### Example

```text
Sent:     10110110
Received: 10100110
                 ↑
             One bit changed
```

Only **one bit** is affected.

### Simple Definition

> **Single-Bit Error:** An error in which only one bit is changed during transmission.

---

## 2. Multiple-Bit Error

A **multiple-bit error** occurs when **more than one bit** is changed during transmission.

The affected bits do not necessarily have to be consecutive.

### Example

```text
Sent:     10110110
Received: 11100111
           ↑  ↑  ↑
        Multiple bits changed
```

### Simple Definition

> **Multiple-Bit Error:** An error in which more than one bit is changed during transmission.

---

## 3. Burst Error

A **burst error** occurs when **several consecutive bits** are affected or changed.

### Example

```text
Sent:     101101100101
Received: 101001111101
             ↑↑↑
        Consecutive bits affected
```

The affected bits occur in a sequence.

### Simple Definition

> **Burst Error:** An error in which several consecutive bits are changed during transmission.

---

## Difference Between Error Types

| Error Type         |  Number of affected bits | Example                 |
| ------------------ | -----------------------: | ----------------------- |
| Single-Bit Error   |                    1 bit | `101101 → 101001`       |
| Multiple-Bit Error |          More than 1 bit | `101101 → 111001`       |
| Burst Error        | Several consecutive bits | `101101100 → 101000100` |

### Easy Way to Remember

```text
Single-Bit   → One bit
Multiple-Bit → More than one bit
Burst Error  → Consecutive bits
```

---

# Error Detection Methods

Error-detection methods are techniques used to determine whether transmitted data contains an error.

Common methods are:

1. **Parity Check**
2. **Checksum**
3. **Cyclic Redundancy Check (CRC)**

```text
Error Detection
       │
       ├── Parity Check
       │
       ├── Checksum
       │
       └── CRC
```

## Key Point

> **Error detection does not necessarily correct the error. It only detects whether an error has occurred.**
# Error Detection Methods

## 1. Parity Check

**Parity Check** is a simple error-detection technique that adds an extra bit called a **parity bit** to the data.

The parity bit is used to make the number of `1`s either **even or odd**.

### Types of Parity

#### Even Parity

The total number of `1`s is  **even**.then add 0 

Example:

```text
Data:        1011001
Number of 1s = 4
Parity bit   = 0

Transmitted: 1011001'0`
```

If the number of `1`s is already even, parity bit = `0`.

Another example:

```text

The total number of `1`s is   **odd**.then add 1
Data:        1011000
Number of 1s = 3
Parity bit   = 1

Transmitted: 1011000'1'
```

Now total number of `1`s = 4 (even).

The total number of `1`s should be **even**.then add 0 
<img width="1092" height="564" alt="image" src="https://github.com/user-attachments/assets/bfef14a2-0811-45df-94fc-aa220a568619" />
<img width="1174" height="381" alt="image" src="https://github.com/user-attachments/assets/acafbbf8-86b7-4e57-a2b2-7636b408a73e" />

#### Odd Parity

The total number of `1`s should be **odd**.

Example:

```text
Data:        1011000
Number of 1s = 3
Parity bit   = 0
```

Total `1`s remains 3 → **odd**.

If the number of `1`s is even, parity bit = `1`.

### Advantages

* Simple and easy to implement
* Requires very little extra data
* Can detect many single-bit errors

### Disadvantage

* Cannot reliably detect errors when an **even number of bits** are changed.

---

# 2. Checksum

**Checksum** is an error-detection technique where data is divided into fixed-size blocks and the blocks are added together.

The final result is called the **checksum** and is sent along with the data.

### Basic Process

```text
Sender
   ↓
Divide data into blocks
   ↓
Add the blocks
   ↓
Generate Checksum
   ↓
Send Data + Checksum
   ↓
Receiver
   ↓
Calculate checksum again
   ↓
Compare
   ↓
Error / No Error
```

### Simple Example

Suppose we have three 4-bit blocks:

```text
1010
1100
1001
```

Add the blocks:

```text
  1010
+ 1100
+ 1001
------
100011
```

The result is processed according to the checksum method, and the resulting checksum is transmitted with the data.

At the receiver side, the checksum is recalculated.

```text
Checksum matches → No error detected
Checksum differs  → Error detected
```

### Advantages

* Simple to implement
* More effective than a simple parity check
* Commonly used in network protocols

### Disadvantage

* Cannot detect all possible errors
* Generally less powerful than CRC for detecting transmission errors

---

## Parity Check vs Checksum

| Feature         | Parity Check           | Checksum                  |
| --------------- | ---------------------- | ------------------------- |
| Basic idea      | Adds a parity bit      | Adds a calculated sum     |
| Extra data      | Usually 1 bit          | Multiple bits             |
| Complexity      | Very simple            | More complex              |
| Error detection | Limited                | Better than parity        |
| Common use      | Simple error detection | Network/data transmission |

### Exam Shortcut

```text
Parity Check → Count 1s
Checksum     → Add data blocks
CRC          → Polynomial division
```

