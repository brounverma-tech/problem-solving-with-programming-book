# 💻 Appendix C: Practical C++ Programs

![C++](https://img.shields.io/badge/C%2B%2B-Practical_Programs-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Practice](https://img.shields.io/badge/Practice-Beginner_to_Advanced-brightgreen?style=for-the-badge)

> Is appendix me syllabus ke important C++ programs category-wise diye gaye hain. Har program ke saath short explanation aur sample output bhi hai.

---

## C.1 Basic Input and Output Programs

### C.1.1 Display a Message

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Welcome to C++ Programming!";
    return 0;
}
```

**Explanation:** `cout` screen par message display karta hai.

**Output:**

```text
Welcome to C++ Programming!
```

### C.1.2 Add Two Numbers

```cpp
#include <iostream>
using namespace std;

int main() {
    int firstNumber, secondNumber;

    cout << "Enter two numbers: ";
    cin >> firstNumber >> secondNumber;

    cout << "Sum = " << firstNumber + secondNumber;
    return 0;
}
```

**Explanation:** User se do integers lekar unka sum display kiya gaya hai.

**Sample Output:**

```text
Enter two numbers: 12 8
Sum = 20
```

### C.1.3 Calculate Simple Interest

```cpp
#include <iostream>
using namespace std;

int main() {
    double principal, rate, time;

    cout << "Enter principal, rate and time: ";
    cin >> principal >> rate >> time;

    double simpleInterest = (principal * rate * time) / 100;
    cout << "Simple Interest = " << simpleInterest;
    return 0;
}
```

**Formula:** `SI = (Principal × Rate × Time) / 100`

### C.1.4 Swap Two Numbers

```cpp
#include <iostream>
using namespace std;

int main() {
    int firstNumber, secondNumber, temporary;

    cin >> firstNumber >> secondNumber;
    temporary = firstNumber;
    firstNumber = secondNumber;
    secondNumber = temporary;

    cout << "After swapping: " << firstNumber << " " << secondNumber;
    return 0;
}
```

---

## C.2 Decision-Making Programs

### C.2.1 Check Even or Odd Number

```cpp
#include <iostream>
using namespace std;

int main() {
    int number;
    cout << "Enter a number: ";
    cin >> number;

    if (number % 2 == 0)
        cout << "Even number";
    else
        cout << "Odd number";

    return 0;
}
```

### C.2.2 Find the Largest of Three Numbers

```cpp
#include <iostream>
using namespace std;

int main() {
    int first, second, third;
    cin >> first >> second >> third;

    int largest = first;

    if (second > largest)
        largest = second;
    if (third > largest)
        largest = third;

    cout << "Largest = " << largest;
    return 0;
}
```

### C.2.3 Check Leap Year

```cpp
#include <iostream>
using namespace std;

int main() {
    int year;
    cin >> year;

    if ((year % 400 == 0) || (year % 4 == 0 && year % 100 != 0))
        cout << "Leap year";
    else
        cout << "Not a leap year";

    return 0;
}
```

### C.2.4 Create a Simple Calculator

```cpp
#include <iostream>
using namespace std;

int main() {
    double first, second;
    char operation;

    cout << "Enter expression (example: 10 + 5): ";
    cin >> first >> operation >> second;

    switch (operation) {
        case '+': cout << first + second; break;
        case '-': cout << first - second; break;
        case '*': cout << first * second; break;
        case '/':
            if (second != 0)
                cout << first / second;
            else
                cout << "Division by zero is not allowed";
            break;
        default: cout << "Invalid operator";
    }

    return 0;
}
```

---

## C.3 Loop-Based Programs

### C.3.1 Print a Multiplication Table

```cpp
#include <iostream>
using namespace std;

int main() {
    int number;
    cin >> number;

    for (int i = 1; i <= 10; i++) {
        cout << number << " x " << i << " = " << number * i << endl;
    }

    return 0;
}
```

### C.3.2 Find the Factorial of a Number

```cpp
#include <iostream>
using namespace std;

int main() {
    int number;
    unsigned long long factorial = 1;
    cin >> number;

    if (number < 0) {
        cout << "Factorial is not defined for negative numbers";
    } else {
        for (int i = 1; i <= number; i++)
            factorial *= i;

        cout << "Factorial = " << factorial;
    }

    return 0;
}
```

### C.3.3 Check a Prime Number

```cpp
#include <iostream>
using namespace std;

int main() {
    int number;
    bool isPrime = true;
    cin >> number;

    if (number < 2)
        isPrime = false;

    for (int i = 2; i * i <= number && isPrime; i++) {
        if (number % i == 0)
            isPrime = false;
    }

    cout << (isPrime ? "Prime number" : "Not a prime number");
    return 0;
}
```

### C.3.4 Display the Fibonacci Series

```cpp
#include <iostream>
using namespace std;

int main() {
    int terms;
    long long first = 0, second = 1;
    cin >> terms;

    for (int i = 1; i <= terms; i++) {
        cout << first << " ";
        long long next = first + second;
        first = second;
        second = next;
    }

    return 0;
}
```

### C.3.5 Reverse a Number

```cpp
#include <iostream>
using namespace std;

int main() {
    int number, reversedNumber = 0;
    cin >> number;

    while (number != 0) {
        int digit = number % 10;
        reversedNumber = reversedNumber * 10 + digit;
        number /= 10;
    }

    cout << "Reversed number = " << reversedNumber;
    return 0;
}
```

### C.3.6 Check a Palindrome Number

```cpp
#include <iostream>
using namespace std;

int main() {
    int number, originalNumber, reversedNumber = 0;
    cin >> number;
    originalNumber = number;

    while (number != 0) {
        reversedNumber = reversedNumber * 10 + number % 10;
        number /= 10;
    }

    if (originalNumber == reversedNumber)
        cout << "Palindrome number";
    else
        cout << "Not a palindrome number";

    return 0;
}
```

---

## C.4 Function Programs

### C.4.1 Find the Maximum Using a Function

```cpp
#include <iostream>
using namespace std;

int maximum(int first, int second) {
    return (first > second) ? first : second;
}

int main() {
    int first, second;
    cin >> first >> second;
    cout << "Maximum = " << maximum(first, second);
    return 0;
}
```

### C.4.2 Find Factorial Using Recursion

```cpp
#include <iostream>
using namespace std;

unsigned long long factorial(int number) {
    if (number <= 1)
        return 1;

    return number * factorial(number - 1);
}

int main() {
    int number;
    cin >> number;

    if (number < 0)
        cout << "Invalid input";
    else
        cout << "Factorial = " << factorial(number);

    return 0;
}
```

### C.4.3 Swap Using Call by Reference

```cpp
#include <iostream>
using namespace std;

void swapNumbers(int &first, int &second) {
    int temporary = first;
    first = second;
    second = temporary;
}

int main() {
    int first = 10, second = 20;
    swapNumbers(first, second);
    cout << first << " " << second;
    return 0;
}
```

---

## C.5 Array Programs

### C.5.1 Find Sum and Average of Array Elements

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[5];
    int sum = 0;

    for (int i = 0; i < 5; i++) {
        cin >> numbers[i];
        sum += numbers[i];
    }

    double average = static_cast<double>(sum) / 5;
    cout << "Sum = " << sum << endl;
    cout << "Average = " << average;
    return 0;
}
```

### C.5.2 Find the Largest Array Element

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[] = {45, 12, 89, 34, 67};
    int largest = numbers[0];

    for (int i = 1; i < 5; i++) {
        if (numbers[i] > largest)
            largest = numbers[i];
    }

    cout << "Largest = " << largest;
    return 0;
}
```

### C.5.3 Search an Element Using Linear Search

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[] = {10, 20, 30, 40, 50};
    int key, position = -1;
    cin >> key;

    for (int i = 0; i < 5; i++) {
        if (numbers[i] == key) {
            position = i;
            break;
        }
    }

    if (position != -1)
        cout << "Element found at index " << position;
    else
        cout << "Element not found";

    return 0;
}
```

### C.5.4 Sort an Array Using Bubble Sort

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[] = {5, 1, 4, 2, 8};
    int size = 5;

    for (int i = 0; i < size - 1; i++) {
        for (int j = 0; j < size - i - 1; j++) {
            if (numbers[j] > numbers[j + 1]) {
                int temporary = numbers[j];
                numbers[j] = numbers[j + 1];
                numbers[j + 1] = temporary;
            }
        }
    }

    for (int number : numbers)
        cout << number << " ";

    return 0;
}
```

### C.5.5 Add Two Matrices

```cpp
#include <iostream>
using namespace std;

int main() {
    int first[2][2] = {{1, 2}, {3, 4}};
    int second[2][2] = {{5, 6}, {7, 8}};
    int sum[2][2];

    for (int row = 0; row < 2; row++) {
        for (int column = 0; column < 2; column++) {
            sum[row][column] = first[row][column] + second[row][column];
            cout << sum[row][column] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

---

## C.6 String Programs

### C.6.1 Count Vowels in a String

```cpp
#include <iostream>
#include <string>
#include <cctype>
using namespace std;

int main() {
    string text;
    int vowelCount = 0;
    getline(cin, text);

    for (char character : text) {
        character = tolower(static_cast<unsigned char>(character));

        if (character == 'a' || character == 'e' || character == 'i' ||
            character == 'o' || character == 'u') {
            vowelCount++;
        }
    }

    cout << "Number of vowels = " << vowelCount;
    return 0;
}
```

### C.6.2 Check a Palindrome String

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string text;
    getline(cin, text);

    bool isPalindrome = true;

    for (int left = 0, right = static_cast<int>(text.length()) - 1;
         left < right; left++, right--) {
        if (text[left] != text[right]) {
            isPalindrome = false;
            break;
        }
    }

    cout << (isPalindrome ? "Palindrome string" : "Not a palindrome string");
    return 0;
}
```

---

## C.7 Pointer Programs

### C.7.1 Access a Variable Using a Pointer

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 25;
    int *pointer = &number;

    cout << "Value = " << *pointer << endl;
    cout << "Address = " << pointer;
    return 0;
}
```

### C.7.2 Find Array Sum Using a Pointer

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[] = {10, 20, 30, 40, 50};
    int *pointer = numbers;
    int sum = 0;

    for (int i = 0; i < 5; i++)
        sum += *(pointer + i);

    cout << "Sum = " << sum;
    return 0;
}
```

### C.7.3 Use Dynamic Memory for an Array

```cpp
#include <iostream>
using namespace std;

int main() {
    int size;
    cin >> size;

    int *numbers = new int[size];

    for (int i = 0; i < size; i++)
        cin >> numbers[i];

    for (int i = 0; i < size; i++)
        cout << numbers[i] << " ";

    delete[] numbers;
    numbers = nullptr;
    return 0;
}
```

---

## C.8 Structure and File Programs

### C.8.1 Store Student Details Using a Structure

```cpp
#include <iostream>
#include <string>
using namespace std;

struct Student {
    int rollNumber;
    string name;
    float marks;
};

int main() {
    Student student;

    cout << "Enter roll number: ";
    cin >> student.rollNumber;
    cin.ignore();

    cout << "Enter name: ";
    getline(cin, student.name);

    cout << "Enter marks: ";
    cin >> student.marks;

    cout << "\nStudent Details\n";
    cout << "Roll Number: " << student.rollNumber << endl;
    cout << "Name: " << student.name << endl;
    cout << "Marks: " << student.marks;
    return 0;
}
```

### C.8.2 Write and Read Data from a File

```cpp
#include <iostream>
#include <fstream>
#include <string>
using namespace std;

int main() {
    ofstream outputFile("student.txt");

    if (!outputFile) {
        cout << "Unable to create file";
        return 1;
    }

    outputFile << "Aman 85" << endl;
    outputFile.close();

    ifstream inputFile("student.txt");
    string line;

    while (getline(inputFile, line))
        cout << line << endl;

    inputFile.close();
    return 0;
}
```

---

## C.9 Practice Questions

1. Celsius ko Fahrenheit me convert karne ka program likhiye.
2. Armstrong number check karne ka program likhiye.
3. Kisi number ke digits ka sum calculate kijiye.
4. `1` se `n` tak sabhi prime numbers display kijiye.
5. Array me second-largest element find kijiye.
6. Do matrices ka multiplication kijiye.
7. String me words, vowels aur consonants count kijiye.
8. Pointer ka use karke do numbers swap kijiye.
9. Function overloading ka program likhiye.
10. File me student records save aur display kijiye.

---

## ✅ Programming Checklist

- Problem aur required input-output ko pehle samjhein.
- Algorithm ya rough steps banayein.
- Meaningful variable names use karein.
- Invalid input aur special cases handle karein.
- Program compile karke multiple test values se check karein.
- Output ko expected result ke saath verify karein.

---

## 📝 One-Line Summary

> **Programming sirf code padhne se nahi, balki programs khud likhne, test karne aur errors solve karne se aati hai.**

---

[⬅️ Appendix B](appendix-b-cpp-syntax-quick-reference.md) | [📚 Table of Contents](../SUMMARY.md)
