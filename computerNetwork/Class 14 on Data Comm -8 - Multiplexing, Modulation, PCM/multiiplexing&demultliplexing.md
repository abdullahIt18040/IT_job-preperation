<img width="1054" height="598" alt="image" src="https://github.com/user-attachments/assets/edfcbf2b-898f-4657-b18e-dd815b0f6974" />
# Multiplexer (MUX) and Demultiplexer (DEMUX)

## 1. Multiplexer (MUX)

### Definition
A **Multiplexer (MUX)** is a digital circuit that selects one input from many inputs and sends it to one output.

**বাংলা ব্যাখ্যা:** অনেকগুলো Input থেকে একটি Input নির্বাচন করে একটি Output-এ পাঠায়।

### Block Diagram
```text
 I0 ───┐
 I1 ───┤
 I2 ───┤──► [ 4-to-1 MUX ] ───► Y
 I3 ───┘
             ▲
          S0, S1
        (Select Lines)
```

### Example: 4-to-1 Multiplexer

A 4-to-1 MUX has:
- 4 inputs: I0, I1, I2, I3
- 2 select lines: S0, S1
- 1 output: Y

| S1 | S0 | Selected Input | Output |
|---|---|---|---|
| 0 | 0 | I0 | Y = I0 |
| 0 | 1 | I1 | Y = I1 |
| 1 | 0 | I2 | Y = I2 |
| 1 | 1 | I3 | Y = I3 |

### Formula

If the number of select lines is `n`, the maximum number of inputs is:

**Number of inputs = 2ⁿ**

Examples:
- 1 select line → 2 inputs
- 2 select lines → 4 inputs
- 3 select lines → 8 inputs
- 4 select lines → 16 inputs

### Applications
- Data selection
- Communication systems
- Digital signal processing
- Sharing a communication channel among multiple data sources

---

## 2. Demultiplexer (DEMUX)

### Definition
A **Demultiplexer (DEMUX)** is a digital circuit that takes one input and sends it to one selected output from many outputs.

**বাংলা ব্যাখ্যা:** একটি Input-কে Select line-এর সাহায্যে অনেকগুলো Output-এর মধ্যে নির্দিষ্ট একটি Output-এ পাঠায়।

### Block Diagram

```text
                  ┌──► Y0
                  ├──► Y1
 D ──► [ 1-to-4   ├──► Y2
       DEMUX ]    └──► Y3
            ▲
          S0, S1
       (Select Lines)
```

### Example: 1-to-4 Demultiplexer

A 1-to-4 DEMUX has:
- 1 input: D
- 2 select lines: S0, S1
- 4 outputs: Y0, Y1, Y2, Y3

Assuming the input is `D = 1`:

| S1 | S0 | Selected Output | Output Values (Y0, Y1, Y2, Y3) |
|---|---|---|---|
| 0 | 0 | Y0 | (1, 0, 0, 0) |
| 0 | 1 | Y1 | (0, 1, 0, 0) |
| 1 | 0 | Y2 | (0, 0, 1, 0) |
| 1 | 1 | Y3 | (0, 0, 0, 1) |

Only the selected output receives the input value. The other outputs remain 0 in this example.

### Formula

If the number of select lines is `n`, the number of outputs is:

**Number of outputs = 2ⁿ**

Examples:
- 1 select line → 2 outputs
- 2 select lines → 4 outputs
- 3 select lines → 8 outputs
- 4 select lines → 16 outputs

### Applications
- Data distribution
- Communication systems
- Digital circuit design
- Routing data to a selected destination

---

## 3. Difference Between MUX and DEMUX

| Feature | Multiplexer (MUX) | Demultiplexer (DEMUX) |
|---|---|---|
| Main function | Selects one input | Selects one output |
| Input | Multiple | Single |
| Output | Single | Multiple |
| Data flow | Many-to-one | One-to-many |
| Select lines | Choose the input | Choose the output |
| Example | 4-to-1 MUX | 1-to-4 DEMUX |

## 4. Easy Real-Life Example

**Multiplexer (MUX):** Imagine four CCTV cameras connected to a system that selects one camera's video to display on a single monitor.

**Demultiplexer (DEMUX):** Real-life example: মনে করো, একটি পানির পাইপ থেকে পানি চারটি পাইপের যেকোনো একটিতে পাঠানো হচ্ছে। কোন পাইপে পানি যাবে, তা একটি সুইচ দিয়ে নির্বাচন করা হয়। DEMUX-ও একইভাবে একটি Input-কে নির্দিষ্ট Output-এ পাঠায়।.

<img width="976" height="570" alt="image" src="https://github.com/user-attachments/assets/d48eb977-43cf-4131-bd34-fbdd84d94376" />
<img width="1073" height="589" alt="image" src="https://github.com/user-attachments/assets/82aa3bf1-d69b-4cc8-88dc-6661387ffcc9" />
<img width="1058" height="540" alt="image" src="https://github.com/user-attachments/assets/d0565353-168e-472d-9ed6-b234e23f32f7" />

<img width="1148" height="595" alt="image" src="https://github.com/user-attachments/assets/d9562b86-1c8a-4851-bba8-f0e29a0adee8" />


# Frequency Division Multiplexing (FDM)

## 1. Definition

**Frequency Division Multiplexing (FDM)** is a technique in which multiple signals are transmitted simultaneously through a single communication channel using different frequency bands.

**বাংলা ব্যাখ্যা:** একটি Communication Channel-এ আলাদা আলাদা Frequency ব্যবহার করে একাধিক Signal একই সময়ে পাঠানোর পদ্ধতিকে FDM বলে।

## 2. How Does FDM Work?

1. Multiple input signals are collected.
2. Each signal is assigned a different frequency band.
3. All signals are transmitted simultaneously through the same communication channel.
4. The receiver selects the required frequency to receive the desired signal.

## 3. Example: Radio Broadcasting

Suppose three radio stations use different frequencies:

- Radio Station A → 90 MHz
- Radio Station B → 95 MHz
- Radio Station C → 100 MHz

All three stations can broadcast at the same time using different frequencies.

When we tune a radio to 95 MHz, we receive Radio Station B.

**বাংলা ব্যাখ্যা:** প্রতিটি Radio Station আলাদা Frequency ব্যবহার করে। তাই তারা একই সময়ে সম্প্রচার করতে পারে। Radio-তে নির্দিষ্ট Frequency নির্বাচন করলে সেই Station-এর সম্প্রচার শোনা যায়।

## 4. Diagram

```text
Signal A ──► 90 MHz ──┐
Signal B ──► 95 MHz ──┼──► Multiplexer ──► Single Channel
Signal C ──► 100 MHz ─┘

                   Receiver
                       │
              Select required frequency
                       │
                 Desired Signal
```

## 5. Advantages

- Multiple signals can be transmitted simultaneously.
- Continuous transmission is possible.
- Suitable for radio and television broadcasting.

## 6. Disadvantages

- Requires sufficient bandwidth.
- Signals may interfere with each other if frequency bands are not properly separated.
- Guard bands may be required to reduce interference.

## 7. Applications

- Radio broadcasting
- Television broadcasting
- Cable television
- Communication systems

<img width="956" height="576" alt="image" src="https://github.com/user-attachments/assets/f0c02d7e-e1e1-4a18-b9b8-f46b82545ded" />

##  What is a Frequency Band?

A Frequency Band is a range of frequencies used to transmit a signal.

Example: 90 MHz to 100 MHz is a frequency band.
## Demultiplexing in FDM work as Radio 
<img width="695" height="561" alt="image" src="https://github.com/user-attachments/assets/0c827d9f-bf9b-4018-b654-340ffc68ad9c" />
## WDM(wavelength division multiplexing)
<img width="967" height="540" alt="image" src="https://github.com/user-attachments/assets/115ad0ff-341b-47ab-8868-629fdb5151e0" />

1. What is Wavelength?

Wavelength is the distance between two consecutive identical points of a wave, such as two consecutive crests or troughs.
 Wavelength Formula

λ = v / f

Where:

λ = Wavelength

v = Wave speed

f = Frequency
<img width="1095" height="602" alt="image" src="https://github.com/user-attachments/assets/7d88fd1e-47cd-453f-bce2-2ae8c8b461ae" />
# WDM (Wavelength Division Multiplexing)

## 1. What is WDM?

**WDM stands for Wavelength Division Multiplexing.**

WDM is a multiplexing technique that allows multiple optical signals to travel simultaneously through a single optical fiber using different wavelengths of light.

**বাংলায়:** WDM হলো এমন একটি প্রযুক্তি, যেখানে আলোর বিভিন্ন wavelength ব্যবহার করে একই optical fiber দিয়ে একসঙ্গে একাধিক signal পাঠানো হয়।

## 2. How Does WDM Work?

WDM works in four steps:

1. **Input Signals:** Multiple data signals are received.
2. **Multiplexer:** Each signal is converted into light with a different wavelength and combined.
3. **Optical Fiber:** All combined signals travel through a single optical fiber.
4. **Demultiplexer:** The receiver separates the signals according to their wavelengths.

## 3. WDM Diagram

```text
Signal 1 ──(λ1)──┐
Signal 2 ──(λ2)──┤
Signal 3 ──(λ3)──┤
                 ▼
          ┌─────────────┐
          │ Multiplexer │
          └──────┬──────┘
                 │
                 ▼
       Single Optical Fiber
          (λ1 + λ2 + λ3)
                 │
                 ▼
          ┌───────────────┐
          │ Demultiplexer │
          └───────┬───────┘
                  │
          ┌───────┼───────┐
          ▼       ▼       ▼
       Signal 1 Signal 2 Signal 3
```

Here, `λ` (Lambda) represents wavelength.

## 4. Types of WDM

### A. CWDM (Coarse Wavelength Division Multiplexing)

- Uses wavelength channels with relatively wide spacing.
- Supports fewer wavelength channels than typical DWDM systems.
- Often used in metropolitan and access networks.
- Generally less complex and less expensive.

### B. DWDM (Dense Wavelength Division Multiplexing)

- Uses closely spaced wavelength channels.
- Supports many optical channels over a single fiber.
- Suitable for high-capacity, long-distance communication.
- Commonly used in telecom backbone networks.

## 5. WDM vs FDM

| Feature | FDM | WDM |
|---|---|---|
| Full form | Frequency Division Multiplexing | Wavelength Division Multiplexing |
| Signal separation | Different frequencies | Different light wavelengths |
| Medium | Radio, copper and other communication systems | Optical fiber |
| Signal type | Commonly electrical/RF signals | Optical signals |
| Application | Radio broadcasting | Fiber-optic communication |

## 6. Advantages of WDM

- Increases the capacity of optical fiber.
- Transmits multiple signals simultaneously.
- Makes efficient use of existing fiber infrastructure.
- Supports high-speed data communication.
- Can increase capacity without installing additional fibers.

## 7. Disadvantages of WDM

- Equipment can be expensive.
- Requires precise optical components.
- System design and maintenance can be complex.

## 8. Real-Life Applications

- High-speed internet networks
- Telecommunications
- Undersea fiber-optic cables
- Data center interconnections
- Long-distance communication networks


## Total channel capacity 
<img width="811" height="528" alt="image" src="https://github.com/user-attachments/assets/4943b4b4-04df-4514-a65a-75c00bdc14c6" />
<img width="1111" height="528" alt="image" src="https://github.com/user-attachments/assets/33b0d5aa-9233-4848-b612-75a2c9be6361" />
<img width="1078" height="482" alt="image" src="https://github.com/user-attachments/assets/e2cd64fc-9171-4941-acc1-d0d281d239ac" />
## TDM
# Time Division Multiplexing (TDM)

## 1. What is TDM?

**TDM (Time Division Multiplexing)** is a technique in which multiple devices share a single communication channel by transmitting data at different time slots.

**বাংলায়:** TDM হলো এমন একটি পদ্ধতি, যেখানে একাধিক ডিভাইস একটি Communication Channel ব্যবহার করে, কিন্তু প্রত্যেকে নির্দিষ্ট সময়ে ডেটা পাঠায়।

**Example:** একটিমাত্র রাস্তা দিয়ে একাধিক গাড়ি পালাক্রমে চলার মতো।

## 2. How Does TDM Work?

Suppose three computers (A, B, and C) want to transmit data through a single communication channel.

```text
Computer A ──┐
Computer B ──┼──> MUX ──> Shared Channel ──> DEMUX ──> Receivers
Computer C ──┘
```

- **MUX (Multiplexer):** Combines data from multiple input devices.
- **Shared Channel:** Carries data from different devices in assigned time slots.
- **DEMUX (Demultiplexer):** Separates the received data and sends it to the correct destination.

### Time Slot Allocation

```text
Time ──────────────────────────────────>

|   A   |   B   |   C   |   A   |   B   |   C   |
   T1      T2      T3      T4      T5      T6
```

Each device transmits data during its assigned time slot.

## 3. What Is a Time Slot?

A **Time Slot** is a small, specific portion of time allocated to a device for transmitting data.

Example:

| Time Slot | Device |
|---|---|
| T1 | Computer A |
| T2 | Computer B |
| T3 | Computer C |
| T4 | Computer A |

The process repeats continuously.

## 4. Types of TDM

### A. Synchronous TDM

 <img width="974" height="513" alt="image" src="https://github.com/user-attachments/assets/114292fb-5800-4ecb-8ee7-5b83dd357df3" />
 
<img width="1059" height="578" alt="image" src="https://github.com/user-attachments/assets/fb8bafbe-d559-420e-8ae8-2d1c95e9bd35" />

- Each device gets a fixed time slot.
- Time slots are assigned even if a device has no data to transmit.
- Empty slots may waste bandwidth.
- The receiver knows the slot allocation in advance.

**Example:** A fixed schedule where A, B, and C transmit in turns.

### B. Statistical TDM (Asynchronous TDM)
<img width="1076" height="518" alt="image" src="https://github.com/user-attachments/assets/617fcf5b-2dca-454e-bebd-e6d2126d5812" />

- Time slots are allocated dynamically to devices that have data to send.
- Slots are not necessarily reserved for every device in every cycle.
- Usually uses bandwidth more efficiently than synchronous TDM.
- The transmitted data generally needs addressing or identification information.

**Example:** Only A and C have data, so the system allocates slots to A and C instead of reserving an empty slot for B.

## 5. Real-Life Applications of TDM

- Digital telephone communication systems.
- Digital data transmission systems.
- GSM cellular networks, which use TDMA for sharing radio resources.
- Multiplexing multiple digital data streams over a communication link.

## 6. Difference Between TDM and FDM

| Feature | TDM | FDM |
|---|---|---|
| Full Form | Time Division Multiplexing | Frequency Division Multiplexing |
| Resource divided | Time | Frequency |
| Transmission | Different time slots | Different frequency bands |
| Example | Taking turns to speak | Speaking on separate frequency channels |

## 7. Advantages of TDM

- Allows multiple devices to share one communication channel.
- Can improve channel utilization.
- Avoids the need for a separate channel for every device.
- Suitable for digital communication systems.

## 8. Disadvantages of TDM

- Requires accurate timing and synchronization.
- Synchronous TDM can waste slots when devices have no data.
- Delays may occur while a device waits for its assigned time slot.
- Statistical TDM requires additional control information to identify data sources.




# CDM and CDMA (Code Division Multiplexing)

## 1. What is CDM?

**CDM (Code Division Multiplexing)** is a technique in which multiple signals share the same communication channel using different codes to distinguish them.

**বাংলায়:** CDM হলো এমন একটি পদ্ধতি, যেখানে একাধিক সিগন্যাল একই Communication Channel ব্যবহার করে, কিন্তু প্রতিটি সিগন্যালকে আলাদা করার জন্য ভিন্ন কোড ব্যবহার করা হয়।

### Example

Imagine three users transmitting data simultaneously:

- User A uses Code A.
- User B uses Code B.
- User C uses Code C.

The receiver uses the appropriate code to recover the desired user's data.

## 2. How Does CDM Work?

```text
     User A (Code A) ──┐
                       │
     User B (Code B) ──┼──> Combiner
                       │        |
     User C (Code C) ──┘        v
                         Shared Communication
                                Channel
                                  |
                                  v
                              Receiver
                                  |
                         Code-based Detection
                                  |
                         Recover Desired Data
```

### Working Steps

1. Each user is assigned a unique code.
2. Each user's data is encoded using its assigned code.
3. Multiple encoded signals are transmitted over the same channel, potentially at the same time.
4. The receiver uses the appropriate code to recover the desired signal.

**Important:** The codes must have suitable correlation properties so that the receiver can distinguish the signals reliably.

## 3. What is CDMA?

**CDMA (Code Division Multiple Access)** is a multiple-access technology that allows multiple users to communicate over the same frequency band at the same time using different codes.

**বাংলায়:** CDMA হলো এমন একটি প্রযুক্তি, যেখানে একাধিক ব্যবহারকারী একই সময়ে একই Frequency Band ব্যবহার করে যোগাযোগ করতে পারে। প্রত্যেক ব্যবহারকারীর সিগন্যাল আলাদা করার জন্য ভিন্ন কোড ব্যবহৃত হয়।

### Real-Life Example

Imagine several people speaking simultaneously in a room using different languages.

A listener may focus on a language they understand. This is a simple analogy for distinguishing signals, although real CDMA uses mathematical codes rather than languages.

## 4. CDM vs CDMA

| Feature | CDM | CDMA |
|---|---|---|
| Full form | Code Division Multiplexing | Code Division Multiple Access |
| Meaning | A code-based signal multiplexing technique | A multiple-access communication technology |
| Main purpose | Combine and distinguish multiple signals using codes | Allow multiple users to share communication resources |
| Code usage | Different codes distinguish signals | Different user codes distinguish transmissions |
| Example | Code-based signal multiplexing | IS-95 cellular networks |

**Note:** CDM and CDMA are closely related terms and are sometimes used interchangeably in introductory networking materials.

## 5. CDM vs TDM vs FDM

| Feature | TDM | FDM | CDM |
|---|---|---|---|
| Full form | Time Division Multiplexing | Frequency Division Multiplexing | Code Division Multiplexing |
| Resource separation | Time slots | Frequency bands | Codes |
| Sharing method | Different times | Different frequencies | Different codes |
| Simultaneous transmission | Depends on slot assignment | Possible | Possible |
| Memory trick | Time | Frequency | Code |

### Simple Examples

- **TDM:** Users take turns transmitting.
- **FDM:** Users transmit on separate frequency bands.
- **CDM:** Signals share the channel using different codes.

## 6. Advantages of CDMA

- Multiple users can transmit simultaneously.
- Efficient sharing of radio spectrum is possible.
- Spread-spectrum techniques can provide resistance to certain types of interference.
- Code-based signal separation supports multiple users on shared resources.

## 7. Disadvantages of CDMA

- Requires more complex encoding and decoding.
- Interference can increase as the number of users grows.
- Power control is important in cellular systems to reduce the near-far problem.
- Performance depends on code properties, synchronization, and channel conditions.

## 8. Applications

- IS-95 (cdmaOne) mobile networks.
- CDMA2000 cellular networks.
- Some 3G mobile communication systems.
- Code-based spread-spectrum communication systems.

**Note:** Modern 4G LTE and 5G NR primarily use OFDM-based radio access techniques rather than traditional CDMA cellular access.

## 9. Important Exam Notes

- CDM stands for **Code Division Multiplexing**.
- CDMA stands for **Code Division Multiple Access**.
- CDMA allows multiple users to share the same frequency band at the same time.
- Different codes help distinguish users' signals.
- TDM separates transmissions by time.
- FDM separates transmissions by frequency.
- CDM separates signals using codes.

### Memory Trick

**TDM = Time**

**FDM = Frequency**

**CDM = Code**

**CDMA = Multiple users + Different codes**
<img width="912" height="588" alt="image" src="https://github.com/user-attachments/assets/1419a23d-3e39-4846-988e-9630247e8208" />
## 100 % asbe 
<img width="1056" height="525" alt="image" src="https://github.com/user-attachments/assets/44ef5ab4-191b-4bb3-92c9-8ddec7b421a1" />
<img width="1121" height="556" alt="image" src="https://github.com/user-attachments/assets/a244e07d-22d5-4158-81c0-bca674f2ed1c" />

<img width="1140" height="441" alt="image" src="https://github.com/user-attachments/assets/6329a24c-bab1-486e-abd8-35aa1dbefdc8" />

<img width="1137" height="661" alt="image" src="https://github.com/user-attachments/assets/4f437e18-0cf5-4971-a526-ccf43dc9bb56" />
<img width="1151" height="509" alt="image" src="https://github.com/user-attachments/assets/91e7dcae-8e43-4406-9a84-3204e6d4ba29" />


### MOdulation 
# Modulation and Demodulation

## 1. Modulation
<img width="1142" height="592" alt="image" src="https://github.com/user-attachments/assets/0ce99780-2b35-4db8-b5d9-13ab7e6aff5c" />


**Modulation** is the process of combining information with a carrier signal to make it suitable for long-distance transmission.


## 2. Demodulation

**Demodulation** is the process of recovering the original information from a received modulated signal.
<img width="859" height="548" alt="image" src="https://github.com/user-attachments/assets/c37b326a-5e2b-405a-bca4-d9434a7d8257" />

**Example:** A radio receiver uses demodulation to recover audio from a radio signal.

## 3. Modulation vs. Demodulation
<img width="1056" height="539" alt="image" src="https://github.com/user-attachments/assets/670efeef-bff7-495a-a6ec-3e7ae5be4192" />

| Modulation | Demodulation |
|---|---|
| Done at the transmitter | Done at the receiver |
| Prepares information for transmission | Recovers the original information |
| Uses a modulator | Uses a demodulator |

## 4. Communication System Diagram

```text
Message Signal
      |
      v
  Modulation
      |
      v
Communication Channel
      |
      v
 Demodulation
      |
      v
Original Message
```

## 5. Real-Life Example

**Radio Communication:**
1. A radio station uses modulation to transmit audio information.
2. The radio signal travels through the air.
3. A radio receiver uses demodulation to recover the audio.

## 6. Important Points

- Modulation is performed at the transmitter.
- Demodulation is performed at the receiver.
- AM changes amplitude.
- FM changes frequency.
- PM changes phase.


### Types of Modulation
<img width="1173" height="650" alt="image" src="https://github.com/user-attachments/assets/74eab77b-f5c4-4b8f-b3ae-2b4589c32304" />

- **AM (Amplitude Modulation):** Changes the amplitude of the carrier signal.
- **FM (Frequency Modulation):** Changes the frequency of the carrier signal.
- **PM (Phase Modulation):** Changes the phase of the carrier signal.


<img width="831" height="515" alt="image" src="https://github.com/user-attachments/assets/b61e05da-687b-4834-bcf7-be5842866a18" />
# Wave Properties: Amplitude, Wavelength, Frequency, and Phase

## 1. Amplitude (A)

**Amplitude** is the maximum height of a wave measured from its resting position.

- **Symbol:** A
- **Unit:** Meter (m)

**Remember:** Amplitude = Wave height from the middle position.

## 2. Wavelength (λ)

**Wavelength** is the distance between two consecutive crests or two consecutive troughs.

- **Symbol:** λ (Lambda)
- **Unit:** Meter (m)
<img width="915" height="560" alt="image" src="https://github.com/user-attachments/assets/ebb0844c-c66b-4234-aae4-db8ff30bec8a" />

**Remember:** Wavelength = Distance.

## 3. Frequency (f)

**Frequency** is the number of complete wave cycles that pass a point in one second.
<img width="922" height="553" alt="image" src="https://github.com/user-attachments/assets/4ae2c7e7-d419-446c-a2a6-1cfbf0001f4f" />


- **Symbol:** f
- **Unit:** Hertz (Hz)

**Example:** 5 Hz means 5 cycles per second.

**Remember:** Frequency = Cycles per second.

<img width="1066" height="567" alt="image" src="https://github.com/user-attachments/assets/c2d7b10d-1d9b-4b2c-90dd-b3b5e5521611" />

<img width="997" height="223" alt="image" src="https://github.com/user-attachments/assets/9e66b027-c7aa-4ba8-9365-0b5707bd74e9" />

<img width="941" height="601" alt="image" src="https://github.com/user-attachments/assets/46f27812-6fe5-4243-87c9-32c6844e0008" />


# Amplitude Modulation (AM)

## Definition
**Amplitude Modulation (AM)** is a type of modulation in which the amplitude of the carrier signal changes according to the message signal, while the carrier frequency remains constant.
<img width="1175" height="570" alt="image" src="https://github.com/user-attachments/assets/ffd6c8b3-f65a-4bdd-9f23-2778e0147bc8" />
## How It Works
- A message signal contains information, such as voice.
- A carrier signal carries the information.
- In AM, the carrier signal's amplitude changes according to the message signal.

## Example
AM radio broadcasting uses amplitude modulation to transmit audio signals.

## Important Points
- **Changed:** Amplitude
- **Constant:** Carrier frequency
- **Used in:** AM radio broadcasting

## Remember
**AM = Amplitude Changes.**
# Frequency Modulation (FM)

## Definition
**Frequency Modulation (FM)** is a type of modulation in which the frequency of the carrier signal changes according to the message signal, while the carrier amplitude remains constant.

<img width="1107" height="564" alt="image" src="https://github.com/user-attachments/assets/163c56de-bdcf-46cf-a748-de200b33deb6" />
## How It Works
- A message signal contains information, such as voice.
- A carrier signal carries the information.
- In FM, the carrier signal's frequency changes according to the message signal.

## Example
FM radio broadcasting uses frequency modulation to transmit audio signals.

## Important Points
- **Changed:** Frequency
- **Constant:** Amplitude
- **Used in:** FM radio broadcasting

## Remember
**FM = Frequency Changes.**
# Phase Modulation (PM)

## Definition
**Phase Modulation (PM)** is a type of modulation in which the phase of the carrier signal changes according to the message signal, while the carrier amplitude remains constant.
<img width="1118" height="573" alt="image" src="https://github.com/user-attachments/assets/3a7a5d70-7d10-4623-9435-22215bd524df" />
## How It Works
- A message signal contains information, such as voice or data.
- A carrier signal carries the information.
- In PM, the phase of the carrier signal changes according to the message signal.

## Example
Phase modulation is used in digital communication systems and some radio communication systems.

## Important Points
- **Changed:** Phase
- **Constant:** Amplitude
- **Used in:** Radio and digital communication systems

## Remember
**PM = Phase Changes.**

# Pulse Code Modulation (PCM)

## Definition
**Pulse Code Modulation (PCM)** is a technique used to convert an analog signal into digital data.
<img width="684" height="467" alt="image" src="https://github.com/user-attachments/assets/d010e76e-a6a2-4796-97b1-9fe5fc36c50f" />

## How It Works
PCM has three main steps:
<img width="1116" height="589" alt="image" src="https://github.com/user-attachments/assets/b7503933-7308-443a-bc06-c914d4b0e20a" />
<img width="659" height="615" alt="image" src="https://github.com/user-attachments/assets/9ff776e6-74f8-41f1-95c0-8512e22d5453" />
<img width="1177" height="577" alt="image" src="https://github.com/user-attachments/assets/f74a3fbb-42a7-4703-8d68-5e1eb2b1be6a" />
<img width="1128" height="455" alt="image" src="https://github.com/user-attachments/assets/b3a19c41-14ce-4403-8aaf-f461c7bd5e87" />
<img width="1159" height="569" alt="image" src="https://github.com/user-attachments/assets/7cd4fabc-401a-437d-833c-464ec340c852" />


1. **Sampling:** Measures the analog signal at regular time intervals.
2. **Quantization:** Assigns each sample to a suitable discrete level.
3. **Encoding:** Converts each quantized sample into binary code (0s and 1s).

## Example
Digital audio recording and digital telephone systems use PCM to represent audio as digital data.

## Important Points
- **Full Form:** Pulse Code Modulation
- **Input:** Analog signal
- **Output:** Digital data
- **Main Steps:** Sampling, Quantization, Encoding

## Remember
**PCM = Sampling + Quantization + Encoding.**



![Uploading image.png…]()

