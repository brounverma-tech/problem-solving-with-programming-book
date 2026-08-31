<div align="center">

# 📊 Chapter 11: Arrays

### 🔴 Unit D — Functions, Arrays and Pointers in C++

![Level](https://img.shields.io/badge/Level-Intermediate-orange?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Code](https://img.shields.io/badge/Programs-C%2B%2B-purple?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Array ko define aur memory layout samajh sakenge.
- One-dimensional array declare, initialize aur traverse kar sakenge.
- Array elements input, output aur update kar sakenge.
- Sum, average, minimum aur maximum calculate kar sakenge.
- Linear search aur basic sorting apply kar sakenge.
- Two-dimensional arrays aur matrices use kar sakenge.
- Multidimensional arrays samajh sakenge.
- Arrays ko functions mein safely pass kar sakenge.
- Common boundary aur initialization errors avoid kar sakenge.

---

# 11.1 Introduction to Arrays

## 11.1.1 Meaning of Array

> An array is a fixed-size collection of elements of the same data type stored in contiguous memory locations.

**Hinglish:** Array same data type ki multiple values ko ek hi name ke under consecutive memory locations mein store karta hai.

## 11.1.2 Need for Arrays

Without array:

```cpp
int mark1, mark2, mark3, mark4, mark5;
```

With array:

```cpp
int marks[5];
```

Arrays repeated data ko organize karte hain aur loops ke saath processing easy banate hain.

## 11.1.3 Main Characteristics

- All elements same data type ke hote hain.
- Size fixed hota hai for built-in arrays.
- Elements contiguous memory mein stored hote hain.
- Zero-based indexing use hoti hai.
- Direct index access fast hota hai.
- Built-in array apni size automatically runtime par track nahi karta.

## 11.1.4 Important Terms

| Term | Pronunciation | Meaning |
|---|---|---|
| Array | अरे | Same-type elements ka collection |
| Element | एलिमेंट | Array ki individual value |
| Index | इंडेक्स | Element ki position number |
| Traversal | ट्रैवर्सल | All elements ko visit karna |
| Contiguous | कंटिग्युअस | Consecutive memory locations |
| Dimension | डाइमेंशन | Array indexing directions ki count |
| Boundary | बाउंड्री | Valid index range ki limit |

---

# 11.2 One-Dimensional Arrays

## 11.2.1 Declaration

### Syntax

```cpp
dataType arrayName[arraySize];
```

### Example

```cpp
int marks[5];
double prices[10];
char grades[4];
```

## 11.2.2 Indexing

Five-element array ke valid indexes:

```text
Index:   0    1    2    3    4
Value:  [ ]  [ ]  [ ]  [ ]  [ ]
```

For size n, valid indexes:

$$0\text{ to }n-1$$

## 11.2.3 Element Access

```cpp
marks[0] = 75;
marks[1] = 82;

cout << marks[0];
```

## 11.2.4 Element Update

```cpp
marks[2] = 90;
marks[2] += 5;
```

---

# 11.3 Array Initialization

## 11.3.1 Complete Initialization

```cpp
int numbers[5] = {10, 20, 30, 40, 50};
```

## 11.3.2 Size Inference

```cpp
int numbers[] = {10, 20, 30, 40, 50};
```

Compiler initializer count se size determine karta hai.

## 11.3.3 Partial Initialization

```cpp
int numbers[5] = {10, 20};
```

Remaining elements zero-initialize hote hain.

## 11.3.4 Zero Initialization

```cpp
int numbers[5] = {};
```

All elements zero ho jate hain.

## 11.3.5 Character Array Initialization

```cpp
char word[] = {'H', 'e', 'l', 'l', 'o', '\0'};
char text[] = "Hello";
```

Null character `\0` C-style string ka end mark karta hai.

---

# 11.4 Array Input and Output

## 11.4.1 Input with Loop

```cpp
const int size = 5;
int marks[size];

for (int i = 0; i < size; ++i)
{
    cout << "Enter mark " << i + 1 << ": ";
    cin >> marks[i];
}
```

## 11.4.2 Output with Loop

```cpp
for (int i = 0; i < size; ++i)
{
    cout << marks[i] << ' ';
}
```

## 11.4.3 Range-Based for Loop

```cpp
int values[] = {10, 20, 30, 40};

for (int value : values)
{
    cout << value << ' ';
}
```

Elements modify karne ke liye reference use ho sakta hai:

```cpp
for (int& value : values)
{
    value *= 2;
}
```

---

# 11.5 Array Size

## 11.5.1 sizeof Method

Same scope mein complete built-in array available ho to:

```cpp
int values[] = {10, 20, 30, 40, 50};

int count = sizeof(values) / sizeof(values[0]);
```

## 11.5.2 std::size

Modern C++:

```cpp
#include <iterator>

int count = std::size(values);
```

> Function parameter mein built-in array pointer-like form mein adjust ho jata hai, isliye size separately pass karna useful hai.

---

# 11.6 Basic Array Operations

## 11.6.1 Traversal

All elements ko sequentially visit karna.

## 11.6.2 Insertion by Position

Fixed array mein middle insertion ke liye elements right shift karne padte hain, aur enough capacity required hoti hai.

## 11.6.3 Deletion by Position

Element logically remove karne ke liye later elements left shift kiye jate hain aur logical size decrease hoti hai.

## 11.6.4 Searching

Target element locate karna.

## 11.6.5 Sorting

Elements ko ascending ya descending order mein arrange karna.

---

# 11.7 Sum and Average

### Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    const int size = 5;
    double marks[size];
    double total = 0;

    for (int i = 0; i < size; ++i)
    {
        cout << "Enter mark " << i + 1 << ": ";
        cin >> marks[i];
        total += marks[i];
    }

    double average = total / size;

    cout << "Total = " << total << '\n';
    cout << "Average = " << average << '\n';
    return 0;
}
```

---

# 11.8 Minimum and Maximum

## 11.8.1 Algorithm

1. First element ko initial minimum/maximum maan lein.
2. Remaining elements traverse karein.
3. Smaller value mile to minimum update karein.
4. Larger value mile to maximum update karein.

### Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    int values[] = {42, 15, 89, 7, 63};
    const int size = 5;

    int minimum = values[0];
    int maximum = values[0];

    for (int i = 1; i < size; ++i)
    {
        if (values[i] < minimum)
            minimum = values[i];

        if (values[i] > maximum)
            maximum = values[i];
    }

    cout << "Minimum = " << minimum << '\n';
    cout << "Maximum = " << maximum << '\n';
    return 0;
}
```

---

# 11.9 Linear Search

## 11.9.1 Meaning

> Linear search checks elements one by one until the target is found or the array ends.

## 11.9.2 Working

1. Index 0 se start karein.
2. Current element ko target se compare karein.
3. Match par index return/display karein.
4. End tak match na ho to not found.

### Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    int values[] = {12, 25, 7, 40, 18};
    const int size = 5;
    int target;
    int foundIndex = -1;

    cout << "Enter value to search: ";
    cin >> target;

    for (int i = 0; i < size; ++i)
    {
        if (values[i] == target)
        {
            foundIndex = i;
            break;
        }
    }

    if (foundIndex != -1)
        cout << "Found at index " << foundIndex;
    else
        cout << "Not found";

    return 0;
}
```

## 11.9.3 Complexity

Worst case mein n elements check karne padte hain: $O(n)$.

---

# 11.10 Bubble Sort

## 11.10.1 Meaning

Bubble sort repeatedly adjacent elements compare karta hai aur wrong order mein hone par swap karta hai.

## 11.10.2 Working

Har pass ke baad largest unsorted element end ki taraf move hota hai.

### Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    int values[] = {5, 1, 4, 2, 8};
    const int size = 5;

    for (int pass = 0; pass < size - 1; ++pass)
    {
        bool swapped = false;

        for (int i = 0; i < size - 1 - pass; ++i)
        {
            if (values[i] > values[i + 1])
            {
                int temp = values[i];
                values[i] = values[i + 1];
                values[i + 1] = temp;
                swapped = true;
            }
        }

        if (!swapped)
            break;
    }

    for (int value : values)
        cout << value << ' ';

    return 0;
}
```

## 11.10.3 Complexity

Typical/worst-case time complexity $O(n^2)$ hai. Large data ke liye more efficient standard sorting algorithms prefer hote hain.

---

# 11.11 Arrays and Functions

## 11.11.1 Passing Array to Function

```cpp
void display(const int values[], int size)
{
    for (int i = 0; i < size; ++i)
        cout << values[i] << ' ';
}
```

## 11.11.2 Modifying Elements

```cpp
void doubleValues(int values[], int size)
{
    for (int i = 0; i < size; ++i)
        values[i] *= 2;
}
```

## 11.11.3 Read-Only Array Parameter

Input-only array ke liye `const` use karein.

## 11.11.4 Fixed-Size Array by Reference

Template/reference syntax size preserve kar sakti hai:

```cpp
template <std::size_t N>
void display(const int (&values)[N])
{
    for (int value : values)
        cout << value << ' ';
}
```

Beginner programs mein array plus explicit size simple aur clear approach hai.

---

# 11.12 Two-Dimensional Arrays

## 11.12.1 Meaning

> A two-dimensional array stores elements in rows and columns.

### Declaration

```cpp
int matrix[3][4];
```

Yeh 3 rows aur 4 columns ka array hai.

## 11.12.2 Initialization

```cpp
int matrix[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```

## 11.12.3 Element Access

```cpp
cout << matrix[0][1];  // 2
matrix[1][2] = 10;
```

## 11.12.4 Traversal

```cpp
for (int row = 0; row < 2; ++row)
{
    for (int column = 0; column < 3; ++column)
    {
        cout << matrix[row][column] << ' ';
    }
    cout << '\n';
}
```

## 11.12.5 Row-Major Storage

C++ built-in multidimensional arrays row-major order mein store hote hain: first row ke elements, then second row, and so on.

---

# 11.13 Matrix Input and Output

### Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    const int rows = 2;
    const int columns = 3;
    int matrix[rows][columns];

    for (int row = 0; row < rows; ++row)
    {
        for (int column = 0; column < columns; ++column)
        {
            cout << "Enter [" << row << "][" << column << "]: ";
            cin >> matrix[row][column];
        }
    }

    cout << "Matrix:\n";

    for (int row = 0; row < rows; ++row)
    {
        for (int column = 0; column < columns; ++column)
        {
            cout << matrix[row][column] << '\t';
        }
        cout << '\n';
    }

    return 0;
}
```

---

# 11.14 Matrix Addition

Two matrices add karne ke liye dimensions same hone chahiye.

$$C[i][j] = A[i][j] + B[i][j]$$

### Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    const int rows = 2;
    const int columns = 2;

    int first[rows][columns] = {{1, 2}, {3, 4}};
    int second[rows][columns] = {{5, 6}, {7, 8}};
    int sum[rows][columns] = {};

    for (int i = 0; i < rows; ++i)
    {
        for (int j = 0; j < columns; ++j)
        {
            sum[i][j] = first[i][j] + second[i][j];
        }
    }

    for (int i = 0; i < rows; ++i)
    {
        for (int j = 0; j < columns; ++j)
            cout << sum[i][j] << ' ';
        cout << '\n';
    }

    return 0;
}
```

---

# 11.15 Matrix Transpose

## 11.15.1 Meaning

Transpose mein rows columns aur columns rows ban jate hain.

$$T[j][i] = A[i][j]$$

### Example

```text
Original:       Transpose:
1 2 3           1 4
4 5 6           2 5
                3 6
```

---

# 11.16 Multidimensional Arrays

## 11.16.1 Meaning

Two se more indexing dimensions wala array multidimensional array hai.

```cpp
int data[2][3][4];
```

## 11.16.2 Access

```cpp
data[0][1][2] = 50;
```

## 11.16.3 Uses

- 3D coordinates
- Scientific data
- Image/video volumes
- Multiple tables
- Game boards and simulations

## 11.16.4 Traversal

Three-dimensional array ke liye three nested loops use hote hain.

---

# 11.17 Modern Array Containers

## 11.17.1 std::array

Fixed-size standard container jo size information preserve karta hai.

```cpp
#include <array>

std::array<int, 5> values = {10, 20, 30, 40, 50};
```

Useful functions: `size()`, `at()`, `front()`, `back()`.

## 11.17.2 std::vector

Dynamic-size standard container.

```cpp
#include <vector>

std::vector<int> values = {10, 20, 30};
values.push_back(40);
```

> Syllabus ke built-in arrays important foundation hain; modern C++ applications mein `std::array` aur `std::vector` safety aur convenience improve karte hain.

---

# 11.18 Common Mistakes

## 11.18.1 Out-of-Bounds Access

```cpp
int values[5];
values[5] = 10;  // Invalid; last valid index is 4
```

Built-in arrays automatic boundary checking nahi karte. Invalid access undefined behavior cause karta hai.

## 11.18.2 Uninitialized Elements

Local built-in array without initializer indeterminate values contain kar sakta hai.

```cpp
int values[5] = {};
```

## 11.18.3 Off-by-One Loop

```cpp
for (int i = 0; i <= size; ++i) // Wrong
for (int i = 0; i < size; ++i)  // Correct
```

## 11.18.4 Losing Size in Function Parameter

Array parameter ke saath size separately pass karein.

## 11.18.5 Wrong Matrix Bounds

Row loop rows tak aur column loop columns tak chalna chahiye.

## 11.18.6 Empty Array Assumption

Minimum/maximum logic se pehle ensure karein ki logical element count greater than zero hai.

---

# 11.19 Important Differences

## 11.19.1 Variable vs Array

| Variable | Array |
|---|---|
| One value | Multiple same-type values |
| Direct name access | Name plus index |
| Example: `mark` | Example: `marks[5]` |

## 11.19.2 One-Dimensional vs Two-Dimensional

| One-Dimensional | Two-Dimensional |
|---|---|
| One index | Row and column indexes |
| List-like | Table/matrix-like |
| `a[i]` | `a[i][j]` |

## 11.19.3 Built-in Array vs vector

| Built-in Array | std::vector |
|---|---|
| Fixed size | Dynamic size |
| Limited member operations | Rich member functions |
| Size often separately managed | `size()` available |

---

# 11.20 Chapter Summary

An array is a fixed-size collection of same-type elements stored in contiguous memory and accessed through zero-based indexes. One-dimensional arrays represent lists, while two-dimensional arrays represent rows and columns and higher-dimensional arrays model more complex data. Loops support input, output, traversal, aggregation, searching and sorting. Linear search checks elements sequentially, while bubble sort repeatedly compares adjacent elements. Arrays can be passed to functions, but built-in array parameters normally require size information separately. Matrix operations use nested loops. Correct bounds, initialization and dimension limits are essential because built-in arrays do not perform automatic boundary checking. Standard containers such as std::array and std::vector provide safer and more convenient alternatives for many modern programs.

---

# 11.21 Quick Revision

- Array same-type elements ka fixed collection hai.
- Built-in array elements contiguous memory mein hote hain.
- Index zero se start hota hai.
- Size n ke valid indexes 0 to n−1 hain.
- Loop se traversal, input aur output hota hai.
- Linear search one-by-one elements check karta hai.
- Bubble sort adjacent elements compare karta hai.
- Function ko array ke saath size pass karna useful hai.
- 2D array rows aur columns use karta hai.
- Matrix operations nested loops se hote hain.
- Out-of-bounds access undefined behavior cause karta hai.

---

# 11.22 Important Abbreviations

| Abbreviation | Full Form |
|---|---|
| 1D | One-Dimensional |
| 2D | Two-Dimensional |
| 3D | Three-Dimensional |
| STL | Standard Template Library |

---

# 11.23 Multiple-Choice Questions

1. Array elements ka data type kaisa hota hai?  
   A. Same  B. Always different  C. None  D. Only char  
   **✅ Answer: A**

2. Five-element array ka last valid index kya hai?  
   A. 5  B. 4  C. 3  D. 1  
   **✅ Answer: B**

3. Rows aur columns kis array mein hote hain?  
   A. 2D array  B. Scalar only  C. Function  D. Pointer only  
   **✅ Answer: A**

4. Sequential search ka naam kya hai?  
   A. Linear search  B. Bubble sort  C. Recursion  D. Linking  
   **✅ Answer: A**

5. Adjacent elements repeatedly compare karne wala basic sort?  
   A. Bubble sort  B. Linear search  C. DFS  D. Compiler  
   **✅ Answer: A**

6. Dynamic-size standard container kaunsa hai?  
   A. `std::vector`  B. Built-in scalar  C. `goto`  D. `switch`  
   **✅ Answer: A**

7. Built-in array boundary cross karne se kya ho sakta hai?  
   A. Undefined behavior  B. Guaranteed zero  C. Automatic resize  D. Always compile error  
   **✅ Answer: A**

---

# 11.24 Short-Answer Questions

1. Array ko define kijiye.
2. Array ki main characteristics likhiye.
3. Declaration aur initialization explain kijiye.
4. Zero-based indexing kya hai?
5. Traversal kya hai?
6. Linear search explain kijiye.
7. Bubble sort ka working likhiye.
8. Array ko function mein kaise pass karte hain?
9. 2D array declare aur initialize kijiye.
10. Row-major storage kya hai?
11. Multidimensional array ka use kya hai?
12. Out-of-bounds error explain kijiye.

---

# 11.25 Long-Answer and Exam Questions

1. One-dimensional array ko complete program ke saath explain kijiye.
2. Array input, output, sum aur average ka program likhiye.
3. Minimum aur maximum find karne ka algorithm/program likhiye.
4. Linear search ko program aur complexity ke saath explain kijiye.
5. Bubble sort ko passes aur program ke saath explain kijiye.
6. Arrays as function parameters explain kijiye.
7. Two-dimensional arrays ko matrix example ke saath samjhaiye.
8. Matrix addition ka C++ program likhiye.
9. Matrix transpose explain kijiye.
10. Built-in array, std::array aur vector compare kijiye.

---

# 11.26 Practice Programs

1. n elements input karke reverse order mein print kijiye.
2. Array mein even aur odd elements count kijiye.
3. Second-largest element find kijiye.
4. Target ki frequency count kijiye.
5. Array copy aur merge kijiye.
6. Ascending bubble sort likhiye.
7. 3×3 matrices add kijiye.
8. Matrix ke diagonal elements ka sum find kijiye.
9. Matrix transpose print kijiye.
10. Function se array average calculate kijiye.

---

# 11.27 Viva Questions

1. Array ka first index kya hota hai?
2. Array size 10 ka last index kya hai?
3. Same array mein different data types rakh sakte hain?
4. Array elements memory mein kaise stored hote hain?
5. Range-based for loop ka use kya hai?
6. Linear search kab stop hota hai?
7. Bubble sort mein largest element kahan move hota hai?
8. 2D array element ke liye kitne indexes chahiye?
9. Function parameter mein array size kyun pass karte hain?
10. vector built-in array se kaise different hai?

---

<div align="center">

## ✅ Chapter 11 Complete

[⬅️ Previous Chapter](chapter-10-functions-and-structured-programming.md) · [📚 Table of Contents](../SUMMARY.md) · **Next: Pointers ➡️**

</div>
