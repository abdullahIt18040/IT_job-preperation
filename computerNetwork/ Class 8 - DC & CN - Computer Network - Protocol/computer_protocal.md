Question
```
Synthia wants to send an email to her friend. She sends the email through the Application Layer and Transport Layer. Draw a diagram showing how the email is transmitted from Synthia (sender) to her friend (receiver), including the protocols used at each layer.
```
<img width="977" height="607" alt="image" src="https://github.com/user-attachments/assets/c4d551fb-081c-4ec0-b073-a7516fd81fab" />

<img width="1115" height="605" alt="image" src="https://github.com/user-attachments/assets/434d413e-2730-40e6-8876-2af5c19e6003" />
<img width="613" height="433" alt="image" src="https://github.com/user-attachments/assets/61ba4578-8a7c-4115-a4aa-753fecb64e8c" />
<img width="835" height="416" alt="image" src="https://github.com/user-attachments/assets/a24f89a9-701b-48c0-b42a-381bcbdadbdd" />
<img width="991" height="515" alt="image" src="https://github.com/user-attachments/assets/fb07a498-40b7-47a0-a4a5-6d39d6ebb2b6" />

<img width="677" height="360" alt="image" src="https://github.com/user-attachments/assets/f6962b16-fc88-4b4b-910c-335544917f4b" />
<img width="988" height="518" alt="image" src="https://github.com/user-attachments/assets/34453993-94e9-4fd3-83c3-d380a2f4455b" />
<img width="654" height="420" alt="image" src="https://github.com/user-attachments/assets/3dc42fa9-174b-4d4d-affd-1d866d6d7e34" />
<img width="778" height="363" alt="image" src="https://github.com/user-attachments/assets/152e0745-5eab-49ca-8ff9-528a8e02cf9c" />
<img width="830" height="410" alt="image" src="https://github.com/user-attachments/assets/724b5533-43b1-4fb0-9f37-74d4a51f5b30" />
<img width="901" height="478" alt="image" src="https://github.com/user-attachments/assets/acc178a5-34b0-42d7-8dfe-b0f4adb8f5c2" />
<img width="539" height="602" alt="image" src="https://github.com/user-attachments/assets/c6e137e4-d887-4089-a9b5-11d6b20c0eea" />

<img width="853" height="423" alt="image" src="https://github.com/user-attachments/assets/cfee1424-5d67-4cec-9bea-4da09d84e385" />


<img width="548" height="288" alt="image" src="https://github.com/user-attachments/assets/3532a5ac-b5c4-4f08-a36c-d4d848992588" />
## very very importent (NAT)

<img width="856" height="475" alt="image" src="https://github.com/user-attachments/assets/4d75599c-59a5-4d50-a87e-ae5d57c3092e" />


Answer
### (a) Why was NAT necessary?
```
The original IPv4 addressing system uses a 32-bit IP address.

Therefore, the total number of IPv4 addresses is:

$$ 2^{32}=4,294,967,296 $$

Approximately 4.3 billion addresses.

As the number of computers, smartphones, servers, and other Internet-connected devices increased, IPv4 addresses became insufficient.

Main problems
IPv4 provides only about 4.3 billion addresses.
Many addresses are reserved for special purposes.
The Internet grew rapidly.
Organizations needed many IP addresses.
Public IPv4 addresses became scarce.

To reduce the demand for public IPv4 addresses, NAT (Network Address Translation) was introduced.

NAT allows many devices inside a private network to share one public IP address when accessing the Internet.
```
## (b) NAT Translation Process
```
Suppose an employee has:

Private IP: 172.168.1.5

and wants to access:

www.example.com

The communication works approximately like this:

Employee PC
Private IP
172.168.1.5
      |
      | 1. Web Request
      ↓
+------------------+
|   NAT Router     |
|                  |
| Private:         |
| 172.168.1.5      |
|                  |
| Public:          |
| 203.0.113.10    |
+------------------+
      |
      | 2. Translated Request
      ↓
    Internet
      |
      ↓
External Web Server
Step 1: Internal computer creates a request

The employee's computer sends a request:

Source IP      = 172.168.1.5
Source Port    = 5000
Destination IP = Web Server IP
Destination Port = 80/443

The source IP is the internal address.

Step 2: Request reaches the NAT router

The NAT router receives the packet.

The router knows that:

172.168.1.5

is an internal/private network address.

The router replaces the private source IP with its public IP.

For example:

Before NAT:

Source IP = 172.168.1.5
Source Port = 5000

After NAT:

Source IP = 203.0.113.10
Source Port = 6001

The router also stores this information in its NAT translation table.

Example:

Private Address	Public Address
172.168.1.5:5000	203.0.113.10:6001
Step 3: Request goes to the Internet

The NAT router sends the translated packet to the external web server.

172.168.1.5:5000
        ↓
NAT Router
        ↓
203.0.113.10:6001
        ↓
Internet
        ↓
Web Server

The external server sees:

Source IP = 203.0.113.10

It does not see the employee's internal IP.

Step 4: Web server sends the response

The web server sends the response back to:

203.0.113.10:6001

The NAT router receives this response because 203.0.113.10 is its public IP.

Step 5: NAT router checks its NAT table

The router looks at the destination port:

203.0.113.10:6001

and finds:

203.0.113.10:6001
        ↓
172.168.1.5:5000

So the router knows that the response belongs to the employee's connection.

Step 6: Router translates the response

The NAT router changes the destination address:

Before translation:

Destination = 203.0.113.10:6001

to:

After translation:

Destination = 172.168.1.5:5000

Then it forwards the packet to the employee's computer.

Complete NAT Flow
        PRIVATE NETWORK                         PUBLIC INTERNET

+-------------------+
| Employee PC       |
| 172.168.1.5       |
+-------------------+
          |
          | Source: 172.168.1.5:5000
          ↓
+-------------------+
|    NAT Router     |
|                   |
| Private:          |
| 172.168.1.5       |
| Public:           |
| 203.0.113.10      |
+-------------------+
          |
          | Source: 203.0.113.10:6001
          ↓
       Internet
          |
          ↓
+-------------------+
|   Web Server      |
+-------------------+
          |
          | Response
          ↓
+-------------------+
|    NAT Router     |
|                   |
| NAT Table:        |
| 203.0.113.10:6001 |
|       ↓            |
| 172.168.1.5:5000  |
+-------------------+
          |
          ↓
+-------------------+
| Employee PC       |
| 172.168.1.5       |
+-------------------+
Key Point for Exam

NAT translates private IP addresses into a public IP address for outgoing communication and uses the NAT translation table to translate the returning response back to the correct internal device.

Important correction

The image/question appears to show 172.168.1.5. Note that 172.168.x.x is not a private IPv4 range. The private 172.x.x.x range is:

172.16.0.0 – 172.31.255.255

So, if your question intends a private IP, it should be something like:

172.18.1.5

or

192.168.1.5

rather than 172.168.1.5
```
# ICMPv4 — Internet Control Message Protocol Version 4

## What is ping & tracert ?

**ICMPv4 (Internet Control Message Protocol version 4)** is a **Network Layer protocol** used with IPv4 networks.
> **ICMPv4 is a Network Layer protocol used with IPv4 to report packet-delivery errors and perform network diagnostics.**
It is mainly used for:

* Error reporting
* Network diagnostics
* Control and informational messages

---

# Why is ICMPv4 Needed?

Suppose a PC sends an IPv4 packet to a server:

```text
PC ───────────> Router ───────────> Server
```

If the packet cannot reach the destination, the network device can use ICMPv4 to inform the sender about the problem.

```text
PC ── IPv4 Packet ──> Router ──X──> Server
                       │
                       │ ICMPv4 Error Message
                       ↓
PC <────────────────────────────
```

So, ICMPv4 helps devices **report problems related to IPv4 packet delivery**.

---

# Main Functions of ICMPv4

## 1. Error Reporting

ICMPv4 reports problems that occur during IPv4 packet delivery.

Common examples:

* **Destination Unreachable** → The destination cannot be reached.
* **Time Exceeded** → The packet's TTL has reached 0.
* **Parameter Problem** → There is a problem with the IPv4 packet header.
* **Redirect** → A better route may be available.

---

## 2. Network Diagnostics

ICMPv4 is commonly used to test network connectivity.

For example:

```bash
ping google.com
```

The `ping` command uses:

```text
ICMP Echo Request
ICMP Echo Reply
```

### Ping Process

```text
PC                         Server
 |                           |
 |---- ICMP Echo Request ---->|
 |                           |
 |<---- ICMP Echo Reply ------|
 |                           |
```

If the PC receives an Echo Reply, it indicates that the destination is reachable and responding to ICMP.

---

# 3. Traceroute / Tracert

ICMP messages are also involved in discovering the path between two devices.

### Windows

```bash
tracert google.com
```

### Linux

```bash
traceroute google.com
```

Example:

```text
PC
 ↓
Router 1
 ↓
Router 2
 ↓
Router 3
 ↓
Server
```

Traceroute uses the **TTL (Time To Live)** field and ICMP messages to identify intermediate routers.

---

<img width="859" height="410" alt="image" src="https://github.com/user-attachments/assets/c552fd79-f797-42f6-9370-be764c717245" />


# UDP — User Datagram Protocol

## What is UDP?

**UDP (User Datagram Protocol)** is a **Transport Layer protocol** used to send data between devices over a network **without establishing a connection or guaranteeing delivery**.

### Bangla Meaning

> **UDP হলো একটি Transport Layer protocol, যা network-এর মাধ্যমে device-এর মধ্যে আগে connection establish না করে data পাঠায় এবং data অবশ্যই পৌঁছাবে—এমন কোনো guarantee দেয় না।**

---

## Simple Definition

> **UDP = Connectionless + Fast + Low Overhead + No Delivery Guarantee**

---

## How UDP Works

UDP does not establish a connection before sending data.

```text
Sender                         Receiver
  |                               |
  |--------- UDP Data ----------->|
  |--------- UDP Data ----------->|
  |--------- UDP Data ----------->|
```

There is no connection establishment like TCP.

---

## Main Features of UDP

### 1. Connectionless

UDP does not establish a connection before sending data.

```text
No Connection
      ↓
 Send Data
      ↓
 Receiver
```

---

### 2. Fast

UDP has low overhead because it does not perform:

* Connection establishment
* Acknowledgment
* Retransmission
* Complex flow control

Therefore, UDP is generally faster than TCP.

---

### 3. No Delivery Guarantee

UDP does not guarantee that the data will reach the destination.

```text
Sender ─────> Network ───X───> Receiver
                         Packet Lost
```

If a packet is lost, UDP does not automatically retransmit it.

---

### 4. No Ordering Guarantee

UDP does not guarantee that packets will arrive in the same order in which they were sent.

```text
Sender:

Packet 1
Packet 2
Packet 3

        ↓

Receiver:

Packet 2
Packet 1
Packet 3
```

---

### 5. No Retransmission

If a UDP packet is lost, UDP itself does not send it again.

```text
Packet Lost
     ↓
UDP does not retransmit
```

---

# UDP Header

UDP has a simple header with **4 main fields**.

```text
  0               15 16              31
 +------------------+------------------+
 |   Source Port    | Destination Port |
 +------------------+------------------+
 |      Length      |     Checksum     |
 +------------------+------------------+
 |                Data                |
 +-------------------------------------+
```

| Field                | Purpose                              |
| -------------------- | ------------------------------------ |
| **Source Port**      | Identifies the sending application   |
| **Destination Port** | Identifies the receiving application |
| **Length**           | Total length of UDP header + data    |
| **Checksum**         | Used for error detection             |

### UDP Header Size

> **Minimum UDP header size = 8 bytes**

---

# Common Uses of UDP

UDP is useful when **speed and low latency** are more important than perfect reliability.

Common examples:

* DNS
* DHCP
* VoIP
* Online Gaming
* Live Streaming
* Video Conferencing
* TFTP

---

<img width="757" height="404" alt="image" src="https://github.com/user-attachments/assets/71a3dfca-c037-4f2e-a6df-89f58f1d16be" />

# TCP — Transmission Control Protocol

## What is TCP?

**TCP (Transmission Control Protocol)** is a **Transport Layer protocol** that provides **reliable, ordered, and error-checked delivery of data** between devices over a network.

### Bangla Meaning

> **TCP হলো একটি connection-oriented Transport Layer protocol, যা connection establish করে reliable, ordered এবং error-checkedভাবে data পাঠায়।**

### Simple Definition

> **TCP = Connection-Oriented + Reliable + Ordered + Error-Checked Data Delivery**

---

# Why is TCP Used?

When data is sent over a network, packets may be:

* Lost
* Duplicated
* Damaged
* Received out of order

TCP provides mechanisms to handle these problems.

```text
Sender
  │
  │ TCP
  ↓
Network
  │
  ↓
Receiver
```

---

# Main Features of TCP

## 1. Connection-Oriented

TCP sends data only after establishing a connection between the sender and receiver.

```text
Connection Establish
        ↓
     Send Data
        ↓
 Connection Close
```

---

## 2. Reliable Delivery
TCP নিশ্চিত করে যে data properly receiver-এর কাছে পৌঁছেছে।
TCP ensures reliable delivery using:

* Acknowledgments
* Sequence numbers
* Retransmission
* Checksum

```text
Sender                         Receiver
  |                               |
  |--------- Data --------------->|
  |<-------- ACK -----------------|
```

If a packet is lost, TCP can retransmit it.

```text
Sender ─── Packet 1 ───> Receiver
Sender ─── Packet 2 ───X
Sender ─── Packet 3 ───> Receiver

Packet 2 → Lost

        ↓

TCP retransmits Packet 2
```

---

## 3. Ordered Delivery

TCP ensures that data is delivered to the application in the correct order.

```text
Sender:

Packet 1
Packet 2
Packet 3

        ↓

Receiver:

Packet 1
Packet 2
Packet 3
```

TCP uses **Sequence Numbers** to maintain the correct order.

---

## 4. Error Detection

TCP uses a **checksum** to detect errors in transmitted data.

```text
Data
 ↓
TCP Checksum
 ↓
Receiver checks the data
```

If an error is detected, the affected data can be retransmitted.

---

## 5. Flow Control

TCP prevents a fast sender from overwhelming a slow receiver.

```text
Fast Sender
     ↓
 TCP Flow Control
     ↓
Slow Receiver
```

TCP uses the **Receive Window (Window Size)** for flow control.

---

## 6. Congestion Control

TCP controls the sending rate when the network becomes congested.

```text
Network Congestion
        ↓
TCP reduces sending rate
        ↓
Less Network Congestion
```

---

# TCP Three-Way Handshake

TCP uses a **Three-Way Handshake** to establish a connection.

```text
Client                         Server
  |                              |
  |----------- SYN ------------>|
  |                              |
  |<-------- SYN + ACK ----------|
  |                              |
  |----------- ACK ------------>|
  |                              |
  |     Connection Established   |
```

### Steps

### Step 1 — SYN

Client sends a **SYN** packet to request a connection.

```text
Client → Server : SYN
```

### Step 2 — SYN + ACK

Server accepts the request and responds with:

```text
Server → Client : SYN + ACK
```

### Step 3 — ACK

Client confirms the response:

```text
Client → Server : ACK
```

Now the TCP connection is established.

---

# TCP Connection Termination

TCP normally uses a **Four-Way Termination** to close a connection.

```text
Client                         Server
  |                              |
  |----------- FIN ------------>|
  |                              |
  |<---------- ACK -------------|
  |                              |
  |<---------- FIN -------------|
  |                              |
  |----------- ACK ------------>|
  |                              |
  |      Connection Closed       |
```

---

# TCP Header

TCP has a more complex header than UDP.

```text
  0                   15 16                  31
 +---------------------+---------------------+
 |     Source Port     |   Destination Port  |
 +---------------------+---------------------+
 |                Sequence Number            |
 +-------------------------------------------+
 |             Acknowledgment Number         |
 +-------------------------------------------+
 | Header | Flags |       Window Size        |
 +-------------------------------------------+
 |      Checksum      |    Urgent Pointer    |
 +-------------------------------------------+
 |              Options (Optional)           |
 +-------------------------------------------+
 |                   Data                    |
 +-------------------------------------------+
```

### Minimum TCP Header Size

> **Minimum TCP header size = 20 bytes**

---

# Important TCP Flags

| Flag    | Purpose                        |
| ------- | ------------------------------ |
| **SYN** | Establishes a connection       |
| **ACK** | Acknowledges received data     |
| **FIN** | Gracefully closes a connection |
| **RST** | Resets/terminates a connection |
| **PSH** | Pushes data to the application |
| **URG** | Indicates urgent data          |

---

# Common Uses of TCP

TCP is used when **reliable data delivery** is important.

Common examples:

* **HTTP**
* **HTTPS**
* **FTP**
* **SMTP**
* **IMAP**
* **SSH**

Example:

```text
Web Browser
     ↓
    TCP
     ↓
Web Server
```

---

# TCP vs UDP

| Feature            | TCP                           | UDP                    |
| ------------------ | ----------------------------- | ---------------------- |
| Full Form          | Transmission Control Protocol | User Datagram Protocol |
| Layer              | Transport Layer               | Transport Layer        |
| Connection         | Connection-oriented           | Connectionless         |
| Reliability        | Reliable                      | Not guaranteed         |
| Ordering           | Guaranteed                    | Not guaranteed         |
| Acknowledgment     | Yes                           | No                     |
| Retransmission     | Yes                           | No                     |
| Flow Control       | Yes                           | No                     |
| Congestion Control | Yes                           | No                     |
| Speed              | Generally slower              | Generally faster       |
| Minimum Header     | 20 bytes                      | 8 bytes                |
| Common Uses        | HTTP/HTTPS, FTP, SSH          | DNS, Gaming, VoIP      |

---

## File download from a website normally uses HTTP/HTTPS at the Application Layer and TCP at the Transport Layer.
<img width="734" height="393" alt="image" src="https://github.com/user-attachments/assets/6bade70c-97f3-4ae6-ad26-8d137c24c7aa" />
# TCP Three-Way Handshake

## What is TCP Three-Way Handshake?

**TCP Three-Way Handshake** is the process used by TCP to **establish a connection** between a client and a server before data transmission begins.

It uses **three messages**:

```text
SYN → SYN + ACK → ACK
```

### Simple Definition

> **TCP Three-Way Handshake is a three-step process used to establish a reliable TCP connection between two devices.**

---

# TCP Three-Way Handshake Process

```text
Client                                      Server
  |                                           |
  |------------- SYN ----------------------->|
  |                                           |
  |<------------ SYN + ACK ------------------|
  |                                           |
  |------------- ACK ----------------------->|
  |                                           |
  |       Connection Established              |
  |                                           |
  |<========== Data Transfer ===============>|
```
<img width="579" height="401" alt="image" src="https://github.com/user-attachments/assets/faeb83ae-c567-41c0-997c-dcab2d8776b1" />

---

## Step 1: SYN

The client sends a **SYN (Synchronize)** packet to the server.

```text
Client → Server : SYN
```

### Meaning

The client is saying:

> "I want to establish a TCP connection."

The client also sends an **initial sequence number**.

---

## Step 2: SYN + ACK

The server receives the SYN and responds with **SYN + ACK**.

```text
Server → Client : SYN + ACK
```

Here:

* **SYN** → Server is also synchronizing its sequence number.
* **ACK** → Server acknowledges the client's SYN.

### Meaning

The server is saying:

> "I received your request, and I am ready to establish the connection."

---

## Step 3: ACK

The client sends an **ACK (Acknowledgment)** back to the server.

```text
Client → Server : ACK
```

### Meaning

The client confirms:

> "I received your response."

Now the TCP connection is established.

```text
Connection Established
        ↓
Data Transfer Begins
```

---

<img width="833" height="418" alt="image" src="https://github.com/user-attachments/assets/c4ab1d4f-c8d9-4c24-a80b-4e148e6beb1c" />
<img width="742" height="401" alt="image" src="https://github.com/user-attachments/assets/7bdaf6f7-d40a-4412-b30f-430af0f06380" />
# FTP Control and Data Connection

**FTP (File Transfer Protocol)** is an Application Layer protocol used to transfer files between a client and a server. It uses **TCP**.

### 1. Control Connection

* Used to send **commands** and receive **responses**.
* Uses **TCP port 21**.
* Example: `USER`, `PASS`, `LIST`, `RETR`, `STOR`.

### 2. Data Connection

* Used to transfer **actual files and directory listing data**.
* Port depends on the FTP mode.

### Simple Diagram

```text
Client                         FTP Server
  |                                |
  |--- Control Connection -------->|  TCP 21
  |    Commands / Responses        |
  |                                |
  |<--- Data Connection ---------->|  File/Data
  |                                |
```

### Easy Way to Remember

> **Control = What should I do?**
> **Data = Here is the actual data!**

