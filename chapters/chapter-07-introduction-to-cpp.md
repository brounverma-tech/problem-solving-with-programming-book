<div align="center">

# 💻 Chapter 7: Introduction to C++

### 🟠 Unit C — Programming Fundamentals Using C++

![Level](https://img.shields.io/badge/Level-Beginner-brightgreen?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Code](https://img.shields.io/badge/Programs-C%2B%2B-purple?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Programming language aur C++ ko define kar सकेंगे.
- Algorithm, source code aur object code samajh सकेंगे.
- C++ program ka basic structure explain kar सकेंगे.
- Program ko compile aur execute karne ke steps samajh सकेंगे.
- Tokens, keywords aur identifiers identify kar सकेंगे.
- Fundamental data types select kar सकेंगे.
- Variables aur constants declare kar सकेंगे.
- `cin` aur `cout` se input/output perform kar सकेंगे.
- Simple C++ programs likh, compile aur debug kar सकेंगे.

---

# 7.1 Introduction to Programming

## 7.1.1 Meaning of Programming

### 📘 English Definition

> Programming is the process of designing, writing, testing and maintaining instructions that a computer can execute to solve a problem.

### 💬 Hinglish Explanation

Programming mein hum problem ko samajhkar computer ke liye step-by-step instructions likhte hain. Yeh instructions programming language mein likhi jati hain.

## 7.1.2 Program

> A program is an ordered collection of instructions written to perform a specific task.

**Examples:**

- Do numbers add karna
- Student percentage calculate karna
- Even/odd check karna
- Bill generate karna

## 7.1.3 Programming Language

Programming language rules, symbols aur words ka formal system hai jisse programs likhe jate hain.

## 7.1.4 Types of Programming Languages

### 7.1.4.1 Machine Language

Binary instructions `0` aur `1` mein hoti hain.

### 7.1.4.2 Assembly Language

Mnemonic codes use karti hai, jaise `ADD`, `MOV` aur `SUB`.

### 7.1.4.3 High-Level Language

Human-readable syntax provide karti hai.

**Examples:** C++, C, Java, Python.

## 7.1.5 Problem-Solving Process

```text
Problem Definition
       ↓
Analysis
       ↓
Algorithm / Flowchart
       ↓
Coding
       ↓
Compilation
       ↓
Testing and Debugging
       ↓
Documentation and Maintenance
```

---

# 7.2 Algorithm

## 7.2.1 Meaning of Algorithm

> An algorithm is a finite sequence of clear and ordered steps used to solve a problem.

## 7.2.2 Characteristics of a Good Algorithm

1. Clearly defined input
2. Clearly defined output
3. Unambiguous steps
4. Finite number of steps
5. Effective and practical operations
6. Correct result

## 7.2.3 Example Algorithm: Add Two Numbers

```text
Step 1: Start
Step 2: Read first number A
Step 3: Read second number B
Step 4: Calculate SUM = A + B
Step 5: Display SUM
Step 6: Stop
```

## 7.2.4 Pseudocode

Pseudocode programming logic ko simple language-like statements mein represent karta hai.

```text
BEGIN
    INPUT A, B
    SUM ← A + B
    OUTPUT SUM
END
```

---

# 7.3 Introduction to C++

## 7.3.1 Meaning of C++

### 📘 English Definition

> C++ is a general-purpose programming language that supports procedural, object-oriented and generic programming.

### 💬 Hinglish Explanation

C++ ek powerful programming language hai jisse small programs se lekar games, system software, applications aur performance-sensitive systems tak develop kiye ja sakte hain.

## 7.3.2 Brief History

- C++ ko Bjarne Stroustrup ne Bell Labs mein develop kiya.
- Early work 1979 ke around “C with Classes” ke रूप में start hua.
- 1983 mein language ka name C++ rakha gaya.
- C++ ne C language features ke saath classes aur object-oriented concepts add kiye.

## 7.3.3 Meaning of ++

C++ mein `++` increment operator hai. Name symbolically C language ke improved/extended form ko indicate karta hai.

## 7.3.4 Features of C++

- General-purpose
- Fast and efficient
- Compiled language
- Procedural programming
- Object-oriented programming
- Generic programming
- Rich standard library
- Portability
- Low-level memory control
- Reusable code support

## 7.3.5 Applications of C++

- Operating systems
- Game engines
- Desktop applications
- Embedded systems
- Browsers
- Database systems
- Compilers
- Robotics
- Scientific applications
- High-performance software

---

# 7.4 Programming Terms

## 7.4.1 Source Code

Programmer ke द्वारा written human-readable code.

## 7.4.2 Source File

C++ source-code file generally `.cpp` extension use karti hai.

## 7.4.3 Compiler

C++ source code ko object/machine-oriented code mein translate karta hai aur compile-time errors identify karta hai.

## 7.4.4 Object Code

Compilation ke baad generated intermediate machine-oriented code.

## 7.4.5 Linker

Object code ko required libraries ke saath combine karke executable banata hai.

## 7.4.6 Executable File

Operating system ke through run hone wali final program file.

## 7.4.7 Debugging

Program errors ko locate aur correct karne ki process.

## 7.4.8 Important Terms Table

| Term | Pronunciation | Meaning |
|---|---|---|
| Source Code | सोर्स कोड | Programmer ka written code |
| Compiler | कम्पाइलर | Code translator |
| Linker | लिंकर | Object files/libraries combine karta hai |
| Executable | एग्ज़िक्यूटेबल | Run hone wali final program file |
| Syntax | सिन्टैक्स | Language ke writing rules |
| Debugging | डीबगिंग | Errors find aur fix karna |
| Library | लाइब्रेरी | Reusable code ka collection |

---

# 7.5 Program Development and Execution

## 7.5.1 Main Stages

```text
Source Code (.cpp)
       ↓
Preprocessor
       ↓
Compiler
       ↓
Object Code
       ↓
Linker + Libraries
       ↓
Executable Program
       ↓
Output
```

## 7.5.2 Edit

Source code editor ya IDE mein program likhna.

## 7.5.3 Preprocess

`#include` jaise preprocessor directives process hote hain.

## 7.5.4 Compile

Syntax aur type-related rules check hote hain aur object code generate hota hai.

## 7.5.5 Link

Required library code aur object files combine hote hain.

## 7.5.6 Run

Executable memory mein load hokar instructions execute karta hai.

---

# 7.6 First C++ Program

## 7.6.1 Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    cout << "Hello, World!";
    return 0;
}
```

## 7.6.2 Output

```text
Hello, World!
```

## 7.6.3 Line-by-Line Explanation

### 7.6.3.1 `#include <iostream>`

Standard input/output stream declarations program mein available karta hai.

### 7.6.3.2 `using namespace std;`

Standard-library names, jaise `cout` aur `cin`, ko `std::` prefix ke bina use karne deta hai.

> Larger programs mein explicit `std::cout` aur `std::cin` prefer kiye ja sakte hain.

### 7.6.3.3 `int main()`

Program execution `main` function se start hoti hai. `int` batata hai ki function integer status return karta hai.

### 7.6.3.4 Curly Braces

`{` aur `}` function/block boundaries define karte hain.

### 7.6.3.5 `cout`

Standard output stream. Screen/console par output display karta hai.

### 7.6.3.6 Insertion Operator

`<<` value ko output stream mein insert karta hai.

### 7.6.3.7 Semicolon

`;` statement ka end indicate karta hai.

### 7.6.3.8 `return 0;`

Operating system ko successful completion status return karta hai.

---

# 7.7 Comments in C++

## 7.7.1 Single-Line Comment

```cpp
// This is a single-line comment
```

## 7.7.2 Multi-Line Comment

```cpp
/*
This is a
multi-line comment
*/
```

## 7.7.3 Purpose of Comments

- Code explain karna
- Program readability improve karna
- Important logic document karna
- Maintenance आसान banana

> Comments compiler द्वारा executable instructions mein convert nahi hote.

---

# 7.8 C++ Tokens

## 7.8.1 Meaning

> Tokens are the smallest meaningful units of a C++ program.

## 7.8.2 Types of Tokens

- Keywords
- Identifiers
- Literals/constants
- Operators
- Punctuators/separators

### Example

```cpp
int total = 50;
```

| Token | Type |
|---|---|
| `int` | Keyword |
| `total` | Identifier |
| `=` | Operator |
| `50` | Integer literal |
| `;` | Punctuator |

---

# 7.9 Keywords

## 7.9.1 Meaning

Keywords reserved words hote hain jinka language mein predefined meaning hota hai. Inhe identifiers ke रूप में use nahi kar sakte.

## 7.9.2 Examples

```text
int, char, float, double, if, else, switch,
case, for, while, do, break, continue, return,
const, class, public, private, void, bool
```

### Invalid Example

```cpp
int return = 10;  // Error: return is a keyword
```

---

# 7.10 Identifiers

## 7.10.1 Meaning of Identifier

> An identifier is a user-defined name given to a variable, function, class or other program element.

## 7.10.2 Rules for Identifiers

1. Letters, digits aur underscore use ho sakte hain.
2. First character digit nahi ho sakta.
3. Spaces allowed nahi hain.
4. Special symbols such as `@`, `#`, `%` allowed nahi.
5. Keyword ko identifier nahi bana sakte.
6. C++ case-sensitive hai.
7. Standard reserved names avoid karne chahiye.

## 7.10.3 Valid Identifiers

```text
age
studentName
total_marks
number2
_marks
```

## 7.10.4 Invalid Identifiers

| Identifier | Reason |
|---|---|
| `2number` | Digit se start |
| `student name` | Space present |
| `total-marks` | Hyphen used |
| `float` | Keyword |
| `price@` | Invalid symbol |

## 7.10.5 Case Sensitivity

```cpp
int marks = 80;
int Marks = 90;
```

`marks` aur `Marks` two different identifiers hain.

## 7.10.6 Naming Best Practices

- Meaningful names use karein.
- Variables ke liye `studentAge`, `totalMarks` jaise names.
- Unclear one-letter names unnecessary use na karein.
- Consistent naming style follow karein.
- Standard-library names se conflict avoid karein.

---

# 7.11 Data Types

## 7.11.1 Meaning of Data Type

> A data type specifies the kind of value a variable can store and the operations that can be performed on it.

### 💬 Hinglish Explanation

Data type compiler ko batata hai ki variable mein kis type ka data store hoga, jaise integer, decimal, character ya true/false.

## 7.11.2 Main Categories

```text
C++ Data Types
│
├── Fundamental
│   ├── Integer
│   ├── Floating-point
│   ├── Character
│   ├── Boolean
│   └── Void
│
├── Derived
│   ├── Array
│   ├── Pointer
│   ├── Reference
│   └── Function
│
└── User-Defined
    ├── Class
    ├── Structure
    ├── Union
    └── Enumeration
```

---

# 7.12 Fundamental Data Types

## 7.12.1 Integer Types

Whole numbers store karte hain.

```cpp
int age = 20;
long population = 5000000;
long long largeNumber = 9000000000LL;
```

Integer modifiers:

- `signed`
- `unsigned`
- `short`
- `long`

## 7.12.2 Floating-Point Types

Decimal/real numbers store karte hain.

```cpp
float temperature = 36.5f;
double percentage = 87.625;
long double preciseValue = 3.1415926535L;
```

## 7.12.3 Character Type

Single character store karta hai.

```cpp
char grade = 'A';
```

Single quotes character literal ke liye use hoti hain.

## 7.12.4 Boolean Type

`true` ya `false` store karta hai.

```cpp
bool isPassed = true;
```

## 7.12.5 Void Type

“no value” indicate karta hai. Commonly function return type ke रूप में.

```cpp
void showMessage()
{
    cout << "Welcome";
}
```

## 7.12.6 Typical Data-Type Table

| Data Type | Stores | Example |
|---|---|---|
| `int` | Whole number | `25` |
| `float` | Decimal, single precision | `3.5f` |
| `double` | Decimal, higher precision | `3.14159` |
| `char` | Single character | `'A'` |
| `bool` | True/false | `true` |
| `void` | No value | Function return |

> ⚠️ Exact size and range implementation/platform par depend kar sakte hain. `sizeof` operator se size check kiya ja sakta hai.

---

# 7.13 Checking Data-Type Size

## 7.13.1 Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    cout << "int: " << sizeof(int) << " bytes\n";
    cout << "float: " << sizeof(float) << " bytes\n";
    cout << "double: " << sizeof(double) << " bytes\n";
    cout << "char: " << sizeof(char) << " byte\n";
    cout << "bool: " << sizeof(bool) << " byte\n";

    return 0;
}
```

## 7.13.2 Explanation

`sizeof(type)` selected implementation mein type ki size bytes mein return karta hai.

---

# 7.14 Variables

## 7.14.1 Meaning of Variable

> A variable is a named memory location whose stored value can change during program execution.

## 7.14.2 Declaration

```cpp
int age;
double salary;
char grade;
```

## 7.14.3 Initialization

Declaration ke time initial value assign karna.

```cpp
int age = 20;
double price = 99.50;
char grade = 'A';
```

## 7.14.4 Assignment

Already declared variable ko value dena/change karna.

```cpp
int marks;
marks = 75;
marks = 82;
```

## 7.14.5 Multiple Variables

```cpp
int a = 10, b = 20, sum = 0;
```

Readable code ke liye separate declarations bhi use ki ja sakti hain.

## 7.14.6 Modern Initialization Forms

```cpp
int a = 10;    // Copy initialization
int b(20);     // Direct initialization
int c{30};     // List initialization
```

## 7.14.7 Uninitialized Variables

Local fundamental variable ko initial value diye bina read karna unsafe/undefined behavior cause kar sakta hai.

```cpp
int total = 0;  // Good practice
```

---

# 7.15 Constants

## 7.15.1 Meaning of Constant

> A constant is a value that does not change during program execution.

## 7.15.2 Literal Constants

Code mein directly written fixed values.

```cpp
10
3.14
'A'
"Hello"
true
```

## 7.15.3 Symbolic Constant with `const`

```cpp
const double PI = 3.1415926535;
const int MAX_STUDENTS = 100;
```

Assigned value later change nahi ki ja sakti.

## 7.15.4 Compile-Time Constant with `constexpr`

```cpp
constexpr int DAYS_IN_WEEK = 7;
```

`constexpr` compile-time constant expression represent kar sakta hai.

## 7.15.5 Variable and Constant Difference

| Variable | Constant |
|---|---|
| Value change ho sakti hai | Value fixed hoti hai |
| Normal declaration | `const`/`constexpr` |
| Example: current score | Example: PI |

---

# 7.16 Literals

## 7.16.1 Integer Literals

```cpp
25       // Decimal
0b1010   // Binary in modern C++
075      // Octal
0x2A     // Hexadecimal
```

## 7.16.2 Floating-Point Literals

```cpp
3.14
2.5f
6.02e23
```

## 7.16.3 Character Literals

```cpp
'A'
'7'
'\n'
```

## 7.16.4 String Literals

```cpp
"Hello"
"C++ Programming"
```

## 7.16.5 Boolean Literals

```cpp
true
false
```

---

# 7.17 Escape Sequences

Special characters ko backslash ke saath represent kiya jata hai.

| Escape Sequence | Meaning |
|---|---|
| `\n` | New line |
| `\t` | Horizontal tab |
| `\\` | Backslash |
| `\"` | Double quote |
| `\'` | Single quote |
| `\0` | Null character |

## 7.17.1 Example

```cpp
cout << "Name:\tBroun\nCourse:\tBCA";
```

## 7.17.2 Output

```text
Name:   Broun
Course: BCA
```

---

# 7.18 Standard Output Using cout

## 7.18.1 Basic Output

```cpp
cout << "Welcome to C++";
```

## 7.18.2 Multiple Values

```cpp
int age = 20;
cout << "Age = " << age;
```

## 7.18.3 New Line

```cpp
cout << "First line\n";
cout << "Second line" << endl;
```

## 7.18.4 `\n` vs `endl`

- `\n` new-line character insert karta hai.
- `endl` new line insert ke saath stream flush bhi karta hai.
- Normal output mein `\n` often sufficient aur efficient hota hai.

---

# 7.19 Standard Input Using cin

## 7.19.1 Basic Input

```cpp
int age;
cin >> age;
```

## 7.19.2 Extraction Operator

`>>` input stream se value extract karke variable mein store karta hai.

## 7.19.3 Multiple Inputs

```cpp
int a, b;
cin >> a >> b;
```

## 7.19.4 Prompt with Input

```cpp
int marks;

cout << "Enter marks: ";
cin >> marks;

cout << "You entered: " << marks;
```

---

# 7.20 String Input

## 7.20.1 Word Input with cin

```cpp
string name;
cin >> name;
```

Yeh whitespace tak single word read karta hai.

## 7.20.2 Full-Line Input with getline

```cpp
#include <iostream>
#include <string>
using namespace std;

int main()
{
    string fullName;

    cout << "Enter full name: ";
    getline(cin, fullName);

    cout << "Name: " << fullName;
    return 0;
}
```

## 7.20.3 cin and getline Issue

Formatted input ke baad leftover newline ko handle karna pad sakta hai.

```cpp
#include <limits>

// After cin >> value:
cin.ignore(numeric_limits<streamsize>::max(), '\n');
getline(cin, fullName);
```

---

# 7.21 Program: Add Two Numbers

## 7.21.1 Source Code

```cpp
#include <iostream>
using namespace std;

int main()
{
    int firstNumber;
    int secondNumber;
    int sum;

    cout << "Enter first number: ";
    cin >> firstNumber;

    cout << "Enter second number: ";
    cin >> secondNumber;

    sum = firstNumber + secondNumber;

    cout << "Sum = " << sum << '\n';
    return 0;
}
```

## 7.21.2 Sample Output

```text
Enter first number: 12
Enter second number: 8
Sum = 20
```

## 7.21.3 Dry Run

| Step | firstNumber | secondNumber | sum |
|---|---:|---:|---:|
| Input 1 | 12 | — | — |
| Input 2 | 12 | 8 | — |
| Calculation | 12 | 8 | 20 |
| Output | 12 | 8 | 20 |

---

# 7.22 Program: Student Information

## 7.22.1 Source Code

```cpp
#include <iostream>
#include <string>
using namespace std;

int main()
{
    string name;
    int age;
    double percentage;

    cout << "Enter name: ";
    getline(cin, name);

    cout << "Enter age: ";
    cin >> age;

    cout << "Enter percentage: ";
    cin >> percentage;

    cout << "\n--- Student Details ---\n";
    cout << "Name: " << name << '\n';
    cout << "Age: " << age << '\n';
    cout << "Percentage: " << percentage << "%\n";

    return 0;
}
```

## 7.22.2 Sample Output

```text
Enter name: Broun Verma
Enter age: 20
Enter percentage: 82.5

--- Student Details ---
Name: Broun Verma
Age: 20
Percentage: 82.5%
```

---

# 7.23 Program: Area of a Circle

## 7.23.1 Source Code

```cpp
#include <iostream>
using namespace std;

int main()
{
    constexpr double PI = 3.1415926535;
    double radius;
    double area;

    cout << "Enter radius: ";
    cin >> radius;

    area = PI * radius * radius;

    cout << "Area = " << area << '\n';
    return 0;
}
```

## 7.23.2 Sample Output

```text
Enter radius: 5
Area = 78.5398
```

---

# 7.24 Type Safety and Input Considerations

## 7.24.1 Matching Type and Value

- Age ke liye integer
- Price ke liye double
- Grade ke liye char
- Status ke liye bool
- Name ke liye string

## 7.24.2 Range

Aisa data type choose karein jo required range ko safely store kar sake.

## 7.24.3 Precision

Scientific ya financial calculations mein floating-point behavior aur required precision carefully consider karein.

## 7.24.4 Input Failure

User wrong type enter kare to `cin` fail state mein ja sakta hai. Advanced input validation later chapters mein use hogi.

---

# 7.25 Types of Errors

## 7.25.1 Syntax Error

Language grammar/rules violate hote hain.

```cpp
cout << "Hello"  // Missing semicolon
```

## 7.25.2 Compile-Time Error

Compiler program translate karte time error detect karta hai.

```cpp
cout << unknownVariable;
```

## 7.25.3 Linker Error

Required function/object definition linking ke time nahi milti.

## 7.25.4 Runtime Error

Program run hote time problem hoti hai.

**Examples:** Invalid memory access, certain invalid operations or unavailable resources.

## 7.25.5 Logical Error

Program run hota hai, lekin result incorrect hota hai.

```cpp
area = 2 * PI * radius;  // This is circumference, not area
```

## 7.25.6 Error Comparison

| Error | Detected When | Example |
|---|---|---|
| Syntax/Compile | Compilation | Missing `;` |
| Linker | Linking | Missing definition |
| Runtime | Execution | Invalid operation |
| Logical | Output/testing | Wrong formula |

---

# 7.26 Coding Best Practices

1. Meaningful identifiers use karein.
2. Variables initialize karein.
3. Consistent indentation rakhein.
4. One statement per line prefer karein.
5. Complex logic par useful comments likhein.
6. Constants ke liye `const`/`constexpr` use karein.
7. Input prompts clear rakhein.
8. Program ko small steps mein test karein.
9. Compiler warnings carefully read karein.
10. Code formatting consistent rakhein.

---

# 7.27 Important Differences

## 7.27.1 Compiler vs Linker

| Compiler | Linker |
|---|---|
| Source code translate karta hai | Object files/libraries combine karta hai |
| Syntax/type errors detect karta hai | Missing definitions resolve/check karta hai |
| Object code produce karta hai | Executable produce karta hai |

## 7.27.2 Keyword vs Identifier

| Keyword | Identifier |
|---|---|
| Predefined reserved word | User-defined name |
| Fixed meaning | Programmer-selected meaning |
| Variable name nahi ho sakta | Variable/function/class name ho sakta |
| Example: `int` | Example: `studentAge` |

## 7.27.3 Variable vs Constant

| Variable | Constant |
|---|---|
| Value change ho sakti hai | Value change nahi hoti |
| `int score` | `const int MAX` |
| Mutable data | Fixed rule/value |

## 7.27.4 cin vs cout

| cin | cout |
|---|---|
| Standard input | Standard output |
| `>>` operator | `<<` operator |
| Keyboard/stream se data | Console/stream par result |

---

# 7.28 Chapter Summary

C++ is a compiled, general-purpose programming language that supports procedural, object-oriented and generic programming. Program development begins with problem analysis and an algorithm, followed by coding, compilation, linking, execution, testing and debugging. A C++ program starts from the main function and commonly uses the iostream library for console input and output. Tokens include keywords, identifiers, literals, operators and punctuators. Data types define the kind of values stored in memory, variables represent changeable named locations and constants represent fixed values. The standard streams cin and cout receive input and display output. Correct syntax, meaningful identifiers, proper initialization and careful type selection make programs clearer and safer.

---

# 7.29 Quick Revision

- Program instructions ka ordered set hai.
- Algorithm finite step-by-step solution hai.
- C++ compiled general-purpose language hai.
- Execution `main()` function se start hoti hai.
- `#include <iostream>` input/output declarations provide karta hai.
- Tokens program ki smallest meaningful units hain.
- Keywords reserved words aur identifiers user-defined names hain.
- Data type stored value ka kind define karta hai.
- Variable ki value change ho sakti hai; constant fixed hota hai.
- `cin >>` input aur `cout <<` output ke liye hain.
- Syntax, linker, runtime aur logical errors different stages par hote hain.

---

# 7.30 Important Abbreviations

| Abbreviation | Full Form |
|---|---|
| IDE | Integrated Development Environment |
| CPU | Central Processing Unit |
| I/O | Input/Output |
| OOP | Object-Oriented Programming |
| GNU | GNU's Not Unix |
| GCC | GNU Compiler Collection |
| STL | Standard Template Library |

---

# 7.31 Multiple-Choice Questions

### 1. C++ ko kisne develop kiya?

A. Charles Babbage  
B. Bjarne Stroustrup  
C. Tim Berners-Lee  
D. Dennis Ritchie only  

**✅ Answer:** B

### 2. C++ program execution kahan se start hoti hai?

A. `include`  
B. `main()`  
C. `cout`  
D. Comment  

**✅ Answer:** B

### 3. Standard console output object kya hai?

A. `cin`  
B. `cout`  
C. `main`  
D. `int`  

**✅ Answer:** B

### 4. User-defined name ko kya kehte hain?

A. Keyword  
B. Identifier  
C. Compiler  
D. Comment  

**✅ Answer:** B

### 5. Kaunsa valid identifier hai?

A. `2marks`  
B. `total-marks`  
C. `totalMarks`  
D. `return`  

**✅ Answer:** C

### 6. Decimal value ke liye suitable type kaunsa hai?

A. `double`  
B. `void`  
C. Comment  
D. Namespace only  

**✅ Answer:** A

### 7. Fixed value ke liye kya use hota hai?

A. `const`  
B. `cin`  
C. `return` only  
D. `include` only  

**✅ Answer:** A

### 8. Extraction operator kaunsa hai?

A. `<<`  
B. `>>`  
C. `++`  
D. `//`  

**✅ Answer:** B

### 9. Program run ho lekin wrong result de to kaunsa error hai?

A. Logical error  
B. Syntax error only  
C. Comment error  
D. Keyword error  

**✅ Answer:** A

### 10. Full line string input ke liye kya use hota hai?

A. `getline`  
B. `sizeof`  
C. `return`  
D. `const`  

**✅ Answer:** A

---

# 7.32 Short-Answer Questions

1. Programming ko define kijiye.
2. Algorithm kya hai?
3. C++ ki four features likhiye.
4. Source code aur executable kya hain?
5. Compiler aur linker ka role kya hai?
6. First C++ program ka structure explain kijiye.
7. C++ tokens kya hain?
8. Keyword aur identifier mein difference likhiye.
9. Valid identifier ke rules likhiye.
10. Data type kya hai?
11. Fundamental data types examples ke saath likhiye.
12. Variable declaration aur initialization mein difference likhiye.
13. Constant kya hai?
14. `cin` aur `cout` explain kijiye.
15. Syntax aur logical error mein difference likhiye.

---

# 7.33 Long-Answer and Exam Questions

1. Program-development cycle ko diagram ke saath explain kijiye.
2. C++ ka introduction, history, features aur applications explain kijiye.
3. First C++ program ko line-by-line describe kijiye.
4. C++ tokens ko types aur examples ke saath explain kijiye.
5. Identifier rules aur naming best practices samjhaiye.
6. C++ data types ko classification diagram ke saath explain kijiye.
7. Variables, constants aur literals compare kijiye.
8. Standard input/output ko programs ke saath explain kijiye.
9. Different program errors examples ke saath describe kijiye.
10. Two numbers ka sum aur circle area calculate karne ke C++ programs likhiye.

---

# 7.34 Practical Programs

1. Apna name, course aur city display kijiye.
2. Two integers input karke sum display kijiye.
3. Length aur width input karke rectangle area calculate kijiye.
4. Radius input karke circle area calculate kijiye.
5. Celsius value input karke Fahrenheit calculate kijiye.
6. Student ke three subject marks input karke total aur average display kijiye.
7. Principal, rate aur time input karke simple interest calculate kijiye.
8. `sizeof` se fundamental types ki size display kijiye.

---

# 7.35 Viva Questions

1. C++ compiled language ka kya meaning hai?
2. `main()` function kyun required hai?
3. `#include <iostream>` kya karta hai?
4. Semicolon ka role kya hai?
5. C++ case-sensitive hai?
6. Identifier digit se start ho sakta hai?
7. `char` aur `string` mein difference kya hai?
8. `const` kyun use karte hain?
9. `cin >> name` full name kyun nahi read karta?
10. Logical error compiler kyun nahi pakad sakta?

---

# 7.36 Answers to Selected Viva Questions

1. Source code machine-oriented executable form mein translate hota hai.
2. Program execution ka standard entry point `main()` hai.
3. Standard stream input/output declarations available karta hai.
4. Semicolon C++ statement ka end mark karta hai.
5. Haan, `age` aur `Age` different identifiers hain.
6. Nahi, identifier ka first character digit nahi ho sakta.
7. `char` single character aur `string` characters ka sequence store karta hai.
8. Fixed value ko accidental modification se protect karne ke liye.
9. Formatted extraction whitespace par stop karti hai.
10. Logical error syntax-correct hota hai; problem program logic/formula mein hoti hai.

---

<div align="center">

## ✅ Chapter 7 Complete

[⬅️ Previous Chapter](chapter-06-number-systems-and-computer-codes.md) · [📚 Table of Contents](../SUMMARY.md) · **Next: Operators and Expressions ➡️**

</div>
