# 📘 Appendix B: C++ Syntax Quick Reference

![C++](https://img.shields.io/badge/C%2B%2B-Syntax_Reference-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner_to_Advanced-success?style=for-the-badge)

> C++ ke important syntax ka quick revision guide. Har topic ke niche uska syntax aur chhota example diya gaya hai.

---

## B.1 Basic Program Structure

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!";
    return 0;
}
```

| Part | Purpose |
|---|---|
| `#include <iostream>` | Input-output library include karta hai |
| `using namespace std;` | Standard names ko directly use karne deta hai |
| `int main()` | Program execution yahin se start hota hai |
| `return 0;` | Program successfully complete hone ka signal |

---

## B.2 Comments

### B.2.1 Single-Line Comment

```cpp
// This is a single-line comment
```

### B.2.2 Multi-Line Comment

```cpp
/* This is a
   multi-line comment */
```

---

## B.3 Variables and Data Types

### B.3.1 Variable Declaration

```cpp
dataType variableName;
dataType variableName = value;
```

```cpp
int age = 20;
float marks = 85.5f;
double price = 1250.75;
char grade = 'A';
bool passed = true;
string name = "Aman";
```

### B.3.2 Constants

```cpp
const double PI = 3.14159;
```

---

## B.4 Input and Output

### B.4.1 Output Using `cout`

```cpp
cout << "Welcome";
cout << "Age: " << age << endl;
```

### B.4.2 Input Using `cin`

```cpp
int number;
cin >> number;
```

### B.4.3 Reading a Complete Line

```cpp
string fullName;
getline(cin, fullName);
```

> `cin` ke baad `getline()` use karte samay zarurat ho to `cin.ignore()` lagayein.

---

## B.5 Operators

| Category | Operators |
|---|---|
| Arithmetic | `+`, `-`, `*`, `/`, `%` |
| Relational | `==`, `!=`, `>`, `<`, `>=`, `<=` |
| Logical | `&&`, `\|\|`, `!` |
| Assignment | `=`, `+=`, `-=`, `*=`, `/=`, `%=` |
| Increment/Decrement | `++`, `--` |
| Conditional | `?:` |

```cpp
int sum = a + b;
bool result = (a > b && a > 0);
int maximum = (a > b) ? a : b;
```

---

## B.6 Decision-Making Statements

### B.6.1 `if` Statement

```cpp
if (condition) {
    // statements
}
```

### B.6.2 `if-else` Statement

```cpp
if (marks >= 40) {
    cout << "Pass";
} else {
    cout << "Fail";
}
```

### B.6.3 `else-if` Ladder

```cpp
if (marks >= 75) {
    cout << "Distinction";
} else if (marks >= 60) {
    cout << "First Division";
} else if (marks >= 40) {
    cout << "Pass";
} else {
    cout << "Fail";
}
```

### B.6.4 `switch` Statement

```cpp
switch (choice) {
    case 1:
        cout << "Add";
        break;
    case 2:
        cout << "Delete";
        break;
    default:
        cout << "Invalid choice";
}
```

---

## B.7 Loops

### B.7.1 `for` Loop

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << " ";
}
```

### B.7.2 `while` Loop

```cpp
int i = 1;
while (i <= 5) {
    cout << i << " ";
    i++;
}
```

### B.7.3 `do-while` Loop

```cpp
int i = 1;
do {
    cout << i << " ";
    i++;
} while (i <= 5);
```

### B.7.4 Loop-Control Statements

```cpp
break;     // loop ko turant stop karta hai
continue;  // current iteration skip karta hai
```

---

## B.8 Functions

### B.8.1 Function Declaration and Definition

```cpp
returnType functionName(parameterList);

returnType functionName(parameterList) {
    // statements
    return value;
}
```

### B.8.2 Function Example

```cpp
int add(int a, int b) {
    return a + b;
}

int main() {
    cout << add(10, 20);
    return 0;
}
```

### B.8.3 Pass by Reference

```cpp
void increase(int &number) {
    number++;
}
```

### B.8.4 Default Argument

```cpp
int multiply(int a, int b = 2) {
    return a * b;
}
```

---

## B.9 Arrays

### B.9.1 One-Dimensional Array

```cpp
int marks[5] = {80, 75, 90, 65, 88};

for (int i = 0; i < 5; i++) {
    cout << marks[i] << " ";
}
```

### B.9.2 Two-Dimensional Array

```cpp
int matrix[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```

### B.9.3 Range-Based Loop

```cpp
for (int value : marks) {
    cout << value << " ";
}
```

---

## B.10 Strings

```cpp
#include <string>

string text = "Programming";
cout << text.length();
cout << text[0];
text = text + " in C++";
```

| Operation | Syntax |
|---|---|
| Length | `text.length()` |
| Character access | `text[index]` |
| Join strings | `text1 + text2` |
| Compare | `text1 == text2` |
| Substring | `text.substr(start, length)` |

---

## B.11 Pointers

### B.11.1 Pointer Declaration

```cpp
int number = 10;
int *ptr = &number;
```

### B.11.2 Address and Dereference Operators

```cpp
cout << &number;  // address of number
cout << ptr;      // stored address
cout << *ptr;     // value at stored address
```

### B.11.3 Null Pointer

```cpp
int *ptr = nullptr;
```

### B.11.4 Dynamic Memory

```cpp
int *ptr = new int;
*ptr = 50;
delete ptr;
ptr = nullptr;
```

```cpp
int *arr = new int[5];
delete[] arr;
arr = nullptr;
```

---

## B.12 Structures

```cpp
struct Student {
    int rollNumber;
    string name;
    float marks;
};

Student student1 = {101, "Aman", 88.5f};
cout << student1.name;
```

---

## B.13 Classes and Objects

```cpp
class Student {
private:
    int marks;

public:
    void setMarks(int value) {
        marks = value;
    }

    int getMarks() {
        return marks;
    }
};

Student student1;
student1.setMarks(90);
cout << student1.getMarks();
```

---

## B.14 File Handling

### B.14.1 Writing to a File

```cpp
#include <fstream>

ofstream outputFile("data.txt");
outputFile << "Hello File";
outputFile.close();
```

### B.14.2 Reading from a File

```cpp
ifstream inputFile("data.txt");
string line;

while (getline(inputFile, line)) {
    cout << line << endl;
}

inputFile.close();
```

---

## B.15 Common Escape Sequences

| Escape Sequence | Use |
|---|---|
| `\n` | New line |
| `\t` | Horizontal tab |
| `\\` | Backslash print karna |
| `\"` | Double quotation mark print karna |
| `\'` | Single quotation mark print karna |

---

## B.16 Common Header Files

| Header File | Main Use |
|---|---|
| `<iostream>` | `cin`, `cout` |
| `<string>` | `string` operations |
| `<cmath>` | Mathematical functions |
| `<iomanip>` | Output formatting |
| `<fstream>` | File handling |
| `<cstdlib>` | General utility functions |

---

## B.17 Quick Revision Checklist

- Har C++ statement ke end me generally semicolon `;` lagta hai.
- Code blocks curly braces `{ }` ke andar likhe jaate hain.
- Array indexing `0` se start hoti hai.
- Assignment ke liye `=` aur comparison ke liye `==` use hota hai.
- Integer division decimal part hata deti hai.
- Pointer address store karta hai; `*` dereference aur `&` address operator hai.
- Dynamic memory ko `delete` ya `delete[]` se release karna chahiye.
- C++ case-sensitive language hai: `total` aur `Total` alag identifiers hain.

---

## 📝 One-Line Summary

> **C++ syntax ko yaad karne ka best tarika hai: syntax samjho, chhota program likho, compile karo aur output verify karo.**

---

[⬅️ Appendix A](appendix-a-important-terms.md) | [📚 Table of Contents](../SUMMARY.md)
