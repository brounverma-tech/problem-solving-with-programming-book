<div align="center">

# 👉 Chapter 12: Pointers

### 🔴 Unit D — Functions, Arrays and Pointers in C++

![Level](https://img.shields.io/badge/Level-Intermediate%20to%20Advanced-red?style=flat-square)
![Language](https://img.shields.io/badge/Explanation-English%20%2B%20Hinglish-blue?style=flat-square)
![Code](https://img.shields.io/badge/Programs-C%2B%2B-purple?style=flat-square)

</div>

---

## 🎯 Learning Objectives

Is chapter ko complete karne ke baad aap:

- Pointer aur memory address ko define kar sakenge.
- Address-of aur dereference operators use kar sakenge.
- Null, wild aur dangling pointers samajh sakenge.
- Pointer compatibility aur const combinations explain kar sakenge.
- Pointer-to-pointer declare aur use kar sakenge.
- Arrays aur pointers ka relationship samajh सकेंगे.
- Pointer arithmetic safely perform kar सकेंगे.
- Dynamic memory ko `new`/`delete` se manage kar सकेंगे.
- Array of pointers, void pointers aur function pointers use kar सकेंगे.
- Command-line arguments explain kar सकेंगे.

---

# 12.1 Introduction to Pointers

## 12.1.1 Memory Address

Computer memory bytes/locations mein organized hoti hai. Har location ka unique address hota hai.

## 12.1.2 Meaning of Pointer

> A pointer is a variable that stores the memory address of another object or function.

**Hinglish:** Normal variable value store karta hai, jabki pointer kisi value ke memory address ko store karta hai.

## 12.1.3 Need for Pointers

- Dynamic memory allocation
- Arrays aur strings processing
- Call by address/reference-like operations
- Efficient large-data access
- Linked data structures
- Hardware aur low-level programming
- Function callbacks

## 12.1.4 Important Terms

| Term | Pronunciation | Meaning |
|---|---|---|
| Pointer | पॉइंटर | Address store karne wala variable |
| Address | एड्रेस | Memory location identity |
| Dereference | डीरेफरेंस | Pointer ke address par stored value access karna |
| Null Pointer | नल पॉइंटर | Kisi valid object ko point na karne wala pointer |
| Dangling Pointer | डैंगलिंग पॉइंटर | Invalid/destroyed object ka old address |
| Dynamic Memory | डायनेमिक मेमोरी | Runtime par allocated memory |
| Heap | हीप | Dynamic storage area |

---

# 12.2 Pointer Declaration and Initialization

## 12.2.1 Declaration

### Syntax

```cpp
dataType* pointerName;
```

### Examples

```cpp
int* integerPointer;
double* pricePointer;
char* characterPointer;
```

## 12.2.2 Address-of Operator

`&` variable ka address obtain karta hai.

```cpp
int value = 25;
int* pointer = &value;
```

## 12.2.3 Dereference Operator

`*` pointer ke stored address par present value access karta hai.

```cpp
cout << *pointer;  // 25
```

## 12.2.4 Complete Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    int value = 25;
    int* pointer = &value;

    cout << "Value = " << value << '\n';
    cout << "Address = " << &value << '\n';
    cout << "Pointer stores = " << pointer << '\n';
    cout << "Dereferenced value = " << *pointer << '\n';

    return 0;
}
```

## 12.2.5 Modifying Value Through Pointer

```cpp
int value = 10;
int* pointer = &value;

*pointer = 50;
cout << value;  // 50
```

---

# 12.3 Pointer Types and Compatibility

## 12.3.1 Typed Pointers

Pointer type pointed object type se compatible hona chahiye.

```cpp
int number = 10;
int* pointer = &number;
```

## 12.3.2 Incompatible Assignment

```cpp
double price = 9.5;
int* pointer = &price;  // Invalid type mismatch
```

Correct:

```cpp
double* pointer = &price;
```

## 12.3.3 Pointer Size

Different pointed types ke pointer sizes same implementation par often same hote hain, lekin standard assumptions ke badle `sizeof` se check karein.

```cpp
cout << sizeof(int*) << '\n';
cout << sizeof(double*) << '\n';
```

## 12.3.4 Pointer Conversion

Implicit conversions limited aur type-safe rules follow karti hain. Unrelated object pointer types ko directly assign nahi karna chahiye. Unsafe casts bugs aur undefined behavior cause kar sakte hain.

---

# 12.4 Null, Wild and Dangling Pointers

## 12.4.1 Null Pointer

Kisi valid object ko point nahi karta.

```cpp
int* pointer = nullptr;
```

Use se pehle check:

```cpp
if (pointer != nullptr)
{
    cout << *pointer;
}
```

## 12.4.2 Wild Pointer

Uninitialized pointer jisme indeterminate address ho sakta hai.

```cpp
int* pointer;  // Do not dereference
```

Initialize karein:

```cpp
int* pointer = nullptr;
```

## 12.4.3 Dangling Pointer

Pointer aise object/memory ko refer kare jo destroy/deallocate ho chuki ho.

```cpp
int* pointer = new int(10);
delete pointer;
pointer = nullptr;
```

## 12.4.4 Invalid Dereference

Null, wild ya dangling pointer dereference karna undefined behavior cause kar sakta hai.

---

# 12.5 Pointers and Functions

## 12.5.1 Pointer Parameter

Function pointer ke through caller variable modify kar sakta hai.

### Program: Swap Using Pointers

```cpp
#include <iostream>
using namespace std;

void swapNumbers(int* first, int* second)
{
    int temporary = *first;
    *first = *second;
    *second = temporary;
}

int main()
{
    int a = 10;
    int b = 20;

    swapNumbers(&a, &b);

    cout << "a = " << a << '\n';
    cout << "b = " << b << '\n';
    return 0;
}
```

## 12.5.2 Pointer vs Reference Parameter

| Pointer Parameter | Reference Parameter |
|---|---|
| Address explicitly pass | Variable directly pass |
| Null possible | Normally valid object bound |
| Dereference required | Normal variable syntax |
| `int* p` | `int& r` |

## 12.5.3 Returning a Pointer

Function dynamically allocated memory ya sufficiently long-lived object ka pointer return kar sakta hai, but local automatic variable ka address return nahi karna chahiye.

```cpp
int* wrong()
{
    int local = 10;
    return &local;  // Wrong: local is destroyed
}
```

---

# 12.6 Pointer to Pointer

## 12.6.1 Meaning

> A pointer to pointer stores the address of another pointer.

## 12.6.2 Declaration

```cpp
int** doublePointer;
```

## 12.6.3 Example

```cpp
int value = 50;
int* pointer = &value;
int** pointerToPointer = &pointer;

cout << value << '\n';               // 50
cout << *pointer << '\n';            // 50
cout << **pointerToPointer << '\n';   // 50
```

## 12.6.4 Uses

- Pointer ko function mein modify karna
- Dynamic 2D structures
- Command-line argument representation
- Multi-level indirect data access

---

# 12.7 const and Pointers

## 12.7.1 Pointer to Const Data

Pointer ke through pointed value modify nahi kar sakte.

```cpp
const int* pointer = &value;
```

Pointer another compatible object ko point kar sakta hai.

## 12.7.2 Const Pointer

Pointer ka stored address change nahi kar sakte, pointed value modify ho sakti hai.

```cpp
int* const pointer = &value;
```

## 12.7.3 Const Pointer to Const Data

Na pointer address change aur na pointed value pointer ke through modify.

```cpp
const int* const pointer = &value;
```

## 12.7.4 Comparison

| Declaration | Pointer Changes? | Data Changes Through Pointer? |
|---|:---:|:---:|
| `const int* p` | Yes | No |
| `int* const p` | No | Yes |
| `const int* const p` | No | No |

---

# 12.8 Arrays and Pointers

## 12.8.1 Array-to-Pointer Conversion

Many expressions mein array name first element ke pointer mein convert hota hai.

```cpp
int values[] = {10, 20, 30, 40};
int* pointer = values;
```

## 12.8.2 Element Access

```cpp
cout << values[0];      // 10
cout << *pointer;       // 10
cout << *(pointer + 1); // 20
```

Relationship:

$$values[i] = *(values+i)$$

## 12.8.3 Traversal with Pointer

```cpp
int values[] = {10, 20, 30, 40};
int* pointer = values;

for (int i = 0; i < 4; ++i)
{
    cout << *(pointer + i) << ' ';
}
```

## 12.8.4 Array and Pointer Difference

| Array | Pointer |
|---|---|
| Fixed array object/storage | Address-storing variable |
| Array name assign nahi hota | Pointer another address le sakta hai |
| `sizeof(array)` full array size in same scope | `sizeof(pointer)` pointer size |
| Related but not identical | Related but not identical |

---

# 12.9 Pointer Arithmetic

## 12.9.1 Increment

`pointer++` next element par move karta hai, next byte necessarily nahi; movement pointed type size ke according hota hai.

## 12.9.2 Decrement

`pointer--` previous element par move karta hai within valid array range.

## 12.9.3 Addition and Subtraction

```cpp
pointer + n
pointer - n
```

## 12.9.4 Pointer Difference

Same array ke two pointers subtract karne par element-distance mil sakta hai.

```cpp
int* first = &values[1];
int* second = &values[4];

cout << second - first;  // 3
```

## 12.9.5 Pointer Comparison

Same array/range ke pointers ko position relationship ke context mein compare kiya ja sakta hai.

## 12.9.6 Safety Rules

- Arithmetic only valid array/object range mein karein.
- One-past-the-end pointer form ho sakta hai, dereference nahi.
- Unrelated pointers subtract/order compare na karein.
- Out-of-bounds dereference undefined behavior hai.

---

# 12.10 Dynamic Memory Allocation

## 12.10.1 Meaning

Runtime par required memory heap/free store se allocate karna dynamic memory allocation hai.

## 12.10.2 new Operator

Single object allocate:

```cpp
int* pointer = new int;
*pointer = 25;
```

Initialize directly:

```cpp
int* pointer = new int(25);
```

## 12.10.3 delete Operator

```cpp
delete pointer;
pointer = nullptr;
```

## 12.10.4 Dynamic Array

```cpp
int size;
cin >> size;

int* values = new int[size];
```

Release:

```cpp
delete[] values;
values = nullptr;
```

## 12.10.5 Complete Program

```cpp
#include <iostream>
using namespace std;

int main()
{
    int size;
    cout << "Enter size: ";
    cin >> size;

    if (size <= 0)
    {
        cout << "Invalid size";
        return 1;
    }

    int* values = new int[size];
    long long sum = 0;

    for (int i = 0; i < size; ++i)
    {
        cin >> values[i];
        sum += values[i];
    }

    cout << "Sum = " << sum;

    delete[] values;
    values = nullptr;
    return 0;
}
```

## 12.10.6 Memory Leak

Allocated memory release na hone par memory leak hota hai.

## 12.10.7 Double Delete

Same allocation ko twice delete karna undefined behavior hai.

## 12.10.8 new/delete Matching

| Allocation | Deallocation |
|---|---|
| `new Type` | `delete pointer` |
| `new Type[n]` | `delete[] pointer` |

---

# 12.11 C-Style Memory Allocation Functions

Header: `<cstdlib>`

## 12.11.1 malloc

Raw uninitialized bytes allocate karta hai.

## 12.11.2 calloc

Multiple objects ke liye zero-initialized raw storage allocate karta hai.

## 12.11.3 realloc

Existing C allocation ka size change karne ki attempt karta hai.

## 12.11.4 free

`malloc`/`calloc`/`realloc` family se allocated storage release karta hai.

## 12.11.5 C++ Guidance

- `malloc` constructors call nahi karta.
- `free` destructors call nahi karta.
- `new` ko `free` aur `malloc` ko `delete` ke saath mix na karein.
- Modern C++ mein containers aur smart pointers prefer karein.

---

# 12.12 Smart Pointers

## 12.12.1 Need

Manual `new`/`delete` errors reduce karne ke liye standard smart pointers automatic ownership management provide karte hain.

## 12.12.2 unique_ptr

Single ownership represent karta hai.

```cpp
#include <memory>

auto pointer = std::make_unique<int>(25);
```

## 12.12.3 shared_ptr

Shared ownership with reference counting.

## 12.12.4 weak_ptr

Non-owning observer jo shared ownership cycles avoid karne mein help karta hai.

> Beginner syllabus ke raw pointers samajhna important hai, lekin resource ownership ke liye modern C++ mein RAII, containers aur smart pointers safer hain.

---

# 12.13 Array of Pointers

## 12.13.1 Meaning

Array jiske each element ka type pointer ho.

```cpp
int* pointers[3];
```

## 12.13.2 Example

```cpp
int a = 10;
int b = 20;
int c = 30;

int* pointers[] = {&a, &b, &c};

for (int i = 0; i < 3; ++i)
{
    cout << *pointers[i] << ' ';
}
```

## 12.13.3 Array of C-Style Strings

```cpp
const char* names[] = {"Aman", "Broun", "Chetan"};
```

Modern C++ mein `std::string` container often easier aur safer hai.

---

# 12.14 Void Pointers

## 12.14.1 Meaning

> A void pointer can hold the address of an object of any object type, but it has no direct pointed type information.

```cpp
int value = 10;
void* genericPointer = &value;
```

## 12.14.2 Dereferencing

Void pointer directly dereference nahi hota. Correct type mein convert karna padta hai.

```cpp
int* integerPointer = static_cast<int*>(genericPointer);
cout << *integerPointer;
```

## 12.14.3 Limitations

- Direct dereference allowed nahi.
- Pointer arithmetic directly valid nahi.
- Type safety lost ho sakti hai.
- Incorrect cast undefined behavior cause kar sakta hai.

## 12.14.4 Use

Low-level generic C interfaces aur raw memory APIs mein mil sakta hai. Modern typed abstractions generally safer hain.

---

# 12.15 Function Pointers

## 12.15.1 Meaning

Function pointer function ka address store karta hai.

## 12.15.2 Declaration

```cpp
int (*operation)(int, int);
```

## 12.15.3 Example

```cpp
int add(int a, int b)
{
    return a + b;
}

int subtract(int a, int b)
{
    return a - b;
}

int main()
{
    int (*operation)(int, int) = add;
    cout << operation(10, 5) << '\n';

    operation = subtract;
    cout << operation(10, 5) << '\n';
}
```

## 12.15.4 Uses

- Callbacks
- Operation selection
- Event handling
- Sorting/comparison functions
- Function tables

## 12.15.5 Type Alias

```cpp
using Operation = int (*)(int, int);
Operation function = add;
```

---

# 12.16 Command-Line Arguments

## 12.16.1 Meaning

Program start karte time command line se supplied values command-line arguments hain.

## 12.16.2 main Signature

```cpp
int main(int argc, char* argv[])
```

## 12.16.3 argc

Arguments ki count, normally program name including.

## 12.16.4 argv

C-style strings ka array, jisme argument text hota hai.

## 12.16.5 Program

```cpp
#include <iostream>
using namespace std;

int main(int argc, char* argv[])
{
    cout << "Argument count = " << argc << '\n';

    for (int i = 0; i < argc; ++i)
    {
        cout << "argv[" << i << "] = " << argv[i] << '\n';
    }

    return 0;
}
```

### Example Run

```text
program hello 25
```

Possible values:

```text
argv[0] = program
argv[1] = hello
argv[2] = 25
```

## 12.16.6 Conversion

Arguments strings hote hain. Numeric conversion ke liye validated methods, such as `std::stoi`, use kiye ja sakte hain with error handling.

---

# 12.17 Pointer Applications

## 12.17.1 Dynamic Data Structures

Linked lists, trees aur graphs nodes ko pointers/smart pointers se connect kar sakte hain.

## 12.17.2 Efficient Function Communication

Large data copy avoid aur caller data modify karna.

## 12.17.3 Dynamic Arrays

Runtime-size storage allocate karna.

## 12.17.4 Hardware Access

Embedded/system programming mein mapped memory aur device registers access.

## 12.17.5 Callbacks

Function pointers/callables se behavior dynamically select karna.

---

# 12.18 Common Pointer Errors

## 12.18.1 Null Dereference

`nullptr` ko dereference karna invalid hai.

## 12.18.2 Wild Pointer Use

Uninitialized pointer use na karein.

## 12.18.3 Dangling Pointer Use

Deleted/out-of-scope object ka address access na karein.

## 12.18.4 Memory Leak

Owned allocated memory release na karna.

## 12.18.5 Double Delete

Same memory ko twice release karna.

## 12.18.6 Mismatched Deallocation

`new[]` with `delete[]` aur `new` with `delete` match karein.

## 12.18.7 Out-of-Bounds Arithmetic

Pointer ko valid array range ke outside dereference na karein.

## 12.18.8 Wrong Format or Type Cast

Incorrect cast pointed object type ko change nahi karta; unsafe access undefined behavior cause kar sakta hai.

---

# 12.19 Pointer Safety Best Practices

1. Pointer ko initialize karein, preferably `nullptr` se.
2. Dereference se pehle validity check karein.
3. Ownership clear rakhein.
4. Manual allocation ko correct delete se match karein.
5. Delete ke baad pointer ko `nullptr` set karein where useful.
6. Raw owning pointers ke badle containers/smart pointers prefer karein.
7. `const` correctness use karein.
8. Pointer arithmetic only valid arrays/ranges mein karein.
9. Local object ka pointer/reference return na karein.
10. Compiler warnings aur sanitizers use karein when available.

---

# 12.20 Important Differences

## 12.20.1 Pointer vs Normal Variable

| Normal Variable | Pointer |
|---|---|
| Direct value store | Address store |
| `int value` | `int* pointer` |
| Name se value access | Dereference se pointed value |

## 12.20.2 Null vs Dangling Pointer

| Null Pointer | Dangling Pointer |
|---|---|
| Valid object ko point nahi karta | Invalid old object/memory ko point karta hai |
| Explicit `nullptr` | Deletion/scope exit ke baad ho sakta hai |
| Checkable safe state | Dangerous if used |

## 12.20.3 Static vs Dynamic Array

| Fixed Built-in Array | Dynamic Array |
|---|---|
| Size compile-time/fixed context | Size runtime par select |
| Automatic/static storage possible | `new[]` allocated |
| Automatic cleanup if local object | Manual `delete[]` required for raw pointer |

## 12.20.4 Array of Pointers vs Pointer to Array

| Array of Pointers | Pointer to Array |
|---|---|
| Multiple pointer elements | Complete array object ko point |
| `int* p[5]` | `int (*p)[5]` |

---

# 12.21 Chapter Summary

A pointer is a variable that stores the address of another object or function. The address-of operator obtains an address and the dereference operator accesses the pointed value. Pointer type compatibility, initialization and lifetime are essential because null, wild and dangling pointers must not be dereferenced. Pointers support function communication, multi-level indirection, arrays and pointer arithmetic within valid ranges. Dynamic memory can be allocated with new and released with delete, while arrays require new[] and delete[]. C allocation functions must not be mixed with C++ deallocation. Arrays of pointers store multiple addresses, void pointers provide untyped object addresses and function pointers enable callbacks. Command-line arguments arrive through argc and argv. Modern C++ reduces ownership errors through containers, RAII and smart pointers.

---

# 12.22 Quick Revision

- Pointer another object/function ka address store karta hai.
- `&` address aur `*` dereferenced value deta hai.
- Pointer type pointed object se compatible hona chahiye.
- `nullptr` safe empty pointer state hai.
- Pointer-to-pointer another pointer ka address store karta hai.
- Array name many expressions mein first element pointer ban jata hai.
- Pointer arithmetic element size ke according move karti hai.
- `new`/`delete` aur `new[]`/`delete[]` correctly match hone chahiye.
- Void pointer direct dereference nahi hota.
- Function pointer callback/operation select kar sakta hai.
- `argc` count aur `argv` argument strings contain karta hai.

---

# 12.23 Important Abbreviations

| Abbreviation | Full Form |
|---|---|
| RAII | Resource Acquisition Is Initialization |
| CLI | Command-Line Interface |
| API | Application Programming Interface |
| RAM | Random Access Memory |

---

# 12.24 Multiple-Choice Questions

1. Pointer kya store karta hai?  
   A. Address  B. Only character  C. Loop  D. Header  
   **✅ Answer: A**

2. Address-of operator kaunsa hai?  
   A. `&`  B. `*`  C. `%`  D. `&&`  
   **✅ Answer: A**

3. Dereference operator kaunsa hai?  
   A. `*`  B. `&`  C. `::`  D. `?`  
   **✅ Answer: A**

4. Safe empty pointer literal kaunsa hai?  
   A. `nullptr`  B. `goto`  C. `void` only  D. `case`  
   **✅ Answer: A**

5. Dynamic array release kaise hoti hai?  
   A. `delete[]`  B. `delete` only  C. `free` after new  D. Automatically always  
   **✅ Answer: A**

6. Void pointer direct dereference hota hai?  
   A. No  B. Always  C. Only without type  D. It is an integer  
   **✅ Answer: A**

7. Command-line argument count kahan hoti hai?  
   A. `argc`  B. `argv` only  C. `cout`  D. `main` name  
   **✅ Answer: A**

8. Same allocation ko twice delete karna kya hai?  
   A. Undefined behavior risk  B. Required practice  C. Initialization  D. Overloading  
   **✅ Answer: A**

---

# 12.25 Short-Answer Questions

1. Pointer ko define kijiye.
2. Address-of aur dereference operators explain kijiye.
3. Pointer declaration aur initialization likhiye.
4. Null, wild aur dangling pointer compare kijiye.
5. Pointer compatibility kya hai?
6. Pointer-to-pointer explain kijiye.
7. Const pointer combinations likhiye.
8. Arrays aur pointers ka relation samjhaiye.
9. Pointer arithmetic ke rules likhiye.
10. Memory leak aur double delete kya hain?
11. Void pointer kya hai?
12. Function pointer ka use kya hai?
13. argc aur argv explain kijiye.

---

# 12.26 Long-Answer and Exam Questions

1. Pointers ko memory diagram aur program ke saath explain kijiye.
2. Pointer parameters se swap program likhiye.
3. Pointer-to-pointer ko example ke saath samjhaiye.
4. Arrays and pointers relationship explain kijiye.
5. Pointer arithmetic aur safety rules explain kijiye.
6. Dynamic memory allocation using new/delete describe kijiye.
7. C-style memory functions aur C++ allocation compare kijiye.
8. Array of pointers aur void pointers explain kijiye.
9. Function pointers ko callback example ke saath explain kijiye.
10. Command-line arguments ka program likhiye.
11. Common pointer errors aur safety practices discuss kijiye.

---

# 12.27 Practice Programs

1. Pointer se variable display aur modify kijiye.
2. Pointers se two numbers swap kijiye.
3. Pointer traversal se array sum calculate kijiye.
4. Pointer se maximum array element find kijiye.
5. Runtime-size dynamic array input aur average calculate kijiye.
6. Pointer-to-pointer value display kijiye.
7. Array of pointers se three variables print kijiye.
8. Function pointer se arithmetic operation select kijiye.
9. Command-line arguments print kijiye.
10. `std::unique_ptr` se dynamic integer manage kijiye.

---

# 12.28 Viva Questions

1. Pointer aur address mein kya relation hai?
2. `int* p` mein star ka kya role hai?
3. Dereference kab unsafe hai?
4. nullptr use kyun karte hain?
5. Dangling pointer kaise banta hai?
6. `values[i]` ka pointer form kya hai?
7. Pointer increment kitne bytes move karta hai?
8. new aur delete kyun match hone chahiye?
9. malloc aur new same hain?
10. Function pointer kya store karta hai?
11. argv ka type kya represent karta hai?
12. Smart pointers kyun useful hain?

---

<div align="center">

## ✅ Chapter 12 Complete

[⬅️ Previous Chapter](chapter-11-arrays.md) · [📚 Table of Contents](../SUMMARY.md) · **Course Chapters Complete 🎉**

</div>
