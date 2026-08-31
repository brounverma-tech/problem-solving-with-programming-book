<div align="center">

# 🧱 Chapter 10: Functions and Structured Programming

### 🔴 Unit D — Functions, Arrays and Pointers in C++

![Level](https://img.shields.io/badge/Level-Intermediate-orange?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Code](https://img.shields.io/badge/Programs-C%2B%2B-purple?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Structured programming ke principles samajh sakenge.
- Function declaration, definition aur call explain kar sakenge.
- Library aur user-defined functions use kar sakenge.
- Parameters aur arguments mein difference bata sakenge.
- Call by value aur call by reference apply kar sakenge.
- Return values aur function overloading samajh sakenge.
- Local/global scope aur storage classes explain kar sakenge.
- Arrays ko functions mein pass kar sakenge.
- Recursive functions likh aur trace kar sakenge.

---

## 10.1 Introduction to Structured Programming

### 10.1.1 Meaning of Structured Programming

> Structured programming is a programming approach that organizes a program into clear blocks, control structures and reusable modules.

**Hinglish:** Structured programming mein large problem ko small aur manageable parts mein divide kiya jata hai. Har part ka clear purpose hota hai.

### 10.1.2 Main Control Structures

1. Sequence
2. Selection
3. Repetition

### 10.1.3 Modular Programming

Program ko independent, reusable functions/modules mein divide karna modular programming hai.

```text
Large Problem
│
├── Input Function
├── Processing Function
├── Validation Function
└── Output Function
```

### 10.1.4 Advantages

- Program easy to understand hota hai.
- Testing aur debugging easier hoti hai.
- Code reuse possible hota hai.
- Team work aur maintenance improve hoti hai.
- Repetition aur complexity reduce hoti hai.

---

## 10.2 Introduction to Functions

### 10.2.1 Meaning of Function

> A function is a named, reusable block of code designed to perform a specific task.

### 10.2.2 Need for Functions

- Large program ko smaller parts mein divide karna
- Repeated code avoid karna
- Readability improve karna
- Testing aur debugging simplify karna
- Code reuse support karna

### 10.2.3 Types of Functions

```text
Functions
│
├── Standard/Library Functions
└── User-Defined Functions
```

---

## 10.3 Function Declaration, Definition and Call

### 10.3.1 Function Declaration

Compiler ko function ka name, return type aur parameter types batata hai. Isse function prototype bhi kehte hain.

#### Syntax

```cpp
returnType functionName(parameterTypes);
```

#### Example

```cpp
int add(int, int);
```

### 10.3.2 Function Definition

Function ka actual code/body provide karti hai.

#### Syntax

```cpp
returnType functionName(parameters)
{
    statements;
    return value;
}
```

### 10.3.3 Function Call

Function ko execute karne ke liye name aur arguments use hote hain.

```cpp
int result = add(10, 20);
```

#### Complete Program

```cpp
#include <iostream>
using namespace std;

int add(int, int);

int main()
{
    int result = add(10, 20);
    cout << "Sum = " << result;
    return 0;
}

int add(int first, int second)
{
    return first + second;
}
```

---

## 10.4 Function Components

### 10.4.1 Function Name

Function ko identify karne wala valid identifier.

### 10.4.2 Return Type

Function caller ko kis type ki value return karega.

### 10.4.3 Parameters

Function definition/declaration mein input receive karne wale variables.

### 10.4.4 Function Body

Curly braces ke andar executable statements.

### 10.4.5 Return Statement

Function se value aur control caller ko return karta hai.

### 10.4.6 Function Signature

Function name aur parameter-type list function identity mein important hote hain. Return type alone overloading distinguish nahi karta.

---

## 10.5 Parameters and Arguments

### 10.5.1 Formal Parameters

Function definition mein declared variables.

```cpp
int add(int first, int second)
```

`first` aur `second` formal parameters hain.

### 10.5.2 Actual Arguments

Function call ke time supplied values/expressions.

```cpp
add(10, 20);
```

`10` aur `20` actual arguments hain.

### 10.5.3 Difference

| Parameters | Arguments |
|---|---|
| Function declaration/definition mein | Function call mein |
| Input receive karne wale variables | Supplied values/expressions |
| Example: `int x` | Example: `25` |

---

## 10.6 Categories of User-Defined Functions

### 10.6.1 No Arguments and No Return Value

```cpp
void greet()
{
    cout << "Welcome to C++";
}
```

### 10.6.2 Arguments and No Return Value

```cpp
void printSum(int a, int b)
{
    cout << a + b;
}
```

### 10.6.3 No Arguments but Return Value

```cpp
int readNumber()
{
    int value;
    cin >> value;
    return value;
}
```

### 10.6.4 Arguments and Return Value

```cpp
int maximum(int a, int b)
{
    return (a > b) ? a : b;
}
```

---

## 10.7 Call by Value

### 10.7.1 Meaning

> In call by value, a function receives copies of the argument values.

Original variable directly modify nahi hota.

#### Program

```cpp
#include <iostream>
using namespace std;

void changeValue(int number)
{
    number = 100;
}

int main()
{
    int value = 10;
    changeValue(value);

    cout << value;  // 10
    return 0;
}
```

### 10.7.2 Advantages

- Original data protected rehta hai.
- Function side effects reduce hote hain.
- Small simple types ke liye easy hai.

### 10.7.3 Limitation

Large objects copy karna costly ho sakta hai, aur caller value modify nahi hoti.

---

## 10.8 Call by Reference

### 10.8.1 Meaning

> In call by reference, a reference parameter acts as another name for the original argument.

Function original variable modify kar sakta hai.

#### Program: Swap Two Numbers

```cpp
#include <iostream>
using namespace std;

void swapNumbers(int& first, int& second)
{
    int temporary = first;
    first = second;
    second = temporary;
}

int main()
{
    int a = 10;
    int b = 20;

    swapNumbers(a, b);

    cout << "a = " << a << '\n';
    cout << "b = " << b << '\n';
    return 0;
}
```

#### Output

```text
a = 20
b = 10
```

### 10.8.2 Const Reference

Large object ko copy kiye bina read-only access dene ke liye const reference use ho sakta hai.

```cpp
void display(const string& text)
{
    cout << text;
}
```

### 10.8.3 Value vs Reference

| Call by Value | Call by Reference |
|---|---|
| Copy receive hoti hai | Original ka reference |
| Original unchanged | Original modify ho sakta hai |
| Copy cost possible | Copy avoid ho sakti hai |
| Normal parameter | `&` reference parameter |

---

## 10.9 Returning Values

### 10.9.1 Single Return Value

```cpp
double square(double number)
{
    return number * number;
}
```

### 10.9.2 Early Return

```cpp
bool isPositive(int number)
{
    if (number <= 0)
        return false;

    return true;
}
```

### 10.9.3 void Function

`void` function value return nahi karta.

```cpp
void showMessage()
{
    cout << "Done";
}
```

---

## 10.10 Default Arguments

### 10.10.1 Meaning

Parameter ke liye default value define ki ja sakti hai. Argument omit hone par default use hota hai.

```cpp
double calculatePrice(double amount, double taxRate = 0.18)
{
    return amount + amount * taxRate;
}
```

```cpp
calculatePrice(1000);       // Default taxRate
calculatePrice(1000, 0.05); // Supplied taxRate
```

### 10.10.2 Rules

- Default arguments usually declaration mein specify karein.
- Rightmost parameters se defaults start hone chahiye.
- Same default repeatedly define na karein.

---

## 10.11 Function Overloading

### 10.11.1 Meaning

> Function overloading allows multiple functions to have the same name with different parameter lists.

#### Example

```cpp
int add(int a, int b)
{
    return a + b;
}

double add(double a, double b)
{
    return a + b;
}

int add(int a, int b, int c)
{
    return a + b + c;
}
```

### 10.11.2 Overloading Rules

- Parameter count different ho sakta hai.
- Parameter types different ho sakte hain.
- Parameter order different ho sakta hai.
- Return type alone overload create nahi karta.

---

## 10.12 Standard Library Functions

### 10.12.1 Meaning

Standard library reusable ready-made functions aur classes provide karti hai.

### 10.12.2 Mathematical Functions

Header: `<cmath>`

| Function | Work |
|---|---|
| `sqrt(x)` | Square root |
| `pow(x, y)` | x raised to y |
| `abs(x)` | Absolute value |
| `ceil(x)` | Upward integral rounding |
| `floor(x)` | Downward integral rounding |
| `round(x)` | Nearest integral value |

#### Program

```cpp
#include <cmath>
#include <iostream>
using namespace std;

int main()
{
    cout << sqrt(81.0) << '\n';
    cout << pow(2.0, 5.0) << '\n';
    cout << round(4.6) << '\n';
    return 0;
}
```

### 10.12.3 Character Functions

Header: `<cctype>`

| Function | Work |
|---|---|
| `isalpha(ch)` | Alphabet check |
| `isdigit(ch)` | Digit check |
| `isspace(ch)` | Whitespace check |
| `toupper(ch)` | Uppercase conversion |
| `tolower(ch)` | Lowercase conversion |

### 10.12.4 String Functions

`std::string` member functions:

- `length()` / `size()`
- `empty()`
- `substr()`
- `find()`
- `append()`

---

## 10.13 Scope Rules

### 10.13.1 Local Scope

Block/function ke andar declared variable sirf us scope mein accessible hota hai.

```cpp
void test()
{
    int localValue = 10;
}
```

### 10.13.2 Global Scope

Functions ke outside declared name global scope mein hota hai.

```cpp
int globalValue = 50;
```

> Unnecessary global variables avoid karein because dependencies aur side effects badh sakte hain.

### 10.13.3 Block Scope

```cpp
if (true)
{
    int value = 5;
}
// value is unavailable here
```

### 10.13.4 Shadowing

Inner scope ka same-name variable outer variable ko temporarily hide karta hai.

### 10.13.5 Scope Resolution Operator

Global variable ko access karne ke liye `::` use ho sakta hai.

```cpp
int value = 10;

int main()
{
    int value = 20;
    cout << value << '\n';   // Local: 20
    cout << ::value << '\n'; // Global: 10
}
```

---

## 10.14 Storage Classes

Storage-related specifiers variable ki storage duration, linkage ya access behavior affect karte hain.

### 10.14.1 auto

Traditional syllabus context mein automatic local storage ko describe karta hai. Modern C++ mein `auto` commonly type deduction ke liye use hota hai.

```cpp
auto total = 10 + 20;  // int deduced
```

### 10.14.2 register

Historically compiler ko fast register storage ka hint deta tha. Modern C++ compilers optimization automatically karte hain; keyword modern standards mein removed/deprecated historical topic hai.

### 10.14.3 static

Local static variable calls ke beech value retain karta hai.

```cpp
void countCalls()
{
    static int count = 0;
    ++count;
    cout << count << '\n';
}
```

Three calls par output: `1`, `2`, `3`.

### 10.14.4 extern

Variable/function ki definition another translation unit ya later location par existing hone ka declaration provide karta hai.

```cpp
extern int sharedValue;
```

### 10.14.5 Comparison

| Specifier | Main Idea |
|---|---|
| `auto` | Modern type deduction; historically automatic storage |
| `register` | Historical register hint |
| `static` | Extended storage duration / retained value |
| `extern` | External definition declaration |

---

## 10.15 Arrays as Function Parameters

### 10.15.1 Passing an Array

Built-in array parameter commonly pointer-like form mein receive hota hai; size separately pass karna padta hai.

```cpp
int calculateSum(const int values[], int size)
{
    int sum = 0;

    for (int i = 0; i < size; ++i)
    {
        sum += values[i];
    }

    return sum;
}
```

#### Program

```cpp
#include <iostream>
using namespace std;

int calculateSum(const int values[], int size)
{
    int sum = 0;
    for (int i = 0; i < size; ++i)
        sum += values[i];
    return sum;
}

int main()
{
    int marks[] = {70, 80, 90, 85, 75};
    int size = 5;

    cout << "Total = " << calculateSum(marks, size);
    return 0;
}
```

### 10.15.2 const Array Parameter

`const` function ko array elements modify karne se rokta hai.

### 10.15.3 Returning an Array

Built-in local array directly by value return nahi kiya jata. Safer modern alternatives include `std::array` aur `std::vector`, jo later data-structure study mein useful hain.

---

## 10.16 Recursion

### 10.16.1 Meaning of Recursion

> Recursion is a technique in which a function calls itself to solve a smaller version of the same problem.

### 10.16.2 Base Case

Recursion stop karne wali condition.

### 10.16.3 Recursive Case

Problem ko smaller instance mein reduce karke function dobara call karta hai.

### 10.16.4 Recursive Factorial

```cpp
unsigned long long factorial(unsigned int n)
{
    if (n <= 1)          // Base case
        return 1;

    return n * factorial(n - 1);  // Recursive case
}
```

#### Trace for factorial(4)

```text
factorial(4)
= 4 × factorial(3)
= 4 × 3 × factorial(2)
= 4 × 3 × 2 × factorial(1)
= 24
```

### 10.16.5 Recursive Sum

```cpp
int sumToN(int n)
{
    if (n <= 0)
        return 0;

    return n + sumToN(n - 1);
}
```

### 10.16.6 Recursion and Call Stack

Har recursive call ka separate stack frame hota hai. Base case missing ho to stack overflow ho sakta hai.

### 10.16.7 Recursion vs Iteration

| Recursion | Iteration |
|---|---|
| Function calls itself | Loop repeats |
| Base case required | Loop condition required |
| Elegant for recursive problems | Often less call overhead |
| Stack space use hota hai | Usually constant extra control space |

---

## 10.17 Function Best Practices

1. Function ka one clear purpose rakhein.
2. Meaningful name use karein.
3. Parameters minimal aur meaningful rakhein.
4. Input-only large objects ke liye const reference consider karein.
5. Unnecessary global variables avoid karein.
6. Function ko reasonably short rakhein.
7. Preconditions aur edge cases handle karein.
8. Recursion mein correct base case likhein.
9. Return type aur all return paths verify karein.
10. Repeated code ko reusable function mein move karein.

---

## 10.18 Common Mistakes

### 10.18.1 Missing Declaration

Call se pehle compiler ko declaration/definition visible honi chahiye.

### 10.18.2 Parameter Mismatch

Argument count aur compatible types function declaration se match hone chahiye.

### 10.18.3 Missing Return

Non-void function ke required path par correct value return karein.

### 10.18.4 Expecting Value Parameter to Modify Caller

Original modify karne ke liye reference parameter required ho sakta hai.

### 10.18.5 Returning Local Reference or Pointer

Local automatic variable function end par destroy hota hai; uska dangling reference/pointer return na karein.

### 10.18.6 Missing Recursive Base Case

Unbounded calls aur stack overflow cause ho sakta hai.

---

## 10.19 Important Differences

### 10.19.1 Library vs User-Defined Function

| Library Function | User-Defined Function |
|---|---|
| Standard library provides | Programmer creates |
| Required header use hota hai | Declaration/definition required |
| Example: `sqrt` | Example: `calculateSum` |

### 10.19.2 Declaration vs Definition

| Declaration | Definition |
|---|---|
| Interface batati hai | Actual body provide karti hai |
| Semicolon ke saath prototype | Curly-brace block |

### 10.19.3 Local vs Global Variable

| Local | Global |
|---|---|
| Block/function ke andar | Functions ke outside |
| Limited scope | Wider scope |
| Dependencies lower | Uncontrolled use risk |

---

## 10.20 Chapter Summary

Structured programming organizes a solution through sequence, selection, repetition and reusable modules. A function is a named block that performs a specific task and may accept parameters and return a value. Function declarations describe the interface, definitions provide the body and calls execute the function. Call by value protects the original argument by copying it, while call by reference can modify the caller's variable and avoid copies. C++ supports default arguments, function overloading and many standard library functions. Scope controls name visibility, and storage specifiers such as static and extern affect storage duration or linkage. Arrays can be passed with their size, and recursion solves a problem through smaller self-calls that must reach a base case.

---

## 10.21 Quick Revision

- Structured programming program ko clear modules mein divide karti hai.
- Function reusable named block hai.
- Declaration interface aur definition body deti hai.
- Parameters function mein aur arguments call mein hote hain.
- Call by value copy; call by reference original access karta hai.
- `void` function value return nahi karta.
- Function overloading same name with different parameter lists hai.
- Local scope limited aur global scope wider hota hai.
- Local static variable calls ke beech value retain karta hai.
- Array ke saath size separately pass karna useful hai.
- Recursion mein base case compulsory hai.

---

## 10.22 Important Abbreviations

| Abbreviation | Full Form |
|---|---|
| UDF | User-Defined Function |
| API | Application Programming Interface |
| IDE | Integrated Development Environment |
| STL | Standard Template Library |

---

## 10.23 Multiple-Choice Questions

1. Reusable named block ko kya kehte hain?  
   A. Function  B. Comment  C. Header only  D. Token only  
   **✅ Answer: A**

2. Function interface batane wali statement kya hai?  
   A. Declaration  B. Loop  C. Array element  D. Case  
   **✅ Answer: A**

3. Original variable modify karne ke liye kaunsa suitable hai?  
   A. Call by reference  B. Comment  C. Literal only  D. Namespace  
   **✅ Answer: A**

4. Value return na karne wala return type?  
   A. `void`  B. `double`  C. `int`  D. `char`  
   **✅ Answer: A**

5. Same name aur different parameter lists kya hai?  
   A. Overloading  B. Recursion only  C. Looping  D. Linking  
   **✅ Answer: A**

6. Calls ke beech value retain karne wala local specifier?  
   A. `static`  B. `extern` only  C. `void`  D. `goto`  
   **✅ Answer: A**

7. Recursive function ko stop karne ke liye kya chahiye?  
   A. Base case  B. Global variable compulsory  C. goto  D. switch  
   **✅ Answer: A**

---

## 10.24 Short-Answer Questions

1. Structured programming ko define kijiye.
2. Function kya hai aur kyun use hota hai?
3. Function declaration, definition aur call explain kijiye.
4. Parameters aur arguments mein difference likhiye.
5. User-defined functions ki four categories likhiye.
6. Call by value aur reference compare kijiye.
7. Default arguments kya hain?
8. Function overloading kya hai?
9. Local aur global scope explain kijiye.
10. `static` aur `extern` ka purpose likhiye.
11. Array ko function mein kaise pass karte hain?
12. Recursion aur base case explain kijiye.

---

## 10.25 Long-Answer and Exam Questions

1. Structured programming aur modular programming explain kijiye.
2. C++ functions ko syntax aur complete program ke saath samjhaiye.
3. Function categories examples ke saath explain kijiye.
4. Call by value aur call by reference programs ke saath compare kijiye.
5. Default arguments aur function overloading explain kijiye.
6. Standard mathematical and character functions describe kijiye.
7. Scope rules aur storage classes explain kijiye.
8. Array parameters ko program ke saath explain kijiye.
9. Recursion ko factorial trace ke saath samjhaiye.
10. Recursion aur iteration compare kijiye.

---

## 10.26 Practice Programs

1. Function se two numbers ka maximum find kijiye.
2. Function se number even/odd check kijiye.
3. Reference parameters se two values swap kijiye.
4. Function overloading se integer aur double area calculate kijiye.
5. Array ka average return karne wala function likhiye.
6. Recursive factorial function likhiye.
7. Recursive sum of first n numbers calculate kijiye.
8. Character function se input alphabet/digit check kijiye.

---

## 10.27 Viva Questions

1. Function prototype kya hai?
2. Function call mein control kahan jata hai?
3. Parameters aur arguments same hain?
4. Call by value original variable kyun nahi badalta?
5. Reference parameter mein `&` ka kya meaning hai?
6. Return type alone overload kyun nahi bana sakta?
7. Local variable kahan accessible hota hai?
8. Static local variable kab initialize hota hai?
9. Array size parameter kyun pass karte hain?
10. Recursion mein stack overflow kab ho sakta hai?

---

<div align="center">

### ✅ Chapter 10 Complete

[⬅️ Previous Chapter](chapter-09-decision-making-and-loops.md) · [📚 Table of Contents](../SUMMARY.md) · **Next: Arrays ➡️**

</div>
