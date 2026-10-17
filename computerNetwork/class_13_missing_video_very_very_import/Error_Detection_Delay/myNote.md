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
 <img width="736" height="322" alt="image" src="https://github.com/user-attachments/assets/280ee955-2dd1-478e-947c-cd3f1da2d319" />

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
<img width="718" height="320" alt="image" src="https://github.com/user-attachments/assets/307549af-3c55-4b89-b393-6b541bacea4b" />

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

<img width="615" height="266" alt="image" src="https://github.com/user-attachments/assets/a947006f-eadb-472b-9f84-6ffe8b24ae00" />

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

when data send the =  The total number of `1`s should be even. (data+parity)
if 
The total number of `1`s is  **even**.then add 0 
if 
The total number of `1`s is  **odd **.then add 1

Example:

<img width="407" height="281" alt="image" src="https://github.com/user-attachments/assets/d4f0d5b5-f0e7-4962-9095-7751b29a361d" />


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

#### Odd Parity

when data send the =  The total number of `1`s should be Odd. (data+parity)
if 
The total number of `1`s is  **even**.then add 1 
if 
The total number of `1`s is  **odd **.then add 0
The total number of `1`s should be **odd**.

Example:
<img width="405" height="350" alt="image" src="https://github.com/user-attachments/assets/3c85c2d9-9320-4d3d-bc09-d917184ab974" />


```text
Data:        1011000
Number of 1s = 3
Parity bit   = 0
```
<img width="613" height="215" alt="image" src="https://github.com/user-attachments/assets/d800e205-69b3-4665-a0ce-32326e45577d" />

Total `1`s remains 3 → **odd**.

If the number of `1`s is even, parity bit = `1`.
<img width="546" height="185" alt="image" src="https://github.com/user-attachments/assets/2be2838a-133e-4217-aba4-e194fad397ab" />

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
<img width="1046" height="168" alt="image" src="https://github.com/user-attachments/assets/878218d0-b89d-451f-9de4-df55d288dd66" />

<img width="983" height="451" alt="image" src="https://github.com/user-attachments/assets/cf16da65-79a1-4f38-a39a-6b3d201b35ec" />

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
<img width="1151" height="606" alt="image" src="https://github.com/user-attachments/assets/f929c271-2480-458c-8a5c-17a119a26b46" />


<img width="416" height="639" alt="image" src="https://github.com/user-attachments/assets/d09d58b2-68c6-4218-8e12-e9490f6f1508" />

<img width="999" height="133" alt="image" src="https://github.com/user-attachments/assets/97b11f6a-b278-4c3f-9355-94ec34cf0651" />

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

<img width="937" height="324" alt="image" src="https://github.com/user-attachments/assets/3fd814d6-0fae-4d1f-be08-a1a220443b64" />

## CRC 
<img width="970" height="635" alt="image" src="https://github.com/user-attachments/assets/5066e704-a61a-4740-b4a3-4081f666ea9e" />

<img width="969" height="790" alt="image" src="https://github.com/user-attachments/assets/7c4428eb-1a00-4681-a60f-8f2a545b2016" />

<img width="1149" height="511" alt="image" src="https://github.com/user-attachments/assets/3f9423cd-4ae9-475e-ad18-8910fbde6344" />

if Divisor given polyomial then it convert binary 
<img width="1132" height="610" alt="image" src="https://github.com/user-attachments/assets/cbe2d7b1-049a-45f4-8dce-3a136d38c0d8" />
<img width="1432" height="608" alt="image" src="https://github.com/user-attachments/assets/e8d97907-6f84-4314-a18c-6a1313a58fc1" />
<img width="1309" height="493" alt="image" src="https://github.com/user-attachments/assets/23c3d558-b99e-4c36-a025-2acf404ff4be" />
<img width="828" height="402" alt="image" src="https://github.com/user-attachments/assets/e50c7998-244f-4748-b024-98379bfb57f7" />
## receiver side
<img width="644" height="448" alt="image" src="https://github.com/user-attachments/assets/7e69f904-71b9-4cc5-b923-5d47b30d631b" />


# Data Rate Limit

## Definition
**Data Rate Limit** is the maximum amount of data that can be transmitted over a network per second.

## Explanation (Bangla)
একটি নেটওয়ার্কের মাধ্যমে প্রতি সেকেন্ডে সর্বোচ্চ কত বিট ডেটা পাঠানো যায়, তাকে Data Rate Limit বলে।

## Example
If a network has a data rate limit of **100 Mbps**, it can transmit data at a maximum rate of 100 megabits per second under ideal conditions.

## Units
- bps — bits per second
- Kbps — kilobits per second
- Mbps — megabits per second
- Gbps — gigabits per second

## Important Note
**Data Rate Limit vs. Rate Limiting**

- **Data Rate Limit:** The maximum data transmission speed of a network connection.
- **Rate Limiting:** the number of requests allowed within a specific time.
- **Rate Limiting:** নির্দিষ্ট সময়ে কতগুলো request করা যাবে তার সীমা।

## Key Point for Job Exams
Remember: **Data Rate = Number of bits transmitted per second.**
# Factors Affecting Data Rate

## Definition
**Data Rate** is the number of bits transmitted over a network per second.

**বাংলা:** প্রতি সেকেন্ডে যে পরিমাণ বিট ডেটা প্রেরণ করা হয়, তাকে Data Rate বলে।

## Three Main Factors

### 1. Available Bandwidth
**English:** Higher bandwidth allows a higher data rate.

**বাংলা:** ব্যান্ডউইথ বেশি হলে বেশি গতিতে ডেটা পাঠানো যায়।

### 2. Signal Levels
**English:** More signal levels can transmit more bits per signal.

**বাংলা:** সিগন্যালের লেভেল বেশি হলে প্রতি সিগন্যালে বেশি বিট ডেটা পাঠানো যায়।

### 3. Channel Quality
**English:** Better channel quality reduces noise and errors, allowing a higher data rate.

**বাংলা:** চ্যানেলের মান ভালো হলে নয়েজ ও ডেটা ট্রান্সমিশনের ভুল কম হয়, ফলে বেশি ডেটা পাঠানো যায়।

## Key Point for Job Exams

Data Rate depends on:

1. Available Bandwidth
2. Signal Levels
3. Channel Quality

**Channel Quality ** have two channel 1.noiseless channel and noisy channel .



<img width="863" height="626" alt="image" src="https://github.com/user-attachments/assets/9dee9d47-f6c5-443d-ac10-d506ead08309" />


<img width="871" height="230" alt="image" src="https://github.com/user-attachments/assets/294be282-43ab-49bd-93fb-6f37b5d79c48" />
<img width="877" height="607" alt="image" src="https://github.com/user-attachments/assets/4771b641-532b-43b6-ad3d-dff0b4d4e8e2" />
<img width="1326" height="555" alt="image" src="https://github.com/user-attachments/assets/08422271-c004-49d5-aa69-4eaccacd3fe2" />

<img width="883" height="615" alt="image" src="https://github.com/user-attachments/assets/272453e3-a06e-4dda-a8b0-3555d007c9cd" />
<img width="892" height="654" alt="image" src="https://github.com/user-attachments/assets/c231bc43-e76a-4c8d-abbe-a6221cec2c6f" />
<img width="868" height="636" alt="image" src="https://github.com/user-attachments/assets/0955f800-eccb-4fdd-91fe-b3f92c4a947e" />
<img width="880" height="372" alt="image" src="https://github.com/user-attachments/assets/46d5bd71-bd5f-4a04-85d3-be55c0b2e096" />
<img width="856" height="183" alt="image" src="https://github.com/user-attachments/assets/87034be2-7535-4d0e-86ac-c051cd36d854" />

<img width="885" height="428" alt="image" src="https://github.com/user-attachments/assets/d01b2657-6210-47a6-834f-33727ffad09e" />



