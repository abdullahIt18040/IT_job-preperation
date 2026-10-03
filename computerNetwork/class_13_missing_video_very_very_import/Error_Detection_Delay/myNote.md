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
