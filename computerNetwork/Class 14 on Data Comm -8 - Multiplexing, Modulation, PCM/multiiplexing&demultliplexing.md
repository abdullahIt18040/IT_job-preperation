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

**Demultiplexer (DEMUX):** Imagine one input signal routed to a selected output line among several output lines.

## 5. Important Exam Points

- MUX stands for **Multiplexer**.
- DEMUX stands for **Demultiplexer**.
- MUX performs **many-to-one** data selection.
- DEMUX performs **one-to-many** data distribution.
- The number of selectable inputs or outputs is generally `2ⁿ`, where `n` is the number of select lines.
- A 4-to-1 MUX requires 2 select lines.
- A 1-to-4 DEMUX requires 2 select lines.

### Quick Memory Trick

**MUX:** Many → One

**DEMUX:** One → Many

## 6. MCQ Practice

**Question 1:** Which device selects one input from multiple inputs and sends it to a single output?

A. Decoder  
B. Multiplexer  
C. Encoder  
D. Demultiplexer

**Answer:** B. Multiplexer

**Question 2:** How many select lines are required for an 8-to-1 MUX?

A. 2  
B. 3  
C. 4  
D. 8

**Answer:** B. 3, because 2³ = 8.

**Question 3:** Which device routes a single input to one of multiple outputs?

A. Multiplexer  
B. Encoder  
C. Demultiplexer  
D. Counter

**Answer:** C. Demultiplexer

**Question 4:** How many outputs can a 1-to-16 DEMUX select?

A. 2  
B. 4  
C. 8  
D. 16

**Answer:** D. 16. It requires 4 select lines because 2⁴ = 16.
