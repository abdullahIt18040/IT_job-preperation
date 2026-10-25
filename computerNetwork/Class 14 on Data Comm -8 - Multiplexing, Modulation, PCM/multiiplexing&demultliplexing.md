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




