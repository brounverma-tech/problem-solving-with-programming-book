<div align="center">

# ⚙️ Chapter 8: Operators and Expressions

### 🟠 Unit C — Programming Fundamentals Using C++

![Level](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-orange?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Code](https://img.shields.io/badge/Programs-C%2B%2B-purple?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Operator, operand aur expression define kar sakenge.
- Arithmetic, relational, logical aur assignment operators use kar sakenge.
- Prefix aur postfix increment/decrement samajh sakenge.
- Bitwise aur conditional operators apply kar sakenge.
- Precedence aur associativity ke according expressions evaluate kar sakenge.
- Implicit aur explicit type conversion samajh sakenge.

---

## 8.1 Operator, Operand and Expression

### 8.1.1 Operator

> An operator is a symbol that performs a specific operation on one or more operands.

**Hinglish:** Operator ek symbol hai jo values ya variables par operation karta hai. Example: `a + b` mein `+` operator hai.

### 8.1.2 Operand

Operator jis value ya variable par work karta hai, use operand kehte hain. `a + b` mein `a` aur `b` operands hain.

### 8.1.3 Expression

> An expression is a valid combination of operators and operands that produces a value.

```cpp
(a + b) * 2
```

### 8.1.4 Types by Operand Count

| Type | Operands | Example |
|---|---:|---|
| Unary | 1 | `-x`, `++x`, `!flag` |
| Binary | 2 | `a + b`, `x > y` |
| Ternary | 3 expressions | `condition ? a : b` |

---

## 8.2 Arithmetic Operators

| Operator | Operation | Example |
|:---:|---|---|
| `+` | Addition | `a + b` |
| `-` | Subtraction | `a - b` |
| `*` | Multiplication | `a * b` |
| `/` | Division | `a / b` |
| `%` | Remainder | `a % b` |

### Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    int a = 17;
    int b = 5;

    cout << "Addition = " << a + b << '\n';
    cout << "Subtraction = " << a - b << '\n';
    cout << "Multiplication = " << a * b << '\n';
    cout << "Integer division = " << a / b << '\n';
    cout << "Remainder = " << a % b << '\n';

    return 0;
}
```

### 8.2.1 Integer Division

Dono operands integer hon to fractional part truncate ho jata hai.

```cpp
cout << 7 / 2;    // 3
cout << 7.0 / 2;  // 3.5
```

### 8.2.2 Modulus Uses

- Even/odd check
- Divisibility test
- Last digit obtain karna
- Cyclic calculations

> Division ya modulus se pehle divisor non-zero check karein.

---

## 8.3 Increment and Decrement Operators

### 8.3.1 Prefix

Pehle value update, phir expression mein use.

```cpp
int x = 5;
int y = ++x;  // x = 6, y = 6
```

### 8.3.2 Postfix

Pehle old value use, phir update.

```cpp
int x = 5;
int y = x++;  // y = 5, x = 6
```

| Form | Action |
|---|---|
| `++x` | Increase, then use |
| `x++` | Use, then increase |
| `--x` | Decrease, then use |
| `x--` | Use, then decrease |

---

## 8.4 Relational Operators

Relational operators comparison karke Boolean result dete hain.

| Operator | Meaning |
|:---:|---|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

```cpp
int a = 10;
int b = 20;

cout << boolalpha;
cout << (a == b) << '\n';  // false
cout << (a != b) << '\n';  // true
cout << (a < b) << '\n';   // true
```

### 8.4.1 Assignment vs Equality

```cpp
x = 5;   // Assignment
x == 5;  // Comparison
```

---

## 8.5 Logical Operators

| Operator | Name | True When |
|:---:|---|---|
| `&&` | Logical AND | Both conditions true |
| `\|\|` | Logical OR | At least one true |
| `!` | Logical NOT | Condition ko reverse karta hai |

### 8.5.1 Truth Table

| A | B | A && B | A \|\| B |
|:---:|:---:|:---:|:---:|
| false | false | false | false |
| false | true | false | true |
| true | false | false | true |
| true | true | true | true |

### 8.5.2 Short-Circuit Evaluation

- AND mein first condition false ho to second evaluate nahi hoti.
- OR mein first condition true ho to second evaluate nahi hoti.

```cpp
if (denominator != 0 && numerator / denominator > 2)
{
    cout << "Condition true";
}
```

---

## 8.6 Assignment Operators

| Operator | Equivalent |
|:---:|---|
| `x = y` | y ki value x mein |
| `x += y` | `x = x + y` |
| `x -= y` | `x = x - y` |
| `x *= y` | `x = x * y` |
| `x /= y` | `x = x / y` |
| `x %= y` | `x = x % y` |

```cpp
int score = 50;
score += 10;  // 60
score -= 5;   // 55
score *= 2;   // 110
```

Assignment right-to-left associate hota hai:

```cpp
int a, b, c;
a = b = c = 0;
```

---

## 8.7 Bitwise Operators

Bitwise operators integer values ke individual bits par work karte hain.

| Operator | Name |
|:---:|---|
| `&` | Bitwise AND |
| `\|` | Bitwise OR |
| `^` | Bitwise XOR |
| `~` | Bitwise NOT |
| `<<` | Left shift |
| `>>` | Right shift |

### Binary Examples

```text
  0101     0101     0101
& 0011   | 0011   ^ 0011
------   ------   ------
  0001     0111     0110
```

Therefore, for 5 and 3:

- `5 & 3 = 1`
- `5 | 3 = 7`
- `5 ^ 3 = 6`

### 8.7.1 Shift Operators

```cpp
unsigned int x = 5;
cout << (x << 1);  // 10
cout << (x >> 1);  // 2
```

### 8.7.2 Common Uses

- Flags and masks
- Permissions
- Embedded systems
- Device control
- Low-level programming

### 8.7.3 Logical vs Bitwise

| Logical | Bitwise |
|---|---|
| Boolean conditions | Individual bits |
| `&&`, `\|\|`, `!` | `&`, `\|`, `^`, `~` |
| Short-circuit possible | Both operands evaluated |

---

## 8.8 Conditional Operator

### Syntax

```cpp
condition ? valueIfTrue : valueIfFalse
```

### Example

```cpp
int age = 20;
string result = (age >= 18) ? "Adult" : "Minor";
```

### 8.8.1 Maximum of Two Values

```cpp
int maximum = (a > b) ? a : b;
```

Simple selection ke liye useful hai. Complex logic ke liye `if-else` clearer hota hai.

---

## 8.9 Special Operators

### 8.9.1 sizeof

Type ya object ki size bytes mein return karta hai.

```cpp
cout << sizeof(int);
double price = 50.5;
cout << sizeof(price);
```

### 8.9.2 Address-of and Dereference

```cpp
int value = 10;
int* ptr = &value;
cout << *ptr;
```

- `&value` address obtain karta hai.
- `*ptr` pointed value access karta hai.

### 8.9.3 Scope Resolution

`::` namespace ya class scope access karta hai.

```cpp
std::cout << "Hello";
```

---

## 8.10 Operator Precedence

Precedence decide karti hai ki expression mein kaunsa operator pehle group hoga.

| Priority | Operators | Associativity |
|---:|---|---|
| Highest | `()`, member access, postfix `++ --` | Left to right |
| High | Prefix `++ --`, unary `+ - ! ~`, `sizeof` | Right to left |
| 3 | `* / %` | Left to right |
| 4 | `+ -` | Left to right |
| 5 | `<< >>` | Left to right |
| 6 | `< <= > >=` | Left to right |
| 7 | `== !=` | Left to right |
| 8 | Bitwise AND, XOR, OR | Left to right |
| 9 | Logical AND, OR | Left to right |
| 10 | `?:` | Right to left |
| 11 | Assignment operators | Right to left |
| Lowest | Comma | Left to right |

### Example

```cpp
int result1 = 10 + 5 * 2;    // 20
int result2 = (10 + 5) * 2;  // 30
```

Parentheses intended order aur readability improve karti hain.

---

## 8.11 Associativity

Same precedence ke operators ki grouping direction associativity decide karti hai.

### 8.11.1 Left-to-Right

`20 / 5 * 2` → first 20/5, then ×2 → result 8.

### 8.11.2 Right-to-Left

`a = b = c = 10` → first c, then b, then a ko value milti hai.

> Side effects wali complex expressions avoid karein. Separate statements clearer aur safer hote hain.

---

## 8.12 Expression Evaluation

### Example 1

`10 + 6 / 2 * 3`

1. 6 / 2 = 3
2. 3 × 3 = 9
3. 10 + 9 = 19

### Example 2

`(8 + 4) * 2 - 6`

1. 8 + 4 = 12
2. 12 × 2 = 24
3. 24 - 6 = 18

### Logical Example

`5 > 3 && 10 != 8`

1. 5 > 3 → true
2. 10 != 8 → true
3. true && true → true

---

## 8.13 Type Conversion

### 8.13.1 Implicit Conversion

Compiler automatically compatible conversion karta hai.

```cpp
int count = 5;
double result = count + 2.5;
```

### 8.13.2 Widening Conversion

```cpp
int x = 25;
double y = x;
```

### 8.13.3 Narrowing Conversion

Data loss possible hota hai.

```cpp
double price = 99.95;
int whole = price;  // 99
```

### 8.13.4 Explicit Conversion

```cpp
int total = 7;
int count = 2;

double average = static_cast<double>(total) / count;
cout << average;  // 3.5
```

---

#### Program: Arithmetic Calculator

```cpp
#include <iostream>
using namespace std;

int main()
{
    double first, second;

    cout << "Enter two numbers: ";
    cin >> first >> second;

    cout << "Sum = " << first + second << '\n';
    cout << "Difference = " << first - second << '\n';
    cout << "Product = " << first * second << '\n';

    if (second != 0)
        cout << "Quotient = " << first / second << '\n';
    else
        cout << "Division by zero is not allowed.\n";

    return 0;
}
```

---

#### Program: Even or Odd

```cpp
#include <iostream>
using namespace std;

int main()
{
    int number;
    cout << "Enter an integer: ";
    cin >> number;

    cout << ((number % 2 == 0) ? "Even" : "Odd");
    return 0;
}
```

---

#### Program: Bitwise Demonstration

```cpp
#include <iostream>
using namespace std;

int main()
{
    unsigned int a = 5;
    unsigned int b = 3;

    cout << "AND = " << (a & b) << '\n';
    cout << "OR = " << (a | b) << '\n';
    cout << "XOR = " << (a ^ b) << '\n';
    cout << "Left shift = " << (a << 1) << '\n';
    cout << "Right shift = " << (a >> 1) << '\n';

    return 0;
}
```

---

## 8.14 Common Mistakes

### 8.14.1 Assignment Instead of Comparison

```cpp
if (x = 5)   // Likely mistake
if (x == 5)  // Correct comparison
```

### 8.14.2 Unexpected Integer Division

```cpp
double wrong = 5 / 2;    // 2
double right = 5.0 / 2;  // 2.5
```

### 8.14.3 Wrong Average Expression

```cpp
double wrong = a + b + c / 3.0;
double right = (a + b + c) / 3.0;
```

### 8.14.4 Logical and Bitwise Confusion

- Logical AND: `&&`
- Bitwise AND: `&`
- Logical OR: `||`
- Bitwise OR: `|`

---

## 8.15 Important Differences

### 8.15.1 Assignment vs Equality

| Assignment | Equality |
|---|---|
| `=` | `==` |
| Value store karta hai | Values compare karta hai |

### 8.15.2 Prefix vs Postfix

| Prefix | Postfix |
|---|---|
| Pehle update | Pehle old value use |
| `++x` | `x++` |

### 8.15.3 Implicit vs Explicit Conversion

| Implicit | Explicit |
|---|---|
| Compiler automatic | Programmer requested |
| Convenient | Intent clear |
| Hidden data-loss risk | `static_cast` visible |

---

## 8.16 Chapter Summary

Operators perform operations on operands, and expressions combine operators and values to produce results. C++ provides arithmetic, relational, logical, assignment, increment, decrement, bitwise, conditional and special operators. Integer division removes the fractional part, while the modulus operator returns the remainder. Relational and logical expressions produce Boolean results, and short-circuit evaluation can prevent unnecessary or unsafe operations. Bitwise operators manipulate individual bits. Precedence determines operator priority, associativity resolves operators of equal priority and parentheses make the intended order clear. Implicit conversions happen automatically, while explicit conversions such as static_cast express programmer intent and help control integer division or narrowing.

---

## 8.17 Quick Revision

- Operator operation perform karta hai; operand value hoti hai.
- Arithmetic operators: `+`, `-`, `*`, `/`, `%`.
- Relational operators Boolean result dete hain.
- Logical operators conditions combine karte hain.
- `=` assignment aur `==` comparison hai.
- Prefix pehle update, postfix pehle old value use karta hai.
- Bitwise operators individual bits par work karte hain.
- Conditional operator simple two-way choice deta hai.
- Precedence priority aur associativity grouping direction decide karti hai.
- `static_cast` explicit conversion ke liye use hota hai.

---

## 8.18 Multiple-Choice Questions

1. Remainder ke liye kaunsa operator hai?  
   A. `/`  B. `%`  C. `*`  D. `==`  
   **✅ Answer: B**

2. Integer operands ke saath `7 / 2` ka result kya hai?  
   A. 3  B. 3.5  C. 4  D. 2.5  
   **✅ Answer: A**

3. Equality comparison operator kaunsa hai?  
   A. `=`  B. `==`  C. `+=`  D. `%=`  
   **✅ Answer: B**

4. Logical AND operator kaunsa hai?  
   A. `&`  B. `&&`  C. `!`  D. `^`  
   **✅ Answer: B**

5. `int x=5; int y=x++;` mein y kya hoga?  
   A. 4  B. 5  C. 6  D. Error  
   **✅ Answer: B**

6. `10 + 5 * 2` ka result kya hai?  
   A. 30  B. 20  C. 25  D. 15  
   **✅ Answer: B**

7. Explicit conversion ka example kaunsa hai?  
   A. `static_cast<double>(x)`  B. `x++`  C. `sizeof`  D. `x && y`  
   **✅ Answer: A**

---

## 8.19 Short-Answer Questions

1. Operator, operand aur expression define kijiye.
2. Unary, binary aur ternary operators explain kijiye.
3. Integer division aur modulus samjhaiye.
4. Prefix aur postfix mein difference likhiye.
5. Logical operators ki truth table likhiye.
6. Short-circuit evaluation kya hai?
7. Compound assignment operators explain kijiye.
8. Bitwise operators examples ke saath likhiye.
9. Precedence aur associativity mein difference likhiye.
10. Implicit aur explicit conversion compare kijiye.

---

## 8.20 Long-Answer and Exam Questions

1. C++ operators ko classification aur examples ke saath explain kijiye.
2. Arithmetic, relational aur logical operators ke programs likhiye.
3. Increment/decrement ke prefix aur postfix forms explain kijiye.
4. Bitwise operators binary examples aur program ke saath samjhaiye.
5. Operator precedence aur associativity table ke saath explain kijiye.
6. Expression evaluation solved examples ke saath samjhaiye.
7. Implicit aur explicit type conversions compare kijiye.
8. Arithmetic calculator ka C++ program likhiye.

---

## 8.21 Practice Problems

1. Evaluate: `12 + 4 * 3`
2. Evaluate: `(12 + 4) * 3`
3. Evaluate: `20 / 5 * 2`
4. Predict: `int x=5; int y=++x;`
5. Predict: `int x=5; int y=x++;`
6. Write a program to check divisibility by 5.
7. Write a program to find maximum of two numbers using `?:`.
8. Write a program to demonstrate bitwise AND, OR and XOR.

---

## 8.22 Viva Questions

1. Operator aur operand mein difference kya hai?
2. Modulus operator ka use kya hai?
3. Integer division 5/2 ka result 2 kyun hai?
4. Assignment aur equality mein difference kya hai?
5. Prefix increment kab value update karta hai?
6. Logical AND kab true hota hai?
7. Short-circuit evaluation ka benefit kya hai?
8. Bitwise aur logical AND same hain?
9. Parentheses kyun use karte hain?
10. Explicit cast kab useful hai?

---

<div align="center">

### ✅ Chapter 8 Complete

[⬅️ Previous Chapter](chapter-07-introduction-to-cpp.md) · [📚 Table of Contents](../SUMMARY.md) · **Next: Decision-Making and Loops ➡️**

</div>
