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
<img width="1065" height="588" alt="image" src="https://github.com/user-attachments/assets/cb586ef3-33ee-492c-869e-7b05867e84a6" />
## Data Transmission Based on Delivery

Based on delivery, data transmission is classified into four types:

### 1. Unicast
**Definition:** Data is sent from one sender to one specific receiver.

- **Communication:** One-to-One
- **Example:** Sending an email to one person.

### 2. Broadcast
**Definition:** Data is sent from one sender to all devices in a network.

- **Communication:** One-to-All
- **Example:** An ARP request in a local IPv4 network.

### 3. Multicast
**Definition:** Data is sent from one sender to a specific group of receivers.

- **Communication:** One-to-Selected Group
- **Example:** Streaming a live video to a subscribed group.

### 4. Anycast

<img width="1195" height="527" alt="image" src="https://github.com/user-attachments/assets/47d5a12c-bd01-4f4d-95df-6186f934810c" />


select best one which is optimal among goupe of receiver

**Definition:** Data is sent from one sender to the nearest or best receiver among a group of receivers.
- **Communication:** One-to-One from a Group
- **Example:** DNS services using anycast to direct requests to an appropriate server.

<img width="1015" height="564" alt="image" src="https://github.com/user-attachments/assets/65be817d-31a4-49b2-9bbf-230c58db1137" />

## Transmission Impairment

**Definition:** Transmission impairment is when   a signal becomes weaker or changes while traveling from sender to receiver.

### Types of Transmission Impairment

1. **Attenuation:** The signal loses strength as it travels over a distance.

<img width="820" height="550" alt="image" src="https://github.com/user-attachments/assets/5c7081c1-f5f6-46c3-8edc-c1e915543d69" />

- **Cause:** Long transmission distance.
- **Example:** A weak Wi-Fi signal far from the router.
- **Recovery:**
  - **Amplifier:** Increases the strength of an analog signal.
  - **Repeater:** Regenerates and retransmits a weakened digital signal.

**Remember:** Attenuation = Loss of signal strength.

3. **Distortion:** The signal changes its shape or form during transmission.

<img width="980" height="515" alt="image" src="https://github.com/user-attachments/assets/83aaf9c1-a5dd-4316-aafb-ae068244427a" />


- **Cause:** Different parts of a signal travel at different speeds or experience different delays.
- **Example:** A distorted voice during a phone call.
- **Recovery:** Use equalizers or appropriate communication equipment ( like if we are used copper then we should used pure copper) to reduce distortion.

   - Example: A distorted audio signal during a call.

5. **Noise:** Unwanted signals interfere with the original signal.

<img width="1107" height="568" alt="image" src="https://github.com/user-attachments/assets/1a683f43-7e43-48d4-b7a5-4e93d836f50d" />

### Noise

**Definition:** Noise is an unwanted signal that interferes with the original signal during transmission.

- **Cause:** Electrical interference or electromagnetic interference.

- - Electrical Interference (বৈদ্যুতিক বিঘ্ন): বৈদ্যুতিক যন্ত্র বা তার থেকে উৎপন্ন অবাঞ্ছিত সিগন্যাল মূল ডেটা সিগন্যালকে বাধাগ্রস্ত করে।
উদাহরণ: মোটর বা বৈদ্যুতিক যন্ত্রের কারণে ডেটা সিগন্যালে সমস্যা হওয়া।
- Electromagnetic Interference (তড়িৎচুম্বকীয় বিঘ্ন): বাইরের তড়িৎচুম্বকীয় ক্ষেত্রের কারণে মূল সিগন্যাল বাধাগ্রস্ত বা বিকৃত হওয়া।
  Interference = বিঘ্ন বা বাধা।
  
- **Example:** Static sound during a phone call.
- **Reduction:** Use shielding, filters, or error-correction techniques.

**Remember:** Noise = Unwanted signal interference.

   - Example: Static noise during a phone call.



## Noise

**Definition:** Noise is an unwanted signal that interferes with the original signal during transmission.

**বাংলা:** ডেটা ট্রান্সমিশনের সময় মূল সিগন্যালের সঙ্গে অনাকাঙ্ক্ষিত সিগন্যাল মিশে মূল সিগন্যালকে বাধাগ্রস্ত করলে তাকে **Noise** বলে।

### Types of Noise

1. **Thermal Noise (তাপীয় নয়েজ)**
   - **Definition:** Caused by the random movement of electrons.
   - **বাংলা:** ইলেকট্রনের অনিয়মিত চলাচলের কারণে সৃষ্টি হয়।
   - **Example:** Background noise in electronic circuits.

2. **Induced Noise (বাহ্যিক উৎসজনিত নয়েজ)**
   - **Definition:** Caused by external electromagnetic sources.
   - **বাংলা:** বাইরের বৈদ্যুতিক বা তড়িৎচুম্বকীয় উৎসের কারণে সৃষ্টি হয়।
   - **Example:** Interference caused by an electric motor.

3. **Crosstalk (পারস্পরিক সিগন্যাল বিঘ্ন)**
   - **Definition:** Occurs when a signal from one communication channel interferes with another.
   - **বাংলা:** একটি যোগাযোগ চ্যানেলের সিগন্যাল অন্য চ্যানেলের সিগন্যালকে বাধাগ্রস্ত করলে তাকে Crosstalk বলে।
   - **Example:** One telephone line's signal interfering with another line.

4. **Impulse Noise (আকস্মিক নয়েজ)**
   - **Definition:** Sudden, high-intensity noise caused by events such as lightning or electrical switching.
   - **বাংলা:** বজ্রপাত বা বৈদ্যুতিক সুইচিংয়ের মতো ঘটনার কারণে হঠাৎ তীব্র নয়েজ সৃষ্টি হয়।
   - **Example:** A sudden burst of noise during a phone call.

### Example of Noise
Static sound or unwanted disturbance during a phone call.

**বাংলা:** ফোনে কথা বলার সময় খসখসে বা অপ্রয়োজনীয় শব্দ শোনা।

### Noise Reduction Techniques
- **Shielding:** Protects cables from external interference. (বাইরের বিঘ্ন থেকে তারকে সুরক্ষিত রাখে।)
- **Filters:** Reduce unwanted signal components. (অপ্রয়োজনীয় সিগন্যাল কমায়।)
- **Error Correction:** Detects and corrects certain transmission errors. (ডেটা ট্রান্সমিশনের কিছু ত্রুটি শনাক্ত ও সংশোধন করে।)

### Remember for Job Exams
- **Thermal** = Random movement of electrons
- **Induced** = External electromagnetic source
- **Crosstalk** = One channel interferes with another
- **Impulse** = Sudden, high-intensity noise

**বাংলায় মনে রাখার কৌশল:**
- Thermal = ইলেকট্রনের অনিয়মিত চলাচল
- Induced = বাইরের উৎস
- Crosstalk = এক লাইনের সিগন্যাল অন্য লাইনে বিঘ্ন ঘটায়
- Impulse = হঠাৎ তীব্র নয়েজ

## SNR (Signal-to-Noise Ratio)

**Definition:** SNR is the ratio of signal power to noise power in a communication system.

**বাংলা:** মূল সিগন্যালের শক্তি ও নয়েজের শক্তির অনুপাতকে SNR বলে।

### Formula
<img width="764" height="432" alt="image" src="https://github.com/user-attachments/assets/393aa8cb-40c4-45a6-bc99-2b5e79467e0b" />
<img width="792" height="335" alt="image" src="https://github.com/user-attachments/assets/a322ec18-d574-4fb7-a4af-0f5d52a24d14" />


### Key Points
- **High SNR:** Better signal quality and less noise relative to the signal.
- **Low SNR:** Poorer signal quality and more noise relative to the signal.
- SNR is commonly expressed in **decibels (dB)**.

### Remember for Job Exams
- **SNR = Signal Power / Noise Power**
- **Higher SNR = Better signal quality**
- **Lower SNR = Poorer signal quality**
<img width="919" height="436" alt="image" src="https://github.com/user-attachments/assets/88f02911-8d63-430f-844e-eda87e3fe160" />
<img width="821" height="463" alt="image" src="https://github.com/user-attachments/assets/9669c839-683e-48a9-b4d7-9b84d296e672" />
<img width="1002" height="594" alt="image" src="https://github.com/user-attachments/assets/156032d0-4735-48d2-98b1-a102f4d1fa85" />


