<div align="center">

# 🔢 Chapter 6: Number Systems and Computer Codes

### 🟢 Unit B — Computer Software and Computer Codes

![Level](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-orange?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Practice](https://img.shields.io/badge/Includes-Solved%20Examples-success?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Number system, base aur positional value samajh सकेंगे.
- Decimal, binary, octal aur hexadecimal systems identify kar सकेंगे.
- Numbers ko ek base se doosre base mein convert kar सकेंगे.
- Binary addition, subtraction, multiplication aur division perform kar सकेंगे.
- Fractional numbers ka base conversion kar सकेंगे.
- Signed-magnitude, 1's complement aur 2's complement samajh सकेंगे.
- Signed binary numbers ki range calculate kar सकेंगे.
- BCD, ASCII, Unicode aur related computer codes explain kar सकेंगे.

---

# 6.1 Introduction to Number Systems

## 6.1.1 Meaning of Number System

### 📘 English Definition

> A number system is a method of representing numbers using a defined set of digits and rules.

### 💬 Hinglish Explanation

Number system numbers ko likhne aur represent karne ka तरीका hai. Har number system mein kuch allowed digits aur ek **base** hota hai.

## 6.1.2 Base or Radix

Number system mein available unique digits ki total quantity ko **base** ya **radix** kehte hain.

| Number System | Base | Allowed Digits |
|---|---:|---|
| Binary | 2 | 0, 1 |
| Octal | 8 | 0–7 |
| Decimal | 10 | 0–9 |
| Hexadecimal | 16 | 0–9, A–F |

## 6.1.3 Positional Number System

Digit ki value uske digit aur position dono par depend karti hai.

### 6.1.3.1 General Form

For base $r$:

$$
(d_n...d_2d_1d_0.d_{-1}d_{-2}...)_r
$$

Its decimal value is:

$$
\sum d_i \times r^i
$$

## 6.1.4 Place-Value Example

Decimal number:

$$
(572.4)_{10}
$$

$$
= 5\times10^2 + 7\times10^1 + 2\times10^0 + 4\times10^{-1}
$$

$$
= 500+70+2+0.4=572.4
$$

## 6.1.5 Important Terms

| Term | Pronunciation | Meaning |
|---|---|---|
| Number System | नम्बर सिस्टम | Numbers represent karne ka method |
| Base/Radix | बेस/रेडिक्स | Unique digits ki count |
| Positional Value | पोज़िशनल वैल्यू | Position ke according digit value |
| MSB | मोस्ट सिग्निफिकेंट बिट | Leftmost important bit |
| LSB | लीस्ट सिग्निफिकेंट बिट | Rightmost bit |
| Integer | इंटीजर | Whole-number part |
| Fraction | फ्रैक्शन | Radix point ke baad ka part |
| Complement | कॉम्प्लिमेंट | Binary subtraction/negative representation technique |

---

# 6.2 Decimal Number System

## 6.2.1 Meaning

Decimal system ka base **10** hai aur digits `0` se `9` tak hain.

## 6.2.2 Positional Weights

```text
... 10³  10²  10¹  10⁰ . 10⁻¹  10⁻² ...
```

## 6.2.3 Example

$$
(3847)_{10}
$$

$$
=3\times10^3+8\times10^2+4\times10^1+7\times10^0
$$

$$
=3000+800+40+7
$$

---

# 6.3 Binary Number System

## 6.3.1 Meaning

Binary system ka base **2** hai. Ismein sirf `0` aur `1` digits use hoti hain.

## 6.3.2 Why Computers Use Binary

Electronic circuits easily two stable states represent karte hain:

| Binary | Electronic Meaning |
|---:|---|
| 0 | OFF, Low, False |
| 1 | ON, High, True |

## 6.3.3 Positional Weights

```text
... 2⁴  2³  2²  2¹  2⁰ . 2⁻¹  2⁻²  2⁻³ ...
```

## 6.3.4 Binary Place Values

| Power | Value |
|---:|---:|
| $2^0$ | 1 |
| $2^1$ | 2 |
| $2^2$ | 4 |
| $2^3$ | 8 |
| $2^4$ | 16 |
| $2^5$ | 32 |
| $2^6$ | 64 |
| $2^7$ | 128 |
| $2^8$ | 256 |

---

# 6.4 Binary to Decimal Conversion

## 6.4.1 Method

Har binary digit ko corresponding power of 2 se multiply karke values add karein.

## 6.4.2 Solved Example 1

Convert $(101101)_2$ to decimal.

$$
(101101)_2 =
1\times2^5+0\times2^4+1\times2^3+1\times2^2+0\times2^1+1\times2^0
$$

$$
=32+0+8+4+0+1=45
$$

Therefore:

$$
(101101)_2=(45)_{10}
$$

## 6.4.3 Solved Example 2

Convert $(11001)_2$ to decimal.

$$
=1\times16+1\times8+0\times4+0\times2+1\times1
$$

$$
=25
$$

Therefore:

$$
(11001)_2=(25)_{10}
$$

---

# 6.5 Decimal Integer to Binary Conversion

## 6.5.1 Repeated Division Method

1. Decimal number ko 2 se divide karein.
2. Remainder note karein.
3. Quotient ko again 2 se divide karein.
4. Quotient 0 hone tak repeat karein.
5. Remainders ko bottom-to-top read karein.

## 6.5.2 Solved Example

Convert $(45)_{10}$ to binary.

| Division | Quotient | Remainder |
|---|---:|---:|
| 45 ÷ 2 | 22 | 1 |
| 22 ÷ 2 | 11 | 0 |
| 11 ÷ 2 | 5 | 1 |
| 5 ÷ 2 | 2 | 1 |
| 2 ÷ 2 | 1 | 0 |
| 1 ÷ 2 | 0 | 1 |

Bottom-to-top:

$$
(45)_{10}=(101101)_2
$$

---

# 6.6 Octal Number System

## 6.6.1 Meaning

Octal system ka base **8** hai. Allowed digits `0` se `7` tak hain.

## 6.6.2 Positional Weights

```text
... 8³  8²  8¹  8⁰ . 8⁻¹  8⁻² ...
```

## 6.6.3 Octal to Decimal Example

Convert $(725)_8$ to decimal.

$$
7\times8^2+2\times8^1+5\times8^0
$$

$$
=7\times64+2\times8+5=469
$$

Therefore:

$$
(725)_8=(469)_{10}
$$

## 6.6.4 Decimal to Octal Example

Convert $(156)_{10}$ to octal.

| Division | Quotient | Remainder |
|---|---:|---:|
| 156 ÷ 8 | 19 | 4 |
| 19 ÷ 8 | 2 | 3 |
| 2 ÷ 8 | 0 | 2 |

Bottom-to-top:

$$
(156)_{10}=(234)_8
$$

---

# 6.7 Hexadecimal Number System

## 6.7.1 Meaning

Hexadecimal system ka base **16** hai.

| Decimal | Hexadecimal |
|---:|:---:|
| 0–9 | 0–9 |
| 10 | A |
| 11 | B |
| 12 | C |
| 13 | D |
| 14 | E |
| 15 | F |

## 6.7.2 Positional Weights

```text
... 16³  16²  16¹  16⁰ . 16⁻¹  16⁻² ...
```

## 6.7.3 Hexadecimal to Decimal Example

Convert $(2AF)_{16}$ to decimal.

$$
2\times16^2+10\times16^1+15\times16^0
$$

$$
=512+160+15=687
$$

Therefore:

$$
(2AF)_{16}=(687)_{10}
$$

## 6.7.4 Decimal to Hexadecimal Example

Convert $(254)_{10}$ to hexadecimal.

| Division | Quotient | Remainder |
|---|---:|---:|
| 254 ÷ 16 | 15 | 14 = E |
| 15 ÷ 16 | 0 | 15 = F |

Bottom-to-top:

$$
(254)_{10}=(FE)_{16}
$$

## 6.7.5 Uses of Hexadecimal

- Memory addresses
- Machine-code representation
- Color codes
- Debugging
- Binary data ka compact representation

---

# 6.8 Binary and Octal Conversion

## 6.8.1 Binary to Octal

Radix point se left aur right side bits ko **3-3 ke groups** mein divide karein.

### Solved Example

Convert $(1101011)_2$ to octal.

```text
001 101 011
 1   5   3
```

Therefore:

$$
(1101011)_2=(153)_8
$$

## 6.8.2 Octal to Binary

Har octal digit ko equivalent 3-bit binary group mein convert karein.

| Octal | Binary |
|---:|:---:|
| 0 | 000 |
| 1 | 001 |
| 2 | 010 |
| 3 | 011 |
| 4 | 100 |
| 5 | 101 |
| 6 | 110 |
| 7 | 111 |

### Example

$$
(572)_8
$$

```text
5 → 101
7 → 111
2 → 010
```

$$
(572)_8=(101111010)_2
$$

---

# 6.9 Binary and Hexadecimal Conversion

## 6.9.1 Binary to Hexadecimal

Bits ko **4-4 ke groups** mein divide karein.

### Solved Example

Convert $(1101111010)_2$ to hexadecimal.

```text
0011 0111 1010
  3    7    A
```

Therefore:

$$
(1101111010)_2=(37A)_{16}
$$

## 6.9.2 Hexadecimal to Binary

Har hexadecimal digit ko 4-bit binary group mein convert karein.

| Hex | Binary | Hex | Binary |
|:---:|:---:|:---:|:---:|
| 0 | 0000 | 8 | 1000 |
| 1 | 0001 | 9 | 1001 |
| 2 | 0010 | A | 1010 |
| 3 | 0011 | B | 1011 |
| 4 | 0100 | C | 1100 |
| 5 | 0101 | D | 1101 |
| 6 | 0110 | E | 1110 |
| 7 | 0111 | F | 1111 |

### Example

$$
(9C)_{16}
$$

```text
9 → 1001
C → 1100
```

$$
(9C)_{16}=(10011100)_2
$$

---

# 6.10 Octal and Hexadecimal Conversion

Direct digit grouping common nahi hai. Pehle binary mein convert karein.

## 6.10.1 Octal to Hexadecimal Example

Convert $(73)_8$ to hexadecimal.

```text
7 → 111
3 → 011
Binary = 111011
Group in 4 bits = 0011 1011
Hex = 3B
```

Therefore:

$$
(73)_8=(3B)_{16}
$$

## 6.10.2 Hexadecimal to Octal Example

Convert $(2D)_{16}$ to octal.

```text
2 → 0010
D → 1101
Binary = 00101101
Group in 3 bits = 00 101 101
Octal = 55
```

Therefore:

$$
(2D)_{16}=(55)_8
$$

---

# 6.11 Working with Fractions

## 6.11.1 Binary Fraction to Decimal

Radix point ke right side positions $2^{-1}, 2^{-2}, 2^{-3}...$ hoti hain.

### Solved Example

Convert $(101.101)_2$ to decimal.

$$
1\times2^2+0\times2^1+1\times2^0+
1\times2^{-1}+0\times2^{-2}+1\times2^{-3}
$$

$$
=4+0+1+0.5+0+0.125
$$

$$
=5.625
$$

Therefore:

$$
(101.101)_2=(5.625)_{10}
$$

## 6.11.2 Decimal Fraction to Binary

Fractional part ko repeatedly 2 se multiply karein. Har multiplication ka integer part top-to-bottom read karein.

### Solved Example

Convert $(0.625)_{10}$ to binary.

| Multiplication | Integer Part | Fraction |
|---|---:|---:|
| 0.625 × 2 = 1.250 | 1 | 0.250 |
| 0.250 × 2 = 0.500 | 0 | 0.500 |
| 0.500 × 2 = 1.000 | 1 | 0.000 |

Therefore:

$$
(0.625)_{10}=(0.101)_2
$$

## 6.11.3 Mixed Decimal to Binary Example

Convert $(10.625)_{10}$ to binary.

- Integer part: $(10)_{10}=(1010)_2$
- Fraction part: $(0.625)_{10}=(0.101)_2$

Therefore:

$$
(10.625)_{10}=(1010.101)_2
$$

## 6.11.4 Octal Fraction to Decimal Example

Convert $(17.4)_8$ to decimal.

$$
1\times8^1+7\times8^0+4\times8^{-1}
$$

$$
=8+7+0.5=15.5
$$

## 6.11.5 Hexadecimal Fraction to Decimal Example

Convert $(A.8)_{16}$ to decimal.

$$
10\times16^0+8\times16^{-1}
$$

$$
=10+\frac{8}{16}=10.5
$$

## 6.11.6 Non-Terminating Fractions

Har decimal fraction binary mein exactly terminate nahi hoti. Aise cases mein required precision tak bits calculate karke approximation use ki jati hai.

---

# 6.12 Binary Arithmetic

## 6.12.1 Binary Addition Rules

| Operation | Sum | Carry |
|---|---:|---:|
| 0 + 0 | 0 | 0 |
| 0 + 1 | 1 | 0 |
| 1 + 0 | 1 | 0 |
| 1 + 1 | 0 | 1 |
| 1 + 1 + 1 | 1 | 1 |

### Solved Example

```text
   1011
 + 0110
 ------
  10001
```

$$
(1011)_2+(0110)_2=(10001)_2
$$

## 6.12.2 Binary Subtraction Rules

| Operation | Difference | Borrow |
|---|---:|---:|
| 0 − 0 | 0 | 0 |
| 1 − 0 | 1 | 0 |
| 1 − 1 | 0 | 0 |
| 0 − 1 | 1 | 1 from next position |

### Solved Example

```text
   1010
 - 0011
 ------
   0111
```

## 6.12.3 Binary Multiplication Rules

| Operation | Result |
|---|---:|
| 0 × 0 | 0 |
| 0 × 1 | 0 |
| 1 × 0 | 0 |
| 1 × 1 | 1 |

### Solved Example

```text
     101
   ×  11
   -----
     101
+   1010
   -----
    1111
```

## 6.12.4 Binary Division

Binary long division decimal division jaisi hoti hai, lekin digits 0 aur 1 hote hain.

### Example

$$
(1100)_2 \div (10)_2=(110)_2
$$

Because:

$$
12\div2=6
$$

---

# 6.13 Signed Number Representation

## 6.13.1 Need for Signed Numbers

Computer ko positive aur negative dono integers represent karne hote hain. Fixed number of bits mein sign represent karne ke different methods hain.

## 6.13.2 Sign Bit

Common convention mein leftmost bit sign indicate kar sakti hai:

| Sign Bit | Meaning |
|---:|---|
| 0 | Positive |
| 1 | Negative |

---

# 6.14 Signed-Magnitude Representation

## 6.14.1 Method

MSB sign ke liye aur remaining bits magnitude ke liye use hote hain.

### 8-Bit Example

```text
+13 = 00001101
-13 = 10001101
```

## 6.14.2 Limitation

Positive zero aur negative zero ke two representations hote hain:

```text
+0 = 00000000
-0 = 10000000
```

---

# 6.15 One's Complement Representation

## 6.15.1 Meaning

Positive binary number ke every bit ko invert karke negative number obtain kiya jata hai.

```text
0 → 1
1 → 0
```

## 6.15.2 Example

8-bit $+13$:

```text
00001101
```

All bits invert:

```text
11110010 = -13 in 1's complement
```

## 6.15.3 Limitation

Ismein bhi positive zero aur negative zero ke separate representations hote hain.

---

# 6.16 Two's Complement Representation

## 6.16.1 Meaning

1's complement mein 1 add karke 2's complement milta hai.

## 6.16.2 Steps

1. Positive number ka fixed-bit binary form likhein.
2. All bits invert karein.
3. Result mein 1 add karein.

## 6.16.3 Solved Example

8-bit mein $-13$ represent karein.

```text
+13                = 00001101
Invert all bits    = 11110010
Add 1              = 11110011
```

Therefore:

```text
-13 = 11110011
```

## 6.16.4 Advantages

- Sirf one representation of zero.
- Addition aur subtraction hardware simple hota hai.
- Modern computers mein signed integers ke liye widely used.

## 6.16.5 Signed Range

$n$ bits ke 2's complement number ki range:

$$
-2^{n-1}\text{ to }2^{n-1}-1
$$

### 8-Bit Range

$$
-2^7\text{ to }2^7-1
$$

$$
-128\text{ to }127
$$

## 6.16.6 Reading a Negative Two's Complement Number

Example: $(11110110)_2$

1. MSB 1, so number negative hai.
2. Bits invert: `00001001`
3. Add 1: `00001010`
4. Magnitude = 10

Therefore:

$$
(11110110)_2=-10
$$

---

# 6.17 Subtraction Using Two's Complement

## 6.17.1 Method

To calculate $A-B$:

1. $B$ ka 2's complement calculate karein.
2. Use $A$ mein add karein.
3. Final carry ho to discard karein.
4. No carry aur sign negative ho to result interpret karein.

## 6.17.2 Solved Example: $9-5$

4-bit representation:

```text
9          = 1001
5          = 0101
1's comp 5 = 1010
2's comp 5 = 1011
```

Addition:

```text
  1001
+ 1011
------
1 0100
```

Carry discard:

```text
0100 = 4
```

Therefore:

$$
9-5=4
$$

---

# 6.18 Overflow

## 6.18.1 Meaning

Fixed bits ki representable range se result outside hone par **overflow** hota hai.

### Example

4-bit 2's complement range $-8$ to $+7$ hai.

```text
  0111  (+7)
+ 0001  (+1)
------
  1000
```

Actual result $+8$ hai, jo 4-bit signed range mein represent nahi ho sakta. Isliye overflow hua.

---

# 6.19 Binary-Coded Decimal

## 6.19.1 Meaning of BCD

BCD mein each decimal digit ko separately 4-bit binary group se represent kiya jata hai.

## 6.19.2 BCD Table

| Decimal Digit | BCD |
|---:|:---:|
| 0 | 0000 |
| 1 | 0001 |
| 2 | 0010 |
| 3 | 0011 |
| 4 | 0100 |
| 5 | 0101 |
| 6 | 0110 |
| 7 | 0111 |
| 8 | 1000 |
| 9 | 1001 |

## 6.19.3 Solved Example

Decimal $59$ in BCD:

```text
5 → 0101
9 → 1001
```

Therefore:

```text
(59)₁₀ in BCD = 0101 1001
```

> ⚠️ Pure binary representation of 59 is `111011`, which is different from BCD.

## 6.19.4 Uses

- Digital clocks
- Calculators
- Financial displays
- Decimal-display systems

---

# 6.20 Character Codes

## 6.20.1 Need for Character Codes

Computers binary values store karte hain. Letters, digits, symbols aur different-language characters ko numeric codes se map karna padta hai.

## 6.20.2 ASCII

ASCII ka full form **American Standard Code for Information Interchange** hai.

### 6.20.2.1 Features

- Original standard 7-bit codes use karta hai.
- 128 values represent karta hai.
- English letters, digits, punctuation aur control characters include karta hai.

### 6.20.2.2 Examples

| Character | Decimal ASCII | Binary |
|:---:|---:|:---:|
| A | 65 | 1000001 |
| B | 66 | 1000010 |
| a | 97 | 1100001 |
| 0 | 48 | 0110000 |

## 6.20.3 Extended ASCII

Different 8-bit extensions up to 256 code positions use karte hain, lekin same universal character set nahi hote.

## 6.20.4 Unicode

Unicode worldwide writing systems ke characters ko unique code points provide karta hai.

**Examples:** English, Hindi, Arabic, Chinese characters and emojis.

### 6.20.4.1 Unicode Encodings

- UTF-8
- UTF-16
- UTF-32

### 6.20.4.2 UTF-8

Web aur modern systems mein widely used variable-length Unicode encoding.

## 6.20.5 ASCII vs Unicode

| Basis | ASCII | Unicode |
|---|---|---|
| Character Coverage | Basic English set | Worldwide scripts and symbols |
| Original Size | 7-bit | Large code space |
| Encodings | ASCII | UTF-8, UTF-16, UTF-32 |
| Use | Legacy/basic text | Modern multilingual text |

---

# 6.21 Error-Detection Code

## 6.21.1 Parity Bit

Data transmission/storage mein simple error detection ke liye extra bit add ki ja sakti hai.

## 6.21.2 Even Parity

Total 1-bits ki count even banayi jati hai.

### Example

Data: `1011001` contains four 1s. Even parity bit = `0`.

## 6.21.3 Odd Parity

Total 1-bits ki count odd banayi jati hai.

Same data mein four 1s hain, so odd parity bit = `1`.

## 6.21.4 Limitation

Single parity sab types ke multiple-bit errors detect nahi kar sakti aur error correct nahi karti.

---

# 6.22 Important Differences

## 6.22.1 Binary vs Octal vs Hexadecimal

| Basis | Binary | Octal | Hexadecimal |
|---|---:|---:|---:|
| Base | 2 | 8 | 16 |
| Digits | 0–1 | 0–7 | 0–9, A–F |
| Binary Group | 1 bit | 3 bits | 4 bits |
| Use | Machine representation | Compact binary | Addresses/debugging/colors |

## 6.22.2 Signed Magnitude vs 1's vs 2's Complement

| Basis | Signed Magnitude | 1's Complement | 2's Complement |
|---|---|---|---|
| Negative Form | Sign bit changes | All bits invert | Invert + 1 |
| Zero Forms | Two | Two | One |
| Arithmetic | Complex | End-around carry | Simplest/common |
| Modern Use | Limited | Limited | Widely used |

## 6.22.3 Pure Binary vs BCD

| Pure Binary | BCD |
|---|---|
| Whole number converted together | Each decimal digit separately |
| Compact representation | More bits may be needed |
| $59=111011$ | $59=0101\ 1001$ |

---

# 6.23 Chapter Summary

A number system represents values through a defined set of digits and a base. Computers use binary internally, while octal and hexadecimal provide compact forms of binary data and decimal is used in everyday calculations. Base conversions use positional weights, repeated division, repeated multiplication or binary grouping. Fractional numbers use negative positional powers, and binary arithmetic follows rules based on the digits 0 and 1. Signed values can be represented through signed magnitude, 1's complement or 2's complement, with 2's complement being widely used because it provides one zero and simpler arithmetic. BCD represents each decimal digit separately, ASCII and Unicode encode characters, and parity bits provide basic error detection.

---

# 6.24 Quick Revision

- Base unique digits ki total count hoti hai.
- Binary base 2, octal 8, decimal 10 aur hexadecimal 16 hai.
- Binary-to-octal conversion mein 3-bit groups bante hain.
- Binary-to-hex conversion mein 4-bit groups bante hain.
- Decimal fraction to binary ke liye repeated multiplication by 2 hota hai.
- 2's complement = bits invert + 1.
- $n$-bit signed 2's complement range $-2^{n-1}$ to $2^{n-1}-1$ hai.
- BCD each decimal digit ko separate 4-bit group deta hai.
- ASCII basic English characters encode karta hai.
- Unicode multilingual characters aur symbols support karta hai.
- Parity bit simple error detection ke liye use hoti hai.

---

# 6.25 Important Abbreviations

| Abbreviation | Full Form |
|---|---|
| MSB | Most Significant Bit |
| LSB | Least Significant Bit |
| BCD | Binary-Coded Decimal |
| ASCII | American Standard Code for Information Interchange |
| UTF | Unicode Transformation Format |
| DNS | Domain Name System |
| 1's Comp. | One's Complement |
| 2's Comp. | Two's Complement |

---

# 6.26 Multiple-Choice Questions

### 1. Binary number system ka base kya hai?

A. 2  
B. 8  
C. 10  
D. 16  

**✅ Answer:** A

### 2. Hexadecimal digit F ki decimal value kya hai?

A. 10  
B. 12  
C. 15  
D. 16  

**✅ Answer:** C

### 3. $(1010)_2$ ki decimal value kya hai?

A. 8  
B. 10  
C. 12  
D. 14  

**✅ Answer:** B

### 4. Ek octal digit kitne binary bits ke equivalent hai?

A. 2  
B. 3  
C. 4  
D. 8  

**✅ Answer:** B

### 5. Ek hexadecimal digit kitne binary bits ke equivalent hai?

A. 2  
B. 3  
C. 4  
D. 16  

**✅ Answer:** C

### 6. 2's complement kaise obtain hota hai?

A. Bits invert only  
B. 1 add only  
C. Bits invert karke 1 add  
D. 2 se divide  

**✅ Answer:** C

### 7. 8-bit signed 2's complement range kya hai?

A. 0 to 255  
B. -127 to 127  
C. -128 to 127  
D. -128 to 128  

**✅ Answer:** C

### 8. BCD mein decimal digit 9 kya hai?

A. 1111  
B. 1001  
C. 1010  
D. 0111  

**✅ Answer:** B

### 9. Multilingual characters ke liye suitable standard kaunsa hai?

A. ASCII only  
B. Unicode  
C. BCD  
D. Parity  

**✅ Answer:** B

### 10. $(0.625)_{10}$ ka binary form kya hai?

A. 0.011  
B. 0.101  
C. 0.110  
D. 0.111  

**✅ Answer:** B

---

# 6.27 Short-Answer Questions

1. Number system aur base ko define kijiye.
2. Positional value kya hai?
3. Binary system computers mein kyun use hota hai?
4. Binary number ko decimal mein kaise convert karte hain?
5. Decimal integer ko binary mein convert karne ke steps likhiye.
6. Binary-to-octal conversion explain kijiye.
7. Binary-to-hexadecimal conversion explain kijiye.
8. Decimal fraction ko binary fraction mein kaise convert karte hain?
9. Binary addition ke rules likhiye.
10. Signed-magnitude representation kya hai?
11. 1's aur 2's complement mein difference likhiye.
12. Overflow kya hai?
13. BCD kya hai?
14. ASCII aur Unicode mein difference likhiye.
15. Parity bit kya hai?

---

# 6.28 Long-Answer and Exam Questions

1. Decimal, binary, octal aur hexadecimal systems ko examples ke saath explain kijiye.
2. Different base-conversion methods solved examples ke saath samjhaiye.
3. Binary, octal aur hexadecimal ke direct grouping conversions explain kijiye.
4. Integer aur fractional decimal numbers ko binary mein convert kijiye.
5. Binary arithmetic operations solved examples ke saath explain kijiye.
6. Signed magnitude, 1's complement aur 2's complement compare kijiye.
7. 2's complement subtraction aur overflow explain kijiye.
8. BCD code ko pure binary representation se compare kijiye.
9. ASCII aur Unicode character codes explain kijiye.
10. Parity-based error detection explain kijiye.

---

# 6.29 Practice Problems

## 6.29.1 Convert to Decimal

1. $(101011)_2$
2. $(1101.101)_2$
3. $(347)_8$
4. $(2F9)_{16}$

## 6.29.2 Convert from Decimal

1. $(75)_{10}$ to binary
2. $(256)_{10}$ to octal
3. $(4095)_{10}$ to hexadecimal
4. $(12.375)_{10}$ to binary

## 6.29.3 Direct Conversions

1. $(111010101)_2$ to octal
2. $(1011110010)_2$ to hexadecimal
3. $(657)_8$ to binary
4. $(A7F)_{16}$ to binary

## 6.29.4 Signed Representation

1. Represent $-25$ in 8-bit signed magnitude.
2. Represent $-25$ in 8-bit 1's complement.
3. Represent $-25$ in 8-bit 2's complement.
4. Find decimal value of 8-bit 2's complement `11100110`.

## 6.29.5 Binary Arithmetic

1. $1011+1101$
2. $11010-01011$
3. $101\times111$
4. $11000\div10$

---

# 6.30 Answers to Selected Practice Problems

1. $(101011)_2=(43)_{10}$
2. $(347)_8=(231)_{10}$
3. $(75)_{10}=(1001011)_2$
4. $(256)_{10}=(400)_8$
5. $(4095)_{10}=(FFF)_{16}$
6. $(111010101)_2=(725)_8$
7. $(657)_8=(110101111)_2$
8. $-25$ in 8-bit 2's complement = `11100111`
9. `11100110` in 8-bit 2's complement = $-26$
10. $1011+1101=11000$

---

# 6.31 Viva Questions

1. Radix kya hota hai?
2. Binary system mein kaunse digits hote hain?
3. Octal digit 7 ka binary group kya hai?
4. Hexadecimal A ki decimal value kya hai?
5. Radix point ke right-side powers negative kyun hoti hain?
6. 1's complement kaise banate hain?
7. 2's complement ka main advantage kya hai?
8. BCD aur binary same hain?
9. ASCII ka purpose kya hai?
10. UTF-8 kis standard se related hai?

---

# 6.32 Answers to Selected Viva Questions

1. Radix number system mein unique digits ki count hai.
2. Binary mein 0 aur 1 digits hote hain.
3. Octal 7 ka 3-bit binary group `111` hai.
4. Hexadecimal A ki decimal value 10 hai.
5. Fraction positions base ke inverse powers represent karti hain.
6. Har bit ko invert karke 1's complement banta hai.
7. 2's complement mein one zero aur simpler arithmetic hoti hai.
8. Nahi. BCD each decimal digit separately encode karta hai.
9. ASCII basic characters ko numeric codes se represent karta hai.
10. UTF-8 Unicode character encoding hai.

---

<div align="center">

## ✅ Chapter 6 Complete

[⬅️ Previous Chapter](chapter-05-introduction-to-the-internet.md) · [📚 Table of Contents](../SUMMARY.md) · **Next: Introduction to C++ ➡️**

</div>
