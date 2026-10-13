## Data communication


# Data Transmission Based on Signal Type
<img width="1052" height="495" alt="image" src="https://github.com/user-attachments/assets/3208df83-b962-4b84-97fd-048045ef9418" />

Data transmission is divided into two types:

### 1. Analog Transmission
- Uses continuous signals.
- Example: Analog radio.

**Wave:** `〰️〰️〰️`

### 2. Digital Transmission
- Uses discrete signals (0 and 1).
- Example: Computer networks.

**Wave:** `▁▁▔▔▁▁▔▔`

### Difference

| Analog | Digital |
|---|---|
| Continuous signal | Discrete signal |
| Sine wave | Square wave |
# Types of Data Transmission Based on Direction

### Data transmission based on direction has **three types**: vey very importent. 
<img width="1023" height="422" alt="image" src="https://github.com/user-attachments/assets/fe935c77-0fab-49c7-a82d-4d4686a2cc7c" />

### 1. Simplex
- Data flows in one direction only.
- Example: Keyboard to computer.
- **Diagram:** `A ───→ B`

### 2. Half-Duplex
<img width="1053" height="477" alt="image" src="https://github.com/user-attachments/assets/c19af2af-5525-47df-ab16-6e1c665fbbbc" />

- Data flows in both directions, but one at a time.
- Example: Walkie-talkie.
- **Diagram:** `A ←──→ B` *(one at a time)*

### 3. Full-Duplex
<img width="787" height="483" alt="image" src="https://github.com/user-attachments/assets/36208047-4031-4d7a-b925-50c907785c5f" />

- Data flows in both directions simultaneously.
- Example: Telephone call.
- **Diagram:** `A ⇄ B` *(at the same time)*

## Difference

| Simplex | Half-Duplex | Full-Duplex |
|---|---|---|
| One-way | Both ways, one at a time | Both ways simultaneously |
| Keyboard → Computer | Walkie-talkie | Telephone |

**Memory Trick:**
- Simplex = One-way
- Half-Duplex = Take turns
- Full-Duplex = Both at once
<img width="1109" height="579" alt="image" src="https://github.com/user-attachments/assets/29386da3-7bbd-40dc-995c-8c36eb954a1a" />
## 2. Based on Transmission Method

### 1. Serial Transmission
- Sends **one bit at a time**.
- Example: USB communication.
- Diagram: `1 → 0 → 1 → 1`

### 2. Parallel Transmission
- Sends **multiple bits simultaneously** through multiple lines.
- Example: Traditional parallel printer port.

```text
1 ─────→
0 ─────→
1 ─────→
1 ─────→
```

**Memory Trick:**
- Serial = One bit at a time.
- Parallel = Multiple bits at a time.
- 
<img width="1111" height="569" alt="image" src="https://github.com/user-attachments/assets/85321c35-d69a-4b76-bd96-61dab4f0e87b" />
### 1. Serial Transmission

- **Definition:** Sends data one bit at a time.
- **Example:** USB communication.
- **Diagram:**

```text
1 → 0 → 1 → 1 → 0
```

**Remember:** Serial = One bit at a time.
## Types of Serial Transmission

### 1. Asynchronous Transmission

<img width="929" height="455" alt="image" src="https://github.com/user-attachments/assets/9224c802-6f44-4a58-9a84-bd09454f43b1" />
<img width="746" height="305" alt="image" src="https://github.com/user-attachments/assets/e6846e6a-8f71-4ec6-9d6a-3939488cbdc9" />

- Sends data one character at a time.
- Uses start and stop bits.
- Example: UART.

### 2. Synchronous Transmission
<img width="969" height="354" alt="image" src="https://github.com/user-attachments/assets/8698e007-9db6-411c-9224-d647f39ccc19" />
<img width="735" height="211" alt="image" src="https://github.com/user-attachments/assets/6f86a2e2-63b9-45a9-876b-a5326b76f3a7" />

- Sends data in blocks or frames.
- Uses synchronized timing.
- Example: SPI.

**Memory Trick:**
- Asynchronous = Start and Stop bits.
- Synchronous = Synchronized timing.
### Isochronous Transmission

- **Definition:** Sends data at regular, fixed time intervals.
- **Use:** Real-time audio and video.
- **Example:** Video calling.

**Diagram:**
```text
Data 1 ── Data 2 ── Data 3 ── Data 4
        Equal Time Intervals
```

**Memory Trick:** Isochronous = Fixed time intervals.
<img width="1022" height="225" alt="image" src="https://github.com/user-attachments/assets/0ba3f114-2f57-4766-b6da-b64d188bfe78" />

<img width="863" height="450" alt="image" src="https://github.com/user-attachments/assets/28c1ec4d-61e8-4b98-8151-8badfdec5d0f" />
### Parallel Transmission
<img width="1019" height="507" alt="image" src="https://github.com/user-attachments/assets/d5277250-54ba-4a7c-8a8e-56f878fb6948" />

**Definition:** Parallel Transmission is a method of data transmission in which multiple bits are sent simultaneously from sender to receiver through multiple lines..

- **Uses:** Short-distance data transmission.
- **Example:** Traditional computer-to-printer communication using a parallel port.

**Diagram:**

```text
Sender                 Receiver
  Bit 1 ────────────────►
  Bit 2 ────────────────►
  Bit 3 ────────────────►
  Bit 4 ────────────────►
```

**Advantages:**
- Transfers multiple bits simultaneously.
- Can provide high speed over short distances.

**Disadvantages:**
- Requires multiple communication lines.
- Less suitable for long distances due to signal timing and interference issues.

**Remember:** Parallel Transmission = Multiple bits at the same time through multiple lines.

