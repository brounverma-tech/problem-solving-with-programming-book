<div align="center">

# 🧩 Chapter 4: Computer Software

### 🟢 Unit B — Computer Software and Computer Codes

![Level](https://img.shields.io/badge/Level-Beginner-brightgreen?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-success?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Software ko define kar सकेंगे.
- Hardware aur software mein difference samajh सकेंगे.
- Software ki main categories identify kar सकेंगे.
- System software aur application software explain kar सकेंगे.
- Operating system, drivers, utilities aur translators ka role samajh सकेंगे.
- General-purpose aur customized applications mein difference kar सकेंगे.
- Firmware aur middleware ko examples ke saath explain kar सकेंगे.
- Different software licenses aur installation concepts samajh सकेंगे.

---

## 4.1 Introduction to Computer Software

### 4.1.1 Meaning of Software

#### 📘 English Definition

> Computer software is a collection of programs, procedures and related data that instructs a computer to perform specific tasks.

#### 💬 Hinglish Explanation

Software instructions aur programs ka set hota hai jo computer hardware ko batata hai ki **kya kaam karna hai aur kaise karna hai**. Software ko physically touch nahi kiya ja sakta, lekin screen par uske functions aur results dekhe ja sakte hain.

**Examples:** Windows, Linux, Microsoft Word, web browser, media player aur mobile apps.

#### Program

> A program is an ordered set of instructions written to perform a particular task.

**Example:** Do numbers ka sum calculate karne wala C++ program.

### 4.1.2 Relationship Between Hardware and Software

```text
User → Application Software → System Software → Hardware
                                         ↓
                                      Output
```

- Hardware physical components provide karta hai.
- Software hardware ko instructions deta hai.
- Dono ek doosre ke bina useful computer system nahi bana sakte.

### 4.1.3 Hardware and Software Difference

| Basis | Hardware | Software |
|---|---|---|
| Nature | Physical components | Programs and instructions |
| Touch | Touch kiya ja sakta hai | Touch nahi kiya ja sakta |
| Creation | Manufactured | Developed/programmed |
| Damage | Physically damage ho sakta hai | Corrupt, delete ya infect ho sakta hai |
| Examples | CPU, keyboard, monitor | Windows, browser, Word |

### 4.1.4 Important Terms

| Term | Pronunciation | Meaning |
|---|---|---|
| Software | सॉफ्टवेयर | Programs aur instructions ka collection |
| Program | प्रोग्राम | Task perform karne wali instructions |
| Procedure | प्रोसीजर | Task karne ka defined method |
| Installation | इंस्टॉलेशन | Software ko system par setup karna |
| Configuration | कॉन्फ़िगरेशन | Software settings ko requirements ke अनुसार set karna |
| Update | अपडेट | Software mein improvements/fixes add karna |
| License | लाइसेंस | Software use karne ki legal permission |
| Compatibility | कम्पैटिबिलिटी | Software ka system ke saath correctly work karna |

---

## 4.2 Classification of Computer Software

### 4.2.1 Main Categories

Computer software ko broadly classify kiya jata hai:

1. System Software
2. Application Software

Related specialized categories:

3. Programming Software
4. Firmware
5. Middleware

### 4.2.2 Classification Diagram

```text
Computer Software
│
├── System Software
│   ├── Operating System
│   ├── Device Drivers
│   ├── Language Translators
│   └── Utility Programs
│
├── Application Software
│   ├── General-Purpose
│   ├── Special-Purpose
│   └── Customized Software
│
├── Programming Software
├── Firmware
└── Middleware
```

---

## 4.3 System Software

### 4.3.1 Meaning of System Software

#### 📘 English Definition

> System software is software designed to manage computer hardware and provide a platform for application software.

#### 💬 Hinglish Explanation

System software computer ke hardware ko manage karta hai aur applications ko run karne ke liye environment provide karta hai. Yeh user aur hardware ke beech bridge ki tarah kaam karta hai.

### 4.3.2 Main Functions

- Hardware resources manage karna
- Memory manage karna
- Files aur storage control karna
- Input/output devices handle karna
- Applications ko platform provide karna
- Security aur user accounts manage karna
- System errors detect aur handle karna

### 4.3.3 Types of System Software

- Operating systems
- Device drivers
- Language translators
- Utility software

---

## 4.4 Operating System

### 4.4.1 Meaning of Operating System

> An operating system is system software that manages computer resources and acts as an interface between the user, applications and hardware.

**Examples:** Windows, Linux, macOS, Android and iOS.

### 4.4.2 Functions of Operating System

#### 4.4.2.1 Process Management

Running programs aur CPU time ko manage karta hai.

#### 4.4.2.2 Memory Management

RAM ko programs ke beech allocate aur deallocate karta hai.

#### 4.4.2.3 File Management

Files aur folders create, organize, access aur protect karta hai.

#### 4.4.2.4 Device Management

Keyboard, printer, storage aur other devices ko drivers ke through control karta hai.

#### 4.4.2.5 User Interface

User ko computer interact karne ke liye interface deta hai.

#### 4.4.2.6 Security Management

Authentication, permissions aur access control provide karta hai.

#### 4.4.2.7 Error Handling

Hardware aur software errors detect karke response provide karta hai.

### 4.4.3 Types of User Interface

#### 4.4.3.1 Command-Line Interface

User text commands enter karta hai.

**Examples:** Bash shell, Command Prompt.

#### 4.4.3.2 Graphical User Interface

Windows, icons, menus aur pointer use karta hai.

**Examples:** Windows desktop, Android interface.

### 4.4.4 Types of Operating Systems

#### 4.4.4.1 Single-User Operating System

Ek time par one primary user ko support karta hai.

#### 4.4.4.2 Multi-User Operating System

Multiple users ko resources access karne deta hai.

#### 4.4.4.3 Multitasking Operating System

Ek time par multiple programs run karta hai.

#### 4.4.4.4 Real-Time Operating System

Strict time limit ke andar response provide karta hai.

**Applications:** Medical devices, industrial control and robotics.

#### 4.4.4.5 Network Operating System

Network resources aur connected computers manage karta hai.

#### 4.4.4.6 Mobile Operating System

Smartphones aur tablets ke liye optimized hota hai.

**Examples:** Android and iOS.

---

## 4.5 Device Drivers

### 4.5.1 Meaning

> A device driver is system software that enables the operating system to communicate with a hardware device.

#### 💬 Hinglish Explanation

Har hardware device ka working method different ho sakta hai. Driver operating system ke general commands ko device-specific instructions mein convert karta hai.

#### Examples

- Printer driver
- Graphics driver
- Audio driver
- Network adapter driver
- Scanner driver
- Webcam driver

#### Working

```text
Application → Operating System → Device Driver → Hardware
```

### 4.5.2 Why Drivers Are Important

- Device ko recognize karne ke liye
- Device ke complete features use karne ke liye
- Performance aur compatibility improve karne ke liye
- Hardware errors fix karne ke liye

---

## 4.6 Language Translators

### 4.6.1 Meaning

Language translator source code ko machine-understandable code mein convert karta hai.

### 4.6.2 Assembler

Assembly-language program ko machine code mein translate karta hai.

### 4.6.3 Compiler

Complete source program ko ek unit ke roop mein machine/object code mein translate karta hai.

#### 4.6.3.1 Features

- Complete program compile karta hai.
- Errors compilation ke baad list ho sakte hain.
- Compiled program fast execute hota hai.
- Object/executable code generate kar sakta hai.

### 4.6.4 Interpreter

Program ko generally instruction-by-instruction translate aur execute karta hai.

#### 4.6.4.1 Features

- Line-by-line execution.
- Error milte hi execution stop ho sakta hai.
- Testing aur debugging easy hoti hai.
- Separate machine-code executable zaroori nahi.

### 4.6.5 Compiler and Interpreter Difference

| Basis | Compiler | Interpreter |
|---|---|---|
| Translation | Whole program | Instruction by instruction |
| Error Reporting | Compilation ke baad | Error wali instruction par |
| Execution | Compiled output faster | Usually slower |
| Output File | Object/executable bana sakta hai | Usually separate executable nahi |
| Examples | C, C++ implementations | Python/JavaScript implementations often interpreted or hybrid |

> 💡 Modern language systems compiler aur interpreter techniques ko combine bhi kar sakte hain.

---

## 4.7 Utility Software

### 4.7.1 Meaning

> Utility software helps maintain, protect, analyze and optimize a computer system.

### 4.7.2 Types of Utilities

#### 4.7.2.1 Antivirus

Malware detect, block aur remove karta hai.

#### 4.7.2.2 Backup Utility

Important data ki duplicate copy create aur restore karta hai.

#### 4.7.2.3 Disk Cleanup

Unnecessary temporary files remove karke storage free karta hai.

#### 4.7.2.4 File Compression

Files ka size reduce karta hai.

**Examples:** ZIP and 7z tools.

#### 4.7.2.5 Disk Management

Partitions create, format aur manage karta hai.

#### 4.7.2.6 Firewall

Network traffic monitor aur control karke unauthorized access reduce karta hai.

#### 4.7.2.7 File Manager

Files aur folders browse, copy, move, rename aur delete karne deta hai.

#### 4.7.2.8 System Monitoring Tool

CPU, memory, disk aur network usage show karta hai.

---

## 4.8 Application Software

### 4.8.1 Meaning of Application Software

#### 📘 English Definition

> Application software is designed to help users perform specific personal, educational or business tasks.

#### 💬 Hinglish Explanation

Application software directly user ke kaam ke liye banaya jata hai, jaise document banana, calculation karna, web browse karna ya photo edit karna.

### 4.8.2 Features

- User-oriented hota hai.
- Specific tasks solve karta hai.
- Operating system ke platform par run karta hai.
- Free, paid, web-based ya mobile form mein available ho sakta hai.

### 4.8.3 General-Purpose Application Software

Common tasks ke liye large number of users use kar sakte hain.

#### 4.8.3.1 Word Processor

Documents create aur edit karta hai.

**Examples:** Microsoft Word, LibreOffice Writer.

#### 4.8.3.2 Spreadsheet

Tabular data, formulas, calculations aur charts handle karta hai.

**Examples:** Microsoft Excel, LibreOffice Calc.

#### 4.8.3.3 Presentation Software

Slides create aur present karta hai.

**Examples:** Microsoft PowerPoint, LibreOffice Impress.

#### 4.8.3.4 Database Software

Structured data store, organize aur retrieve karta hai.

#### 4.8.3.5 Web Browser

Web pages aur web applications access karta hai.

**Examples:** Chrome, Firefox, Edge.

#### 4.8.3.6 Media Player

Audio aur video files play karta hai.

#### 4.8.3.7 Graphics Software

Images, drawings aur designs create/edit karta hai.

### 4.8.4 Special-Purpose Application Software

Specific task ya domain ke liye design hota hai.

**Examples:**

- Payroll system
- Billing software
- Railway reservation system
- Hospital management system
- Banking software
- School management system
- Inventory system

### 4.8.5 Customized Software

Particular organization ya user ki unique requirements ke according develop hota hai.

**Example:** Kisi company ka custom employee-management portal.

### 4.8.6 General-Purpose and Customized Software Difference

| Basis | General-Purpose | Customized |
|---|---|---|
| Users | Many users | Specific user/organization |
| Requirements | Common needs | Unique needs |
| Cost | Usually lower | Usually higher |
| Development Time | Ready-made | Development required |
| Examples | Word processor | Custom hospital system |

---

## 4.9 Programming Software

### 4.9.1 Meaning

Programming software developers ko programs create, test, debug aur maintain karne mein help karta hai.

### 4.9.2 Source Code Editor

Program code write aur edit karne ke liye.

### 4.9.3 Integrated Development Environment

IDE editor, compiler/interpreter, debugger aur project tools ko ek environment mein combine karta hai.

**Examples:** Visual Studio, Code::Blocks and IntelliJ IDEA.

### 4.9.4 Debugger

Program ko step-by-step inspect karke errors locate karne mein help karta hai.

### 4.9.5 Build Tools

Source code ko compile, link aur package karne ki process automate karte hain.

### 4.9.6 Version-Control Tools

Code changes track aur collaboration manage karte hain.

**Example:** Git.

---

## 4.10 Firmware

### 4.10.1 Meaning of Firmware

#### 📘 English Definition

> Firmware is specialized software stored in non-volatile memory that provides low-level control for a hardware device.

#### 💬 Hinglish Explanation

Firmware hardware ke andar ya uske close permanently stored software hota hai. Yeh device ko basic level par control aur start karta hai.

### 4.10.2 Characteristics

- ROM, EEPROM ya flash memory mein stored.
- Hardware-specific hota hai.
- Power off hone par retained rehta hai.
- User applications se lower level par work karta hai.
- Manufacturer updates provide kar sakta hai.

#### Examples

- Computer BIOS/UEFI
- Router firmware
- Printer firmware
- Camera firmware
- Smart TV firmware
- Embedded controller firmware

### 4.10.3 Firmware Update

Firmware update bugs fix, security improve ya new features add kar sakta hai.

> ⚠️ Firmware update interrupt ya incorrect file hone par device malfunction ho sakta hai. Official instructions follow karni chahiye.

---

## 4.11 Middleware

### 4.11.1 Meaning of Middleware

#### 📘 English Definition

> Middleware is software that connects different applications, services or system components and enables them to communicate and exchange data.

#### 💬 Hinglish Explanation

Middleware do software systems ke beech **middle layer** ki tarah kaam karta hai. Yeh communication, data conversion, authentication aur message handling ko आसान banata hai.

#### Working

```text
Application A → Middleware → Application B / Database / Service
```

### 4.11.2 Functions

- Applications connect karna
- Different data formats convert karna
- Messages route karna
- Authentication and security
- Database access manage karna
- Distributed systems coordinate karna

#### Examples

- Database middleware
- Message-oriented middleware
- Web application server
- API gateway
- Remote procedure call system

### 4.11.3 Firmware and Middleware Difference

| Basis | Firmware | Middleware |
|---|---|---|
| Main Role | Hardware control | Software systems connect karna |
| Location | Device non-volatile memory | System/server software layer |
| Level | Low-level | Intermediate software level |
| Example | Router firmware | API gateway |

---

## 4.12 Software Licensing

### 4.12.1 Proprietary Software

Owner copyright aur source-code control rakhta hai. Use license conditions ke according hota hai.

### 4.12.2 Open-Source Software

Source code available hota hai aur license ke अनुसार study, modify aur distribute kiya ja sakta hai.

### 4.12.3 Freeware

Use ke liye free hota hai, lekin source code aur modification rights necessarily available nahi hote.

### 4.12.4 Shareware

Trial basis ya limited features ke saath distribute hota hai.

### 4.12.5 Public-Domain Software

Copyright restrictions se free software, applicable law aur dedication conditions ke अनुसार.

### 4.12.6 Licensing Comparison

| Type | Use Cost | Source Code | Typical Restriction |
|---|---|---|---|
| Proprietary | Free or paid | Usually closed | License-controlled |
| Open source | Often free | Available | Open-source license |
| Freeware | Free | Usually closed | Modification restricted |
| Shareware | Trial/limited | Usually closed | Time/features limited |

---

## 4.13 Software Installation and Maintenance

### 4.13.1 Installation

Software files ko system par copy aur configure karke usable banana.

### 4.13.2 Activation

Valid license verify karke software features enable karna.

### 4.13.3 Update

Improvements, compatibility changes aur bug fixes install karna.

### 4.13.4 Patch

Specific problem ya security vulnerability fix karne wala smaller update.

### 4.13.5 Upgrade

Software ke newer major version par move karna.

### 4.13.6 Uninstallation

Software aur related components ko system se remove karna.

### 4.13.7 Safe Software Practices

- Trusted source se software install karein.
- License aur system requirements check karein.
- Security updates timely install karein.
- Important data ka backup rakhein.
- Pirated/cracked software avoid karein.
- Unnecessary permissions allow na karein.

---

## 4.14 Important Differences

### 4.14.1 System Software vs Application Software

| Basis | System Software | Application Software |
|---|---|---|
| Purpose | Hardware/resources manage karna | User task perform karna |
| User Interaction | Mostly background/platform | Direct interaction |
| Dependency | System operation ke liye essential | OS par depend |
| Examples | OS, driver, utility | Word processor, browser |

### 4.14.2 Software vs Firmware

| Software | Firmware |
|---|---|
| General programs/applications | Hardware-specific low-level software |
| Storage device par installed | Non-volatile device memory mein stored |
| Frequently changed ho sakta hai | Less frequently updated |
| Example: browser | Example: router firmware |

### 4.14.3 Utility vs Application Software

| Utility Software | Application Software |
|---|---|
| System maintain/protect karta hai | User task complete karta hai |
| Often background/support role | Direct user work |
| Example: antivirus | Example: spreadsheet |

---

## 4.15 Chapter Summary

Computer software is a collection of programs and instructions that enables hardware to perform useful tasks. System software manages hardware and provides a platform through operating systems, device drivers, language translators and utilities. Application software helps users perform general, specialized or customized tasks such as document creation, calculation, browsing, billing and management. Programming software supports coding, compilation, debugging and version control. Firmware provides low-level control from non-volatile device memory, while middleware connects applications and services. Software may be distributed under proprietary, open-source, freeware or shareware licenses and should be installed, updated and maintained through safe and trusted methods.

---

## 4.16 Quick Revision

- Software programs aur instructions ka collection hai.
- System software hardware manage aur platform provide karta hai.
- Operating system user, applications aur hardware ke beech interface hai.
- Driver OS ko hardware se communicate karata hai.
- Assembler, compiler aur interpreter language translators hain.
- Utility software system maintain aur protect karta hai.
- Application software user-specific tasks perform karta hai.
- Firmware non-volatile memory mein stored low-level software hai.
- Middleware applications aur services ko connect karta hai.
- Patch specific bug ya security problem fix karta hai.

---

## 4.17 Important Abbreviations

| Abbreviation | Full Form |
|---|---|
| OS | Operating System |
| GUI | Graphical User Interface |
| CLI | Command-Line Interface |
| RTOS | Real-Time Operating System |
| IDE | Integrated Development Environment |
| API | Application Programming Interface |
| BIOS | Basic Input/Output System |
| UEFI | Unified Extensible Firmware Interface |

---

## 4.18 Multiple-Choice Questions

### 1. Computer hardware ko manage karne wala software kaunsa hai?

A. Application software  
B. System software  
C. Presentation file  
D. Document  

**✅ Answer:** B

### 2. User aur hardware ke beech interface kaun provide karta hai?

A. Operating system  
B. Keyboard  
C. Spreadsheet  
D. Printer  

**✅ Answer:** A

### 3. Hardware device se communication ke liye kya chahiye?

A. Device driver  
B. Presentation  
C. Database record  
D. Image file  

**✅ Answer:** A

### 4. Complete source program translate karne wala tool kya hai?

A. Scanner  
B. Compiler  
C. Printer  
D. Browser  

**✅ Answer:** B

### 5. System maintenance ke liye kaunsa software use hota hai?

A. Utility software  
B. Customized billing only  
C. Presentation slide  
D. Firmware only  

**✅ Answer:** A

### 6. Hardware ki non-volatile memory mein stored low-level software kya hai?

A. Middleware  
B. Firmware  
C. Spreadsheet  
D. Freeware  

**✅ Answer:** B

### 7. Do applications ko connect karne wali software layer kya hai?

A. Hardware  
B. Middleware  
C. Keyboard driver only  
D. Output unit  

**✅ Answer:** B

### 8. Source code available software ko generally kya kehte hain?

A. Open-source software  
B. Shareware only  
C. Hardware  
D. Firmware  

**✅ Answer:** A

### 9. Specific security problem fix karne wala small update kya hai?

A. Patch  
B. Keyboard  
C. Compiler  
D. Database  

**✅ Answer:** A

### 10. Microsoft Word kis category ka example hai?

A. Application software  
B. Device driver  
C. Firmware  
D. Translator  

**✅ Answer:** A

---

## 4.19 Short-Answer Questions

1. Computer software ko define kijiye.
2. Hardware aur software mein difference likhiye.
3. System software kya hai?
4. Operating system ke four functions likhiye.
5. Device driver kya karta hai?
6. Compiler aur interpreter mein difference likhiye.
7. Utility software kya hai? Two examples dijiye.
8. Application software ko define kijiye.
9. General-purpose aur customized software compare kijiye.
10. Programming software kya hai?
11. Firmware kya hai? Two examples dijiye.
12. Middleware ka role kya hai?
13. Open-source aur proprietary software mein difference likhiye.
14. Patch aur upgrade kya hain?

---

## 4.20 Long-Answer and Exam Questions

1. Computer software ki classification diagram aur examples ke saath explain kijiye.
2. System software aur uske different types detail mein samjhaiye.
3. Operating system ke functions aur types explain kijiye.
4. Assembler, compiler aur interpreter compare kijiye.
5. Utility software ke types aur uses explain kijiye.
6. Application software ki categories examples ke saath describe kijiye.
7. Firmware ki characteristics, uses aur examples explain kijiye.
8. Middleware kya hai? Iske functions aur types explain kijiye.
9. Different software-license categories compare kijiye.
10. Safe software installation aur maintenance practices explain kijiye.

---

## 4.21 Practical Exercises

1. Apne computer ya phone ka operating system aur version identify kijiye.
2. Installed device drivers ki list dekhiye.
3. Five system aur five application software ke examples likhiye.
4. File-compression utility se ek folder compress kijiye.
5. Kisi word processor mein document create aur save kijiye.
6. Compiler aur interpreter ka simple comparison chart banaiye.
7. Apne daily-use software ki license category identify kijiye.

---

## 4.22 Viva Questions

1. Software ko touch kyun nahi kar sakte?
2. Operating system ke bina application kyun nahi chalti?
3. Driver ka role kya hai?
4. Compiler aur interpreter mein main difference kya hai?
5. Antivirus kis category ka software hai?
6. Word processor kis category mein aata hai?
7. Firmware power off par delete kyun nahi hota?
8. Middleware ki zarurat kab hoti hai?
9. Freeware aur open source same kyun nahi hain?
10. Software update kyun important hai?

---

## 4.23 Answers to Selected Viva Questions

1. Software non-physical instructions aur programs ka collection hai.
2. Operating system resources aur execution platform provide karta hai.
3. Driver OS aur hardware ke beech communication enable karta hai.
4. Compiler whole program aur interpreter instructions ko step-by-step translate karta hai.
5. Antivirus utility software hai.
6. Word processor application software hai.
7. Firmware non-volatile memory mein stored hota hai.
8. Jab applications ya services ko communicate/data exchange karna ho.
9. Freeware free-to-use ho sakta hai, lekin source code available hona zaroori nahi.
10. Updates security, stability, compatibility aur performance improve karte hain.

---

<div align="center">

### ✅ Chapter 4 Complete

[⬅️ Previous Chapter](chapter-03-input-and-output-devices.md) · [📚 Table of Contents](../SUMMARY.md) · **Next: Introduction to the Internet ➡️**

</div>
