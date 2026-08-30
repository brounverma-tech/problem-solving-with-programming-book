<div align="center">

# 🧠 Chapter 2: Computer Memory and Processors

### 🔵 Unit A — Computer Systems and Hardware Concepts

![Level](https://img.shields.io/badge/Level-Beginner-brightgreen?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-success?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Computer memory ko define kar sakenge.
- Memory hierarchy aur uske levels samajh सकेंगे.
- Processor aur CPU ke components explain kar सकेंगे.
- Registers aur cache memory ka role bata सकेंगे.
- Primary aur secondary memory mein difference kar सकेंगे.
- RAM aur ROM ke types samajh सकेंगे.
- Common secondary storage devices identify kar सकेंगे.
- Basic processor architecture aur instruction cycle explain kar सकेंगे.

---

# 2.1 Introduction to Computer Memory

## 2.1.1 Meaning of Memory

### 📘 English Definition

> Computer memory is the storage area in which data, instructions and processing results are kept either temporarily or permanently.

### 💬 Hinglish Explanation

Computer memory woh jagah hai jahan computer **data**, **instructions**, **programs** aur **results** ko store karta hai. Kuch memory temporary hoti hai aur power off hone par data lose kar deti hai. Kuch memory data ko permanently save rakhti hai.

## 2.1.2 Why Does a Computer Need Memory?

Computer ko memory ki zarurat hoti hai:

1. Input data store karne ke liye.
2. Program instructions rakhne ke liye.
3. Processing ke beech ke results store karne ke liye.
4. Final output save karne ke liye.
5. Operating system aur applications run karne ke liye.

## 2.1.3 Important Memory Terms

| Term | Pronunciation | Meaning |
|---|---|---|
| Memory | मेमोरी | Data aur instructions store karne ki jagah |
| Storage | स्टोरेज | Data ko save rakhne ki facility |
| Capacity | कैपेसिटी | Kitna data store ho sakta hai |
| Access Time | एक्सेस टाइम | Data tak pahunchne mein lagne wala time |
| Volatile | वॉलटाइल | Power off hone par data lose karne wali memory |
| Non-volatile | नॉन-वॉलटाइल | Power off hone par bhi data save rakhne wali memory |
| Read | रीड | Stored data ko access karna |
| Write | राइट | Memory mein data save karna |

---

# 2.2 Memory Units

## 2.2.1 Bit

**Bit** ka full form **Binary Digit** hai. Yeh computer memory ki smallest unit hai. Ek bit ki value `0` ya `1` ho sakti hai.

## 2.2.2 Nibble

**4 bits = 1 nibble**

## 2.2.3 Byte

**8 bits = 1 byte**

Usually ek character ko store karne ke liye approximately one byte use hota hai.

## 2.2.4 Larger Memory Units

| Unit | Relation |
|---|---:|
| 1 Bit | One binary digit |
| 1 Nibble | 4 bits |
| 1 Byte | 8 bits |
| 1 Kilobyte (KB) | 1024 bytes |
| 1 Megabyte (MB) | 1024 KB |
| 1 Gigabyte (GB) | 1024 MB |
| 1 Terabyte (TB) | 1024 GB |
| 1 Petabyte (PB) | 1024 TB |

> 💡 **Example:** 8 GB RAM ka traditional binary-based meaning approximately $8 × 1024$ MB hota hai.

---

# 2.3 Types of Computer Memory

## 2.3.1 Internal Memory

Internal memory computer ke processing system ke close hoti hai. CPU ise directly ya quickly access kar sakta hai.

**Examples:** Registers, cache, RAM and ROM.

## 2.3.2 External Memory

External memory long-term data storage ke liye use hoti hai.

**Examples:** HDD, SSD, optical disc, pen drive and memory card.

## 2.3.3 Volatile Memory

Power supply band hone par stored data lose ho jata hai.

**Examples:** RAM, most cache memory and registers.

## 2.3.4 Non-volatile Memory

Power supply band hone ke baad bhi data stored rehta hai.

**Examples:** ROM, SSD, HDD, pen drive and memory card.

---

# 2.4 Memory Hierarchy

## 2.4.1 Meaning of Memory Hierarchy

### 📘 English Definition

> Memory hierarchy is the arrangement of computer memory in different levels according to speed, cost, capacity and distance from the CPU.

### 💬 Hinglish Explanation

Computer ki sari memory same speed aur same cost ki nahi hoti. Fast memory costly aur small hoti hai, jabki slower memory cheaper aur large hoti hai. Inhe ek क्रम mein arrange karna memory hierarchy kehlata hai.

## 2.4.2 Levels of Memory Hierarchy

```text
Fastest, Smallest and Most Expensive
                 │
             Registers
                 │
               Cache
          L1 → L2 → L3
                 │
        Primary Memory
              RAM/ROM
                 │
       Secondary Storage
             SSD/HDD
                 │
     Backup/Archival Storage
     Optical Disc/Magnetic Tape
                 │
Slowest, Largest and Least Expensive per Bit
```

## 2.4.3 Memory Hierarchy Comparison

| Memory Level | Speed | Capacity | Cost per Bit | CPU Distance |
|---|---|---|---|---|
| Registers | Fastest | Smallest | Highest | Inside CPU |
| Cache | Very fast | Very small | Very high | Inside/near CPU |
| RAM | Fast | Medium | Medium | Main board |
| SSD/HDD | Slower | Large | Low | Secondary storage |
| Tape/Archive | Slowest | Very large | Lowest | External/archive |

## 2.4.4 Principle of Locality

CPU frequently used data aur nearby instructions ko baar-baar access karta hai. Is behavior ko **locality of reference** kehte hain.

### 2.4.4.1 Temporal Locality

Jo data abhi use hua hai, uske jaldi dobara use hone ki possibility hoti hai.

### 2.4.4.2 Spatial Locality

Jis memory location ka data use hua hai, uske nearby data ke use hone ki possibility hoti hai.

Cache memory isi principle ka benefit leti hai.

---

# 2.5 Processor

## 2.5.1 Meaning of Processor

### 📘 English Definition

> A processor is an electronic component that interprets and executes program instructions and controls data processing operations.

### 💬 Hinglish Explanation

Processor instructions ko samajhta aur execute karta hai. Personal computers mein central processor ko generally **CPU** kaha jata hai. CPU calculations, decisions aur system coordination perform karta hai.

## 2.5.2 Central Processing Unit

CPU ka full form **Central Processing Unit** hai. Isse computer ka **brain** kaha jata hai.

CPU ke main components:

1. Arithmetic Logic Unit
2. Control Unit
3. Registers
4. Internal buses and clock

## 2.5.3 Arithmetic Logic Unit

ALU ka full form **Arithmetic Logic Unit** hai.

### 2.5.3.1 Arithmetic Operations

- Addition
- Subtraction
- Multiplication
- Division

### 2.5.3.2 Logical Operations

- Greater than
- Less than
- Equal to
- AND
- OR
- NOT

## 2.5.4 Control Unit

Control Unit instructions ko decode karti hai aur different components ko control signals bhejti hai.

Main functions:

- Memory se instruction fetch karna.
- Instruction ko decode karna.
- Required components ko signal dena.
- Data flow coordinate karna.
- Execution order control karna.

## 2.5.5 Clock

CPU clock operations ki timing synchronize karta hai. Clock speed ko generally **Hertz**, **Megahertz** ya **Gigahertz** mein express kiya jata hai.

| Unit | Meaning |
|---|---:|
| 1 Hz | 1 cycle per second |
| 1 MHz | 1 million cycles per second |
| 1 GHz | 1 billion cycles per second |

> ⚠️ Higher clock speed akela overall performance decide nahi karta. Core count, architecture, cache aur workload bhi important hain.

## 2.5.6 Processor Cores

Core CPU ka individual processing unit hota hai.

- Single-core: One processing core
- Dual-core: Two cores
- Quad-core: Four cores
- Octa-core: Eight cores

Multiple cores parallel tasks handle karke performance improve kar sakte hain.

---

# 2.6 Registers

## 2.6.1 Meaning of Register

> A register is a very small and extremely fast storage location inside the CPU.

Registers currently processing data, instructions aur addresses ko temporarily hold karte hain.

## 2.6.2 Types of Registers

### 2.6.2.1 Accumulator

Arithmetic aur logical operations ke intermediate results store karta hai.

### 2.6.2.2 Program Counter

Next instruction ka address hold karta hai.

### 2.6.2.3 Instruction Register

Currently execute ho rahi instruction ko hold karta hai.

### 2.6.2.4 Memory Address Register

Jis memory location ko access karna hai, uska address hold karta hai.

### 2.6.2.5 Memory Data Register

Memory se aane ya memory mein jane wala data temporarily hold karta hai.

### 2.6.2.6 General-Purpose Registers

Temporary data aur operation values store karte hain.

### 2.6.2.7 Status or Flag Register

Operation ke result ki condition store karta hai, jaise zero, carry, sign aur overflow.

## 2.6.3 Common Register Abbreviations

| Register | Full Form | Main Work |
|---|---|---|
| ACC | Accumulator | Intermediate result |
| PC | Program Counter | Next instruction address |
| IR | Instruction Register | Current instruction |
| MAR | Memory Address Register | Memory address |
| MDR | Memory Data Register | Transferred data |

---

# 2.7 Cache Memory

## 2.7.1 Meaning of Cache Memory

### 📘 English Definition

> Cache memory is a small, high-speed memory that stores frequently used data and instructions so that the CPU can access them faster.

### 💬 Hinglish Explanation

CPU bahut fast hota hai, lekin RAM comparatively slow hoti hai. Cache CPU aur RAM ke beech speed gap ko reduce karti hai. Frequently used data cache mein mil jaye to CPU ko RAM ka wait nahi karna padta.

## 2.7.2 Cache Hit and Cache Miss

### 2.7.2.1 Cache Hit

Required data cache mein mil jata hai.

### 2.7.2.2 Cache Miss

Required data cache mein nahi milta aur RAM ya lower memory level se lana padta hai.

## 2.7.3 Levels of Cache

| Level | Location | Speed | Typical Characteristic |
|---|---|---|---|
| L1 | Each CPU core ke very close | Fastest | Smallest |
| L2 | Core ke close | Very fast | L1 se larger |
| L3 | Cores ke beech shared ho sakti hai | Fast | L1/L2 se larger |

## 2.7.4 Advantages of Cache

- CPU waiting time reduce karti hai.
- Frequently used data fast provide karti hai.
- Overall system performance improve karti hai.
- RAM access frequency reduce kar sakti hai.

---

# 2.8 Primary Memory

## 2.8.1 Meaning of Primary Memory

Primary memory ko **main memory** bhi kaha jata hai. CPU active programs aur data ke liye ise directly access karta hai.

Main types:

1. RAM
2. ROM

## 2.8.2 Random Access Memory

RAM ka full form **Random Access Memory** hai.

### 2.8.2.1 Features of RAM

- Volatile memory hai.
- Read aur write dono operations support karti hai.
- Running programs aur current data store karti hai.
- Power off hone par data lose ho jata hai.

### 2.8.2.2 Static RAM

SRAM ka full form **Static Random Access Memory** hai.

- Very fast hoti hai.
- Expensive hoti hai.
- Refreshing ki zarurat nahi hoti.
- Cache memory mein commonly use hoti hai.

### 2.8.2.3 Dynamic RAM

DRAM ka full form **Dynamic Random Access Memory** hai.

- SRAM se slower hoti hai.
- Cheaper aur higher capacity hoti hai.
- Data maintain karne ke liye periodic refreshing chahiye.
- Main system RAM mein commonly use hoti hai.

### 2.8.2.4 SRAM and DRAM Difference

| Basis | SRAM | DRAM |
|---|---|---|
| Full Form | Static RAM | Dynamic RAM |
| Speed | Faster | Slower |
| Cost | Expensive | Cheaper |
| Refresh | Not required | Required |
| Common Use | Cache | Main memory |

## 2.8.3 Read-Only Memory

ROM ka full form **Read-Only Memory** hai.

### 2.8.3.1 Features of ROM

- Non-volatile memory hai.
- Permanent instructions store karti hai.
- Power off hone par data retain hota hai.
- Firmware aur startup instructions ke liye use hoti hai.

### 2.8.3.2 PROM

**Programmable Read-Only Memory** ko user ek baar program kar sakta hai.

### 2.8.3.3 EPROM

**Erasable Programmable Read-Only Memory** ko ultraviolet light se erase karke reprogram kiya ja sakta hai.

### 2.8.3.4 EEPROM

**Electrically Erasable Programmable Read-Only Memory** ko electrically erase aur reprogram kiya ja sakta hai.

### 2.8.3.5 RAM and ROM Difference

| Basis | RAM | ROM |
|---|---|---|
| Nature | Volatile | Non-volatile |
| Operation | Read and write | Mainly read |
| Use | Active programs/data | Firmware/startup instructions |
| Data after power off | Lost | Retained |
| Speed | Generally faster | Generally slower |

---

# 2.9 Secondary Storage

## 2.9.1 Meaning of Secondary Storage

> Secondary storage is non-volatile storage used to keep data and programs for long-term use.

Secondary storage ki capacity primary memory se generally larger aur cost per unit lower hoti hai.

## 2.9.2 Characteristics

- Non-volatile
- Large capacity
- Long-term storage
- Primary memory se slower
- Portable ya fixed ho sakti hai
- Backup ke liye useful

---

# 2.10 Magnetic Storage Devices

## 2.10.1 Magnetic Tape

Magnetic tape plastic strip par magnetic coating use karke data store karti hai.

### 2.10.1.1 Features

- Sequential access
- High backup capacity
- Low cost per unit
- Archival aur backup use

## 2.10.2 Floppy Disk

Floppy disk ek removable magnetic storage medium thi.

### 2.10.2.1 Features

- Low capacity
- Portable
- Slow
- Aaj largely obsolete hai

## 2.10.3 Hard Disk Drive

HDD rotating magnetic platters par data store karta hai.

### 2.10.3.1 Main Parts

- Platters
- Read/write head
- Spindle motor
- Controller

### 2.10.3.2 Advantages

- Large capacity
- Low cost per GB
- Long-term storage

### 2.10.3.3 Limitations

- Moving parts ke कारण physical damage ka risk.
- SSD se slower.
- Noise aur power use comparatively higher ho sakte hain.

---

# 2.11 Optical Storage Devices

## 2.11.1 Meaning

Optical discs laser light ki help se data read/write karte hain.

## 2.11.2 Compact Disc

CD ki common capacity approximately **700 MB** hoti hai.

## 2.11.3 Digital Versatile Disc

DVD commonly **4.7 GB** ya usse higher capacity variants mein milti hai.

## 2.11.4 Blu-ray Disc

Blu-ray higher-capacity optical storage hai, commonly HD video aur large data ke liye use hui.

## 2.11.5 Optical Disc Types

- ROM: Factory-written, read-only
- R: Ek baar record
- RW/RE: Erase aur rewrite

---

# 2.12 Solid-State Storage Devices

## 2.12.1 Solid-State Drive

SSD flash memory use karta hai aur ismein mechanical moving parts nahi hote.

### 2.12.1.1 Advantages

- Fast data access
- Silent operation
- Lower power consumption
- Better shock resistance
- Fast boot and application loading

### 2.12.1.2 Limitations

- Cost per GB HDD se higher ho sakti hai.
- Flash cells ki limited write endurance hoti hai.

## 2.12.2 USB Flash Drive

USB port ke through connect hone wali portable flash storage device.

## 2.12.3 Memory Card

Small portable flash storage, commonly cameras, phones aur embedded devices mein use hoti hai.

**Examples:** SD, microSD.

## 2.12.4 HDD and SSD Difference

| Basis | HDD | SSD |
|---|---|---|
| Technology | Magnetic platters | Flash memory |
| Moving Parts | Present | Absent |
| Speed | Slower | Faster |
| Noise | Ho sakta hai | Silent |
| Shock Resistance | Lower | Higher |
| Cost per GB | Usually lower | Usually higher |

---

# 2.13 Mass Storage Devices

## 2.13.1 Meaning

Mass storage large amounts of data ko long-term store karne wali technologies ko describe karta hai.

## 2.13.2 Examples

- Internal and external HDD
- SSD
- Storage arrays
- Network-attached storage
- Magnetic tape libraries
- Cloud-backed storage systems

## 2.13.3 Uses

- Organizational data
- Backups
- Multimedia collections
- Server storage
- Research datasets
- Archives

---

# 2.14 Basic Processor Architecture

## 2.14.1 Main Components

A basic processor architecture mein:

1. ALU
2. Control Unit
3. Registers
4. Cache
5. System buses
6. Clock

## 2.14.2 System Buses

Bus parallel communication paths ka set hota hai jo computer components ke beech signals carry karta hai.

### 2.14.2.1 Data Bus

Actual data transfer karta hai.

### 2.14.2.2 Address Bus

Memory ya I/O location ka address carry karta hai.

### 2.14.2.3 Control Bus

Read, write, clock aur interrupt jaise control signals carry karta hai.

## 2.14.3 Instruction Cycle

CPU instructions ko ek repeating cycle mein execute karta hai.

### 2.14.3.1 Fetch

Control Unit memory se next instruction fetch karti hai.

### 2.14.3.2 Decode

Instruction ka meaning aur required operation identify hota hai.

### 2.14.3.3 Execute

ALU ya required unit operation perform karti hai.

### 2.14.3.4 Store

Result register ya memory mein store hota hai.

```text
Fetch → Decode → Execute → Store → Next Instruction
```

## 2.14.4 Simple Example

Instruction: Do numbers ko add karna.

1. Program Counter next instruction ka address deta hai.
2. Instruction memory se fetch hoti hai.
3. Instruction Register instruction hold karta hai.
4. Control Unit operation decode karti hai.
5. Required values registers mein load hoti hain.
6. ALU addition perform karta hai.
7. Result accumulator/register ya memory mein store hota hai.

---

# 2.15 Important Differences

## 2.15.1 Primary Memory vs Secondary Memory

| Basis | Primary Memory | Secondary Memory |
|---|---|---|
| CPU Access | Direct/fast | I/O system ke through |
| Speed | Faster | Slower |
| Capacity | Smaller | Larger |
| Cost per Unit | Higher | Lower |
| Use | Active processing | Long-term storage |
| Examples | RAM, ROM | HDD, SSD, pen drive |

## 2.15.2 Volatile vs Non-volatile Memory

| Volatile Memory | Non-volatile Memory |
|---|---|
| Power off par data lost | Power off par data retained |
| Temporary working storage | Long-term/permanent storage |
| RAM, cache, registers | ROM, HDD, SSD |

## 2.15.3 Register vs Cache vs RAM

| Basis | Register | Cache | RAM |
|---|---|---|---|
| Location | CPU ke andar | CPU ke andar/near | Motherboard |
| Speed | Fastest | Very fast | Fast |
| Capacity | Smallest | Very small | Larger |
| Purpose | Current operation | Frequent data | Active programs |

---

# 2.16 Chapter Summary

Computer memory stores data, instructions and processing results temporarily or permanently. Memory hierarchy arranges registers, cache, primary memory and secondary storage according to speed, capacity, cost and distance from the CPU. The processor executes instructions with the help of the ALU, Control Unit, registers, cache, buses and clock. Registers are the fastest small storage locations, while cache stores frequently used data to reduce CPU waiting time. Primary memory includes volatile RAM and non-volatile ROM, whereas secondary storage provides large and permanent storage through HDDs, SSDs, optical discs, magnetic tapes, USB drives and memory cards. A processor completes each instruction through the fetch, decode, execute and store cycle.

---

# 2.17 Quick Revision

- Bit computer memory ki smallest unit hai.
- 8 bits milkar 1 byte banate hain.
- Registers memory hierarchy mein fastest hote hain.
- Cache CPU aur RAM ke speed gap ko reduce karti hai.
- RAM volatile aur ROM non-volatile hoti hai.
- SRAM cache aur DRAM main memory mein commonly use hoti hai.
- HDD magnetic storage aur SSD flash storage use karta hai.
- CPU ke main parts ALU, Control Unit aur registers hain.
- Data, address aur control buses components ko connect karte hain.
- Instruction cycle: Fetch, Decode, Execute and Store.

---

# 2.18 Important Abbreviations

| Abbreviation | Full Form |
|---|---|
| CPU | Central Processing Unit |
| ALU | Arithmetic Logic Unit |
| CU | Control Unit |
| RAM | Random Access Memory |
| ROM | Read-Only Memory |
| SRAM | Static Random Access Memory |
| DRAM | Dynamic Random Access Memory |
| PROM | Programmable Read-Only Memory |
| EPROM | Erasable Programmable Read-Only Memory |
| EEPROM | Electrically Erasable Programmable Read-Only Memory |
| HDD | Hard Disk Drive |
| SSD | Solid-State Drive |
| MAR | Memory Address Register |
| MDR | Memory Data Register |
| IR | Instruction Register |
| PC | Program Counter |

---

# 2.19 Multiple-Choice Questions

### 1. Computer memory ki smallest unit kya hai?

A. Byte  
B. Bit  
C. KB  
D. Nibble  

**✅ Answer:** B

### 2. CPU ke andar fastest memory kaunsi hai?

A. HDD  
B. RAM  
C. Register  
D. Optical disc  

**✅ Answer:** C

### 3. Kaunsi memory volatile hai?

A. ROM  
B. SSD  
C. RAM  
D. DVD  

**✅ Answer:** C

### 4. Cache memory ka main purpose kya hai?

A. Permanent backup  
B. CPU ko frequently used data fast dena  
C. Documents print karna  
D. Internet connect karna  

**✅ Answer:** B

### 5. DRAM commonly kahan use hoti hai?

A. Main memory  
B. Optical disc  
C. Magnetic tape  
D. Printer  

**✅ Answer:** A

### 6. Moving parts kis device mein hote hain?

A. SSD  
B. HDD  
C. Register  
D. Cache  

**✅ Answer:** B

### 7. Next instruction ka address kaunsa register rakhta hai?

A. IR  
B. MDR  
C. PC  
D. ACC  

**✅ Answer:** C

### 8. Instruction cycle ka correct order kya hai?

A. Execute–Fetch–Store–Decode  
B. Fetch–Decode–Execute–Store  
C. Store–Fetch–Decode–Execute  
D. Decode–Store–Fetch–Execute  

**✅ Answer:** B

### 9. Address bus kya carry karti hai?

A. Sound  
B. Memory location address  
C. Printed output  
D. Only instructions  

**✅ Answer:** B

### 10. Kaunsi storage non-volatile hai?

A. Register  
B. Cache  
C. RAM  
D. SSD  

**✅ Answer:** D

---

# 2.20 Short-Answer Questions

1. Computer memory ko define kijiye.
2. Bit, nibble aur byte kya hain?
3. Memory hierarchy kya hai?
4. Volatile aur non-volatile memory explain kijiye.
5. Processor kya hai?
6. ALU ka kya function hai?
7. Control Unit ka role kya hai?
8. Register kya hai?
9. Cache hit aur cache miss kya hain?
10. RAM aur ROM mein difference likhiye.
11. SRAM aur DRAM mein difference likhiye.
12. HDD aur SSD mein difference likhiye.
13. Data bus, address bus aur control bus kya hain?
14. Instruction cycle ke stages likhiye.

---

# 2.21 Long-Answer and Exam Questions

1. Memory hierarchy ko diagram aur comparison ke saath explain kijiye.
2. CPU ke main components aur unke functions explain kijiye.
3. Different CPU registers ko detail mein samjhaiye.
4. Cache memory aur uske levels explain kijiye.
5. Primary memory ke types ko detail mein describe kijiye.
6. Secondary storage devices ko examples ke saath explain kijiye.
7. Magnetic, optical aur solid-state storage compare kijiye.
8. Basic processor architecture ko diagram ke saath samjhaiye.
9. Fetch–decode–execute–store cycle ko example ke saath explain kijiye.
10. Primary aur secondary memory mein detailed difference likhiye.

---

# 2.22 Practical Exercises

1. Apne computer ya phone ki RAM aur storage capacity note kijiye.
2. KB se GB tak memory units ka chart banaiye.
3. Memory hierarchy ka labeled diagram draw kijiye.
4. HDD aur SSD ke five differences likhiye.
5. CPU instruction cycle ka flowchart banaiye.
6. Kisi online computer specification mein processor cores, clock speed aur cache identify kijiye.

---

# 2.23 Viva Questions

1. Bit kya hai?
2. Ek byte mein kitne bits hote hain?
3. CPU ke sabse close memory kaunsi hai?
4. Cache RAM se fast kyun hoti hai?
5. RAM volatile kyun kehlati hai?
6. ROM ka use kya hai?
7. SRAM kahan use hoti hai?
8. Program Counter kya store karta hai?
9. HDD aur SSD mein kaunsa faster hai?
10. Fetch ke baad instruction-cycle ka next step kya hai?

---

# 2.24 Answers to Selected Viva Questions

1. Bit binary digit hai, jiski value 0 ya 1 hoti hai.
2. Ek byte mein 8 bits hote hain.
3. Registers CPU ke andar aur uske sabse close hote hain.
4. Cache smaller, high-speed memory hoti hai aur frequently used data hold karti hai.
5. Power off hone par RAM ka data lose ho jata hai.
6. ROM firmware aur startup instructions store karti hai.
7. SRAM commonly cache memory mein use hoti hai.
8. Program Counter next instruction ka address store karta hai.
9. SSD generally HDD se faster hota hai.
10. Fetch ke baad Decode step aata hai.

---

<div align="center">

## ✅ Chapter 2 Complete

[⬅️ Previous Chapter](chapter-01-introduction-to-computers.md) · [📚 Book Home](../README.md) · **Next: Input and Output Devices ➡️**

</div>
