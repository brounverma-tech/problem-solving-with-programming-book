<div align="center">

# 🔀 Chapter 9: Decision-Making and Loops

### 🟠 Unit C — Programming Fundamentals Using C++

![Level](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-orange?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Code](https://img.shields.io/badge/Programs-C%2B%2B-purple?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Control statement aur control flow samajh sakenge.
- `if`, `if-else`, nested `if` aur `else-if` ladder use kar sakenge.
- `switch` statement se multi-way selection bana sakenge.
- `while`, `do-while` aur `for` loops apply kar sakenge.
- Nested loops se patterns aur tables bana sakenge.
- `break`, `continue` aur `goto` ka behavior samajh sakenge.
- Infinite loop aur common control-flow errors identify kar sakenge.
- Decision-making aur repetition based C++ programs likh sakenge.

---

# 9.1 Introduction to Control Statements

## 9.1.1 Control Flow

> Control flow is the order in which the statements of a program are executed.

**Hinglish:** Program ke statements kis order mein execute honge, ise control flow kehte hain.

## 9.1.2 Control Statement

Control statement program execution ka normal sequential order change karta hai.

## 9.1.3 Types of Control Statements

```text
Control Statements
│
├── Selection / Decision
│   ├── if
│   ├── if-else
│   ├── else-if ladder
│   ├── nested if
│   └── switch
│
├── Repetition / Loops
│   ├── while
│   ├── do-while
│   └── for
│
└── Jump Statements
    ├── break
    ├── continue
    ├── goto
    └── return
```

## 9.1.4 Important Terms

| Term | Pronunciation | Meaning |
|---|---|---|
| Condition | कंडीशन | True/false expression |
| Selection | सिलेक्शन | Condition ke according path choose karna |
| Iteration | इटरेशन | Statements ko repeat karna |
| Loop | लूप | Repetition structure |
| Counter | काउंटर | Iteration count track karne wala variable |
| Initialization | इनिशियलाइज़ेशन | Initial value set karna |
| Termination | टर्मिनेशन | Loop/program ka stop hona |
| Infinite Loop | इनफिनिट लूप | Kabhi terminate na hone wala loop |

---

# 9.2 Simple if Statement

## 9.2.1 Meaning

Condition true ho to block execute hota hai; false ho to block skip hota hai.

## Syntax

```cpp
if (condition)
{
    statements;
}
```

## Example

```cpp
int age = 20;

if (age >= 18)
{
    cout << "Eligible to vote";
}
```

## Flow

```text
      Condition
       /     \
    true     false
      |        |
 Execute     Skip
      \        /
       Continue
```

## Program: Positive Number

```cpp
#include <iostream>
using namespace std;

int main()
{
    int number;
    cout << "Enter a number: ";
    cin >> number;

    if (number > 0)
    {
        cout << "Positive number";
    }

    return 0;
}
```

---

# 9.3 if-else Statement

## 9.3.1 Meaning

Condition true ho to `if` block aur false ho to `else` block execute hota hai.

## Syntax

```cpp
if (condition)
{
    statementsForTrue;
}
else
{
    statementsForFalse;
}
```

## Program: Even or Odd

```cpp
#include <iostream>
using namespace std;

int main()
{
    int number;
    cout << "Enter an integer: ";
    cin >> number;

    if (number % 2 == 0)
    {
        cout << "Even";
    }
    else
    {
        cout << "Odd";
    }

    return 0;
}
```

---

# 9.4 else-if Ladder

## 9.4.1 Meaning

Multiple conditions ko top-to-bottom check karta hai. First true condition ka block execute hota hai.

## Syntax

```cpp
if (condition1)
{
    statements1;
}
else if (condition2)
{
    statements2;
}
else if (condition3)
{
    statements3;
}
else
{
    defaultStatements;
}
```

## Program: Grade Calculator

```cpp
#include <iostream>
using namespace std;

int main()
{
    double marks;
    cout << "Enter marks (0-100): ";
    cin >> marks;

    if (marks < 0 || marks > 100)
        cout << "Invalid marks";
    else if (marks >= 90)
        cout << "Grade A";
    else if (marks >= 75)
        cout << "Grade B";
    else if (marks >= 60)
        cout << "Grade C";
    else if (marks >= 40)
        cout << "Grade D";
    else
        cout << "Fail";

    return 0;
}
```

> Conditions ko correct order mein rakhein. `marks >= 40` ko sabse pehle rakhne par higher grades tak program nahi pahunchega.

---

# 9.5 Nested if Statement

## 9.5.1 Meaning

Ek `if` ya `else` block ke andar another `if` statement nested if kehlata hai.

## Program: Login Check

```cpp
#include <iostream>
#include <string>
using namespace std;

int main()
{
    string username;
    string password;

    cout << "Enter username: ";
    cin >> username;

    if (username == "admin")
    {
        cout << "Enter password: ";
        cin >> password;

        if (password == "1234")
            cout << "Login successful";
        else
            cout << "Incorrect password";
    }
    else
    {
        cout << "Unknown user";
    }

    return 0;
}
```

---

# 9.6 Dangling else and Braces

Without braces, `else` nearest unmatched `if` se associate hota hai.

```cpp
if (a > 0)
{
    if (b > 0)
    {
        cout << "Both positive";
    }
    else
    {
        cout << "b is not positive";
    }
}
```

> Braces use karne se control flow clear aur errors kam hote hain.

---

# 9.7 switch Statement

## 9.7.1 Meaning

> A switch statement selects one execution path from multiple constant cases based on an expression.

## Syntax

```cpp
switch (expression)
{
    case constant1:
        statements1;
        break;

    case constant2:
        statements2;
        break;

    default:
        defaultStatements;
}
```

## Working

1. Expression evaluate hoti hai.
2. Matching case locate hota hai.
3. Statements execute hote hain.
4. `break` switch se bahar nikalta hai.
5. Match na mile to `default` execute hota hai.

## Program: Simple Calculator

```cpp
#include <iostream>
using namespace std;

int main()
{
    double a, b;
    char operation;

    cout << "Enter expression (example 8 + 2): ";
    cin >> a >> operation >> b;

    switch (operation)
    {
        case '+':
            cout << a + b;
            break;

        case '-':
            cout << a - b;
            break;

        case '*':
            cout << a * b;
            break;

        case '/':
            if (b != 0)
                cout << a / b;
            else
                cout << "Division by zero is not allowed";
            break;

        default:
            cout << "Invalid operator";
    }

    return 0;
}
```

## 9.7.2 Fall-Through

`break` absent ho to execution next case mein continue kar sakti hai.

```cpp
switch (day)
{
    case 6:
    case 7:
        cout << "Weekend";
        break;
    default:
        cout << "Working day";
}
```

## 9.7.3 switch Limitations

- Case labels compile-time constant values hone chahiye.
- Duplicate case values allowed nahi.
- General ranges directly express nahi hote.
- Complex relational conditions ke liye `if-else` better hai.

---

# 9.8 if-else vs switch

| Basis | if-else | switch |
|---|---|---|
| Conditions | Relational/logical expressions | One expression vs constant cases |
| Ranges | Easy | Directly suitable nahi |
| Data choices | Flexible | Integral/enum-like supported cases |
| Best use | Complex decisions | Menu and fixed choices |
| Fall-through | No | Possible |

---

# 9.9 Introduction to Loops

## 9.9.1 Meaning

> A loop repeatedly executes a block of statements while a condition or iteration rule allows it.

## 9.9.2 Loop Components

1. Initialization
2. Condition
3. Loop body
4. Update
5. Termination

## 9.9.3 Types

- `while` — entry-controlled
- `for` — entry-controlled
- `do-while` — exit-controlled

---

# 9.10 while Loop

## Syntax

```cpp
initialization;

while (condition)
{
    statements;
    update;
}
```

Condition loop body se pehle check hoti hai. Initially false condition par loop zero times execute ho sakta hai.

## Program: 1 to 10

```cpp
#include <iostream>
using namespace std;

int main()
{
    int number = 1;

    while (number <= 10)
    {
        cout << number << ' ';
        ++number;
    }

    return 0;
}
```

## Program: Sum of First n Numbers

```cpp
int n;
long long sum = 0;
int i = 1;

cin >> n;

while (i <= n)
{
    sum += i;
    ++i;
}

cout << "Sum = " << sum;
```

---

# 9.11 do-while Loop

## Syntax

```cpp
do
{
    statements;
    update;
}
while (condition);
```

Condition body ke baad check hoti hai, isliye loop minimum one time execute hota hai.

## Program: Menu Repeat

```cpp
#include <iostream>
using namespace std;

int main()
{
    int choice;

    do
    {
        cout << "\n1. Say Hello\n0. Exit\nChoice: ";
        cin >> choice;

        if (choice == 1)
            cout << "Hello!\n";
        else if (choice != 0)
            cout << "Invalid choice\n";

    } while (choice != 0);

    return 0;
}
```

---

# 9.12 for Loop

## Syntax

```cpp
for (initialization; condition; update)
{
    statements;
}
```

## Program: Multiplication Table

```cpp
#include <iostream>
using namespace std;

int main()
{
    int number;
    cout << "Enter a number: ";
    cin >> number;

    for (int i = 1; i <= 10; ++i)
    {
        cout << number << " x " << i
             << " = " << number * i << '\n';
    }

    return 0;
}
```

## Execution Order

1. Initialization once.
2. Condition check.
3. Body execute.
4. Update execute.
5. Condition dobara check.

## 9.12.1 Multiple Expressions

```cpp
for (int i = 0, j = 10; i < j; ++i, --j)
{
    cout << i << ' ' << j << '\n';
}
```

---

# 9.13 while vs do-while vs for

| Basis | while | do-while | for |
|---|---|---|---|
| Condition | Before body | After body | Before body |
| Minimum executions | 0 | 1 | 0 |
| Best use | Unknown repetitions | Body at least once | Known/count-controlled |
| Update location | Body | Body | Header usually |

---

# 9.14 Nested Loops

Ek loop ke andar another loop nested loop hai.

## Program: Star Pattern

```cpp
#include <iostream>
using namespace std;

int main()
{
    int rows = 5;

    for (int i = 1; i <= rows; ++i)
    {
        for (int j = 1; j <= i; ++j)
        {
            cout << "* ";
        }
        cout << '\n';
    }

    return 0;
}
```

## Output

```text
*
* *
* * *
* * * *
* * * * *
```

## 9.14.1 Iteration Count

Outer loop m aur inner loop n times run ho to total body executions approximately m × n ho sakte hain.

---

# 9.15 break Statement

Current loop ya switch ko immediately terminate karta hai.

```cpp
for (int i = 1; i <= 10; ++i)
{
    if (i == 6)
        break;

    cout << i << ' ';
}
```

Output: `1 2 3 4 5`

> Nested loops mein `break` normally sirf nearest enclosing loop ko terminate karta hai.

---

# 9.16 continue Statement

Current iteration ke remaining statements skip karke next iteration par jata hai.

```cpp
for (int i = 1; i <= 10; ++i)
{
    if (i % 2 == 0)
        continue;

    cout << i << ' ';
}
```

Output: `1 3 5 7 9`

---

# 9.17 goto Statement

## 9.17.1 Meaning

`goto` same function ke labeled statement par unconditional jump karta hai.

```cpp
goto labelName;

labelName:
    statement;
```

## Example

```cpp
int number;

readAgain:
cout << "Enter a positive number: ";
cin >> number;

if (number <= 0)
    goto readAgain;
```

## 9.17.2 Why goto Is Usually Avoided

- Control flow difficult to follow ho sakta hai.
- Debugging aur maintenance hard hoti hai.
- Structured loops aur functions clearer alternatives dete hain.

> Syllabus understanding ke liye `goto` important hai, lekin normal structured programming mein limited use karein.

---

# 9.18 return Statement

Function execution terminate karke caller ko control return karta hai.

```cpp
if (inputInvalid)
{
    return 1;
}
```

`main` se zero return generally success status represent karta hai.

---

# 9.19 Infinite Loops

## 9.19.1 Intentional Infinite Loop

```cpp
while (true)
{
    // Repeated service work
}
```

## 9.19.2 Accidental Infinite Loop

```cpp
int i = 1;

while (i <= 10)
{
    cout << i;
    // Missing ++i
}
```

## 9.19.3 Prevention

- Update statement verify karein.
- Condition eventually false honi chahiye.
- Counter ka correct type/range use karein.
- Debugger ya temporary trace output use karein.

---

# Program: Factorial

For non-negative n:

$$n! = 1 × 2 × 3 × ... × n$$

```cpp
#include <iostream>
using namespace std;

int main()
{
    int n;
    unsigned long long factorial = 1;

    cout << "Enter a non-negative integer: ";
    cin >> n;

    if (n < 0)
    {
        cout << "Factorial is not defined here for negatives";
        return 1;
    }

    for (int i = 2; i <= n; ++i)
    {
        factorial *= i;
    }

    cout << n << "! = " << factorial;
    return 0;
}
```

> Large n par fixed-width integer overflow ho sakta hai.

---

# Program: Prime Number Check

```cpp
#include <iostream>
using namespace std;

int main()
{
    int number;
    bool isPrime = true;

    cout << "Enter an integer: ";
    cin >> number;

    if (number < 2)
    {
        isPrime = false;
    }
    else
    {
        for (int divisor = 2;
             divisor <= number / divisor;
             ++divisor)
        {
            if (number % divisor == 0)
            {
                isPrime = false;
                break;
            }
        }
    }

    cout << (isPrime ? "Prime" : "Not prime");
    return 0;
}
```

---

# Program: Reverse a Number

```cpp
#include <iostream>
using namespace std;

int main()
{
    int number;
    int reversed = 0;

    cout << "Enter a non-negative integer: ";
    cin >> number;

    while (number > 0)
    {
        int digit = number % 10;
        reversed = reversed * 10 + digit;
        number /= 10;
    }

    cout << "Reversed = " << reversed;
    return 0;
}
```

---

# 9.20 Common Mistakes

## 9.20.1 Semicolon After if

```cpp
if (marks >= 40);  // Wrong unintended empty statement
{
    cout << "Pass";
}
```

## 9.20.2 Assignment Instead of Comparison

```cpp
if (choice = 1)   // Assignment
if (choice == 1)  // Comparison
```

## 9.20.3 Missing break in switch

Unwanted fall-through cause ho sakta hai.

## 9.20.4 Missing Loop Update

Infinite loop cause ho sakta hai.

## 9.20.5 Off-by-One Error

`i < n` aur `i <= n` ka incorrect selection one extra ya one fewer iteration cause karta hai.

## 9.20.6 Uninitialized Counter

Counter ko use se pehle initialize karein.

---

# 9.21 Important Differences

## 9.21.1 if vs if-else

| if | if-else |
|---|---|
| True path only | True and false paths |
| False par block skip | False par else block |

## 9.21.2 break vs continue

| break | continue |
|---|---|
| Loop terminate | Current iteration skip |
| Control loop ke baad | Control next iteration par |

## 9.21.3 Entry vs Exit Controlled

| Entry-Controlled | Exit-Controlled |
|---|---|
| Condition body se pehle | Condition body ke baad |
| while, for | do-while |
| Zero executions possible | At least one execution |

---

# 9.22 Chapter Summary

Control statements change the normal sequence of program execution. Selection statements choose a path: if handles a single condition, if-else provides two alternatives, an else-if ladder checks multiple conditions, nested if supports dependent decisions and switch selects among constant cases. Loops repeat statements: while and for are entry-controlled, while do-while is exit-controlled and executes at least once. Nested loops solve grid and pattern problems. The break statement terminates the nearest loop or switch, continue skips the remaining part of the current iteration, goto performs an unconditional labeled jump and return ends a function. Correct initialization, conditions, updates and braces prevent common errors such as infinite loops, fall-through and off-by-one mistakes.

---

# 9.23 Quick Revision

- Control flow statements ka execution order hai.
- `if` condition true hone par block execute karta hai.
- `else-if` ladder multiple conditions check karti hai.
- `switch` fixed choices aur menus ke liye useful hai.
- `break` unwanted switch fall-through rokta hai.
- `while` aur `for` entry-controlled loops hain.
- `do-while` minimum one time execute hota hai.
- Nested loop ke andar another loop hota hai.
- `break` loop terminate aur `continue` iteration skip karta hai.
- `goto` unconditional jump hai aur generally avoid kiya jata hai.
- Missing update infinite loop cause kar sakta hai.

---

# 9.24 Multiple-Choice Questions

1. Two-way selection ke liye kya use hota hai?  
   A. if-else  B. comment  C. include  D. namespace  
   **✅ Answer: A**

2. Fixed menu choices ke liye suitable statement kaunsa hai?  
   A. switch  B. sizeof  C. pointer  D. include  
   **✅ Answer: A**

3. Kaunsa loop minimum one time execute hota hai?  
   A. while  B. for  C. do-while  D. None  
   **✅ Answer: C**

4. Loop ko immediately terminate kaun karta hai?  
   A. continue  B. break  C. case  D. const  
   **✅ Answer: B**

5. Current iteration skip kaun karta hai?  
   A. continue  B. break  C. switch  D. return only  
   **✅ Answer: A**

6. Known number of repetitions ke liye commonly suitable loop?  
   A. for  B. goto  C. switch  D. if only  
   **✅ Answer: A**

7. switch case ke baad missing break kya cause kar sakta hai?  
   A. Fall-through  B. Compilation always stops  C. No output ever  D. Header error  
   **✅ Answer: A**

8. Never-ending loop ko kya kehte hain?  
   A. Nested loop  B. Infinite loop  C. Selection  D. Function  
   **✅ Answer: B**

---

# 9.25 Short-Answer Questions

1. Control statement ko define kijiye.
2. Simple if ka syntax aur working likhiye.
3. if-else aur else-if ladder mein difference likhiye.
4. Nested if kya hai?
5. switch statement ke rules likhiye.
6. switch mein break ka role kya hai?
7. while, do-while aur for compare kijiye.
8. Nested loop kya hai?
9. break aur continue mein difference likhiye.
10. goto generally avoid kyun kiya jata hai?
11. Infinite loop kya hai?
12. Off-by-one error kya hai?

---

# 9.26 Long-Answer and Exam Questions

1. Selection statements ko syntax, flow aur examples ke saath explain kijiye.
2. else-if ladder se grade-calculator program likhiye.
3. switch statement ka calculator program likhiye.
4. while, do-while aur for loops ko compare kijiye.
5. Multiplication table aur sum of n numbers ke programs likhiye.
6. Nested loops se star pattern banaiye.
7. break, continue, goto aur return explain kijiye.
8. Factorial calculate karne ka C++ program likhiye.
9. Prime number check karne ka program likhiye.
10. Common control-flow mistakes aur prevention explain kijiye.

---

# 9.27 Practice Programs

1. Number positive, negative ya zero check kijiye.
2. Three numbers mein largest find kijiye.
3. Leap year check kijiye.
4. Character vowel ya consonant check kijiye.
5. switch se day name display kijiye.
6. 1 to n ka sum calculate kijiye.
7. n ka multiplication table print kijiye.
8. Number ke digits count kijiye.
9. Number palindrome hai ya nahi check kijiye.
10. Fibonacci series ke first n terms print kijiye.
11. Nested loop se number pattern banaiye.
12. 1 to 100 mein multiples of 3 skip kijiye.

---

# 9.28 Viva Questions

1. Condition ka result kis type ka hota hai?
2. else kis if se attach hota hai?
3. switch ka default kab execute hota hai?
4. Fall-through kya hai?
5. while loop zero times kab execute hota hai?
6. do-while ke end mein semicolon kyun hota hai?
7. for loop ke three header parts kya hain?
8. Nested loop mein break kya terminate karta hai?
9. continue aur break same hain?
10. Infinite loop ko kaise prevent karte hain?

---

<div align="center">

## ✅ Chapter 9 Complete

[⬅️ Previous Chapter](chapter-08-operators-and-expressions.md) · [📚 Table of Contents](../SUMMARY.md) · **Next: Functions and Structured Programming ➡️**

</div>
