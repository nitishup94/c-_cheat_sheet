
# 📘 C++ Programming Cheat Sheet

Welcome to the **C++ Quick Reference** 🚀  
This repo contains **syntax, examples, and STL functions** you need for coding interviews, DSA, and competitive programming.  


## 📑 Table of Contents

1. [Basic Input/Output](#1-🖥-basic-inputoutput)  
2. [Data Types](#2-🔢-data-types)  
    - [Fundamental / Basic Types](#21-fundamental--basic-data-types)  
    - [Derived Types](#22-derived-types)  
      - [Array](#221-array)  
      - [Pointer](#222-pointer)  
      - [Reference](#223-reference)  
      - [Function](#224-function)  
    - [User-defined Types](#23-user-defined-types)  
      - [Struct](#231-struct)  
      - [Class](#232-class)  
      - [Enum](#233-enum)  
      - [Typedef](#234-typedef)  
      - [Using (Alias Declaration)](#235-using-alias-declaration)  
3. [Control Statements](#3-control-statements)  
    - [If-Else](#31-if-else)  
    - [Switch-Case](#32-switch-case)  
    - [Loops](#33-🔄-loops)  
      - [For Loop](#1-for-loop)  
      - [While Loop](#2-while-loop)  
      - [Do-While Loop](#3-do-while-loop)  
    - [Break & Continue](#34-break--continue)  
    - [Goto Statement](#35-goto-statement)  
4. [Functions](#4-functions)  
    - [Function Declaration & Definition](#41-function-declaration--definition)  
    - [Call by Value](#42-call-by-value)  
    - [Call by Reference](#43-call-by-reference)  
    - [Inline Functions](#44-inline-functions)  
    - [Default Arguments](#45-default-arguments)  
    - [Function Overloading](#46-function-overloading)  
    - [Recursion](#47-recursion)  
5. [STL (Standard Template Library)](#5-stl-standard-template-library)  
    - [Vector](#51-vector)  
    - [Map](#52-map)  
    - [Set](#53-set)  
    - [Queue](#54-queue)  
    - [Stack](#55-stack)  
    - [Priority Queue (Heap)](#56-priority-queue-heap)  
    - [Algorithms](#57-algorithms)  
6. [Pointers & References](#6-pointers--references)  
    - [Pointers Basics](#61-pointers-basics)  
    - [Pointer Arithmetic](#62-pointer-arithmetic)  
    - [Pointer to Pointer](#63-pointer-to-pointer)  
    - [Null Pointer & Dangling Pointer](#64-null-pointer--dangling-pointer)  
7. [OOP in C++](#7-🏛-oop-in-c)  
    - [Class & Object](#71-class--object)  
    - [Constructors & Destructors](#72-constructors--destructors)  
    - [Inheritance](#73-inheritance)  
      - [Single](#731-single-inheritance)  
      - [Multiple](#732-multiple-inheritance)  
      - [Multilevel](#733-multilevel-inheritance)  
      - [Hierarchical](#734-hierarchical-inheritance)  
    - [Polymorphism](#74-polymorphism)  
      - [Compile-time (Function Overloading / Operator Overloading)](#741-compile-time-polymorphism-function-overloading--operator-overloading)  
      - [Run-time (Virtual Functions)](#742-run-time-polymorphism-virtual-functions)  
    - [Encapsulation & Abstraction](#75-encapsulation--abstraction)  
    - [Friend Functions & Classes](#76-friend-functions--classes)  
    - [Static Members](#77-static-members)  

---

## 1. 🖥 Basic Input/Output
```cpp
#include <iostream>
using namespace std;

int main() {
    int x;
    cout << "Enter a number: ";
    cin >> x;
    cout << "You entered: " << x << endl;
}
```
---
## 2. 🔢 Data Types

### 2.1 Fundamental / Basic Data Types
C++ provides several **built-in fundamental types** to store basic data values.

---

#### List of Basic Types

**Primitive Data Types in C++** 

| Type     | Description                        | Size (approx) |
|----------|------------------------------------|---------------|
| `int`    | Stores integers                    | 4 bytes       |
| `float`  | Stores decimal numbers (~6 precision)  | 4 bytes       |
| `double` | Stores large decimal numbers (~15 precision) | 8 bytes       |
| `char`   | Stores a single character          | 1 byte        |
| `string` | Stores sequence of characters      | Variable      |
| `bool`   | Stores `true` or `false`           | 1 byte        |
| `void`   | Represents no value (used in functions) | 0 bytes       |

---

#### Example Code
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    float b = 3.14;
    double c = 2.718281828;
    char d = 'A';
    string e = "Hello C++";
    bool f = true;

    cout << "int: " << a << "\n";
    cout << "float: " << b << "\n";
    cout << "double: " << c << "\n";
    cout << "char: " << d << "\n";
    cout << "string: " << e << "\n";
    cout << "bool: " << f << "\n";

    return 0;
}
```

**Tricky Examples**
---
#### Q1: Char and ASCII

```cpp
#include <iostream>
using namespace std;

int main() {
char ch = 65;
cout << ch;
   return 0;
}
```
**Output:** A  
**Explanation:** 65 is the ASCII value of 'A'.

#### Q2: Boolean Conversion

```cpp
#include <iostream>
using namespace std;

int main() {
    bool b1 = 10;
    bool b2 = 0;
    cout << b1 << " " << b2;
    return 0;
}
```
Output: 1 0  
Explanation: Any non-zero integer converts to true (1) and zero to false (0).

---

#### Q3: Integer Division

```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 7, y = 2;
    cout << x / y;
    return 0;
}
```
Output: 3  
Explanation: Dividing two integers truncates the decimal part.

---

#### Q4: Implicit Conversion

```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 5;
    double y = 2.0;
    cout << x / y;
    return 0;
}
```
Output: 2.5  
Explanation: When an int is used with a double, the int is promoted to double, resulting in floating-point division.


### 2.2 Derived Types

Derived types in C++ build upon basic types to create more complex data structures. This section covers arrays, pointers, references, and functions.

## 2.2.1. Array

Arrays store a fixed-size sequential collection of elements of the same type.

Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    // Iterate over the array
    for(int i = 0; i < 5; i++) {
        cout << "Element " << i << ": " << arr[i] << "\n";
    }
    return 0;
}
```

## 2.2.2. Pointer

Pointers are variables that store memory addresses. They allow dynamic memory management and manipulation of data addresses.

Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 25;
    int *ptr = &x; // pointer holds the address of x
    cout << "Value of x: " << x << "\n";
    cout << "Address of x: " << ptr << "\n";
    cout << "Value at ptr: " << *ptr << "\n"; // dereferencing
    return 0;
}
```

## 2.2.3. Reference

References are aliases for existing variables. Once initialized, a reference cannot be reseated.

Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 100;
    int &ref = a;  // ref is a reference to a
    ref = 200;     // changes the value of a
    cout << "Value of a: " << a << "\n";
    cout << "Value via ref: " << ref << "\n";
    return 0;
}
```

## 2.2.4. Function

In C++, functions can be treated as first-class entities using pointers. Function pointers allow functions to be passed as arguments or stored for callback purposes.

Example:
```cpp
#include <iostream>
using namespace std;

int add(int a, int b) {
    return a + b;
}

int execute(int (*func)(int, int), int x, int y) {
    return func(x, y);
}

int main() {
    int result = execute(add, 5, 3);
    cout << "Result: " << result << "\n";
    return 0;
}
```

---

## Tricky Interview Questions

1. Q: How can you dynamically allocate an array and what must you not forget to do afterward?  
   A: Use the `new` keyword to allocate and `delete[]` to free the memory.  
   Example:
   ```cpp
   int* arr = new int[10]; // allocate
   // Use the array
   delete[] arr; // free the memory
   ```

2. Q: Explain the difference between pointers and references?  
   A: A pointer can be reassigned and can be null, while a reference is an alias for an already initialized variable and cannot be reseated.

3. Q: How can a function pointer be used to implement callback mechanisms in C++?  
   A: By passing a function pointer to another function, you can call the function dynamically during runtime.  
   (See the function pointer example above.)

4. Q: What are potential pitfalls when using pointers and how would you avoid them?  
   A: Issues include dereferencing null or dangling pointers and memory leaks. Ensure initialization, proper deletion, and avoid using pointers after freeing memory.



## 2.3  User-defined Types

C++ allows the creation of custom types to better model real-world data and improve code clarity. The most common user-defined types are:

---

### 2.3.1. struct

A struct is a composite data type that groups variables under a single name. Members of a struct are public by default.

**Example Code:**

```cpp
#include <iostream>
using namespace std;

struct Person {
    string name;
    int age;
};

int main() {
    Person p = {"Alice", 30};
    cout << "Name: " << p.name << "\nAge: " << p.age << "\n";
    return 0;
}
```

**Interview Question:**
Q: What is the default access specifier for members of a struct?  
A: Public.

---

### 2.3.2. class

A class is similar to a struct, but members are private by default. It supports encapsulation, inheritance, and polymorphism.

**Example Code:**

```cpp
#include <iostream>
using namespace std;

class Rectangle {
private:
    int width, height;
public:
    Rectangle(int w, int h) : width(w), height(h) {}
    int area() {
        return width * height;
    }
};

int main() {
    Rectangle rect(10, 5);
    cout << "Area: " << rect.area() << "\n";
    return 0;
}
```

**Interview Question:**
Q: How do classes and structs differ in C++?  
A: The only difference is the default access level (private for classes, public for structs).

---

### 2.3.3. enum

An enum defines a type for a set of named integral constants, improving code readability.

**Example Code:**

```cpp
#include <iostream>
using namespace std;

enum Color { RED, GREEN, BLUE };

int main() {
    Color myColor = GREEN;
    cout << "Color value: " << myColor << "\n";  // Displays underlying integer value
    return 0;
}
```

**Interview Question:**
Q: What are the benefits of using enums over plain integer constants?  
A: Enums offer better type safety and a clear list of named constants.

---

### 2.3.4. typedef

`typedef` creates an alias for a type, making complex declarations simpler or improving code readability.

**Example Code:**

```cpp
#include <iostream>
using namespace std;

typedef unsigned long ulong;

int main() {
    ulong population = 7800000000;
    cout << "World population: " << population << "\n";
    return 0;
}
```

**Interview Question:**
Q: When would you use `typedef` in C++?  
A: To simplify complex type declarations or improve code clarity by providing descriptive names for types.

---

### 2.3.5. using (Alias Declaration)

The `using` keyword, introduced in C++11, can also create type aliases. It is often preferred over `typedef` due to its clearer syntax, especially with templates.

**Example Code:**

```cpp
#include <iostream>
using namespace std;

using uint = unsigned int;

int main() {
    uint count = 100;
    cout << "Count: " << count << "\n";
    return 0;
}
```

**Interview Question:**
Q: How does the `using` keyword improve clarity compared to `typedef`?  
A: The `using` syntax is more intuitive and works better with template declarations, providing clearer and more maintainable alias definitions.

---
## 3. Control Statements

Control statements manage the flow of execution in your programs. Below are explanations, examples, and common interview questions for two popular control constructs: If-Else and Switch-Case.

---

### 3.1 If-Else

The if-else statement evaluates a boolean condition. If the condition is true, the corresponding block is executed; otherwise, an alternative block (if provided) is executed.

**Example Code:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int num = 5;
    if (num % 2 == 0) {
        cout << num << " is even." << "\n";
    } else {
        cout << num << " is odd." << "\n";
    }
    return 0;
}
```

**Interview Questions:**

1. Q: How does an if-else statement work in C++?  
   A: It evaluates a condition; if true, executes one block of code; otherwise, executes another block if provided.

2. Q: What happens if the condition in an if-else is not properly enclosed in parentheses?  
   A: The code may not compile; proper syntax is required for evaluation.

---

### 3.2 Switch-Case

The switch-case construct is useful when a variable is compared against multiple constant values. It provides a clean approach to execute different code blocks based on the variable's value.

**Example Code:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int day = 3;
    switch (day) {
        case 1:
            cout << "Monday" << "\n";
            break;
        case 2:
            cout << "Tuesday" << "\n";
            break;
        case 3:
            cout << "Wednesday" << "\n";
            break;
        default:
            cout << "Other Day" << "\n";
    }
    return 0;
}
```

**Interview Questions:**

1. Q: What is the benefit of using switch-case over multiple if-else conditions?  
   A: Switch-case enhances readability and often makes the code more efficient when checking multiple discrete values.

2. Q: What is fallthrough in a switch-case statement and how can it be managed?  
   A: Fallthrough occurs when the break statement is omitted, causing execution to continue to subsequent cases. Proper use of break or explicit case handling is needed to manage this behavior.
## 3.3 🔄 Loops

Loops allow you to execute a block of code repeatedly based on a condition. They are invaluable for iterating over data or executing code until a specific state is achieved.

### 1. For Loop

A for loop is ideal when the number of iterations is known. It combines initialization, condition-checking, and iteration in a single line.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    // Iterate from 0 to 4
    for (int i = 0; i < 5; i++) {
        cout << "Iteration " << i << "\n";
    }
    return 0;
}
```

**Interview Questions with Answers:**
- Q: What components are included in a for loop and why is it preferred when the iteration count is known?  
  A: A for loop includes initialization, a condition, and an iteration expression. Its compact structure makes it ideal when the number of iterations is predetermined.
- Q: How would you modify the loop if you wanted to decrement the counter instead?  
  A: Replace the increment expression (i++) with a decrement (i--) and adjust the condition (e.g., start from a higher value and check if i >= 0).

---

### 2. While Loop

A while loop continues executing as long as its condition remains true. It is preferred when the number of iterations is not predetermined.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;
    // Continue until i is less than 5
    while (i < 5) {
        cout << "Iteration " << i << "\n";
        i++;
    }
    return 0;
}
```

**Interview Questions with Answers:**
- Q: How does a while loop differ from a for loop in terms of structure and use cases?  
  A: A while loop requires only a condition and is used when the number of iterations isn’t fixed, whereas a for loop combines initialization, condition, and update in one line.
- Q: What potential issues might arise if the loop variable is not correctly updated?  
  A: Failing to update the loop variable can lead to infinite loops or unintended behavior.

---

### 3. Do-While Loop

A do-while loop guarantees execution of the loop body at least once since the condition is checked after the loop executes.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;
    do {
        cout << "Iteration " << i << "\n";
        i++;
    } while (i < 5);
    return 0;
}
```

**Interview Questions with Answers:**
- Q: In what scenarios would a do-while loop be more appropriate than a while loop?  
  A: A do-while loop is ideal when you need the loop body to execute at least once regardless of the condition.
- Q: What happens if the condition is false in a do-while loop?  
  A: The loop body executes once, and then the condition is evaluated; if false, the loop exits immediately after the first iteration.

---

### 3.4. Break & Continue

- The **break** statement exits the loop immediately when encountered.
- The **continue** statement skips the rest of the current iteration and moves to the next loop cycle.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 10; i++) {
        if (i == 5) {
            break;  // Exit the loop when i equals 5
        }
        if (i % 2 == 0) {
            continue;  // Skip even numbers
        }
        cout << "Odd number: " << i << "\n";
    }
    return 0;
}
```

**Interview Questions with Answers:**
- Q: How do break and continue alter the normal flow of loop execution?  
  A: The break statement terminates the loop entirely, while the continue statement skips to the next iteration, bypassing any code that follows in the current cycle.
- Q: Can break and continue be used in both for and while loops? Explain with an example.  
  A: Yes, both can be used in for, while, and do-while loops. For example, in a for loop, break can exit the loop early, and continue can skip the rest of the code for a specific iteration.

---

### 3.5. Goto Statement

The goto statement provides an unconditional jump to a labeled statement. Although it can simplify some code logic, its use is typically discouraged due to reduced code readability.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;
start:
    if (i >= 5) {
        goto end;
    }
    cout << "Iteration " << i << "\n";
    i++;
    goto start;
end:
    cout << "Exited loop using goto.\n";
    return 0;
}
```

**Interview Questions with Answers:**
- Q: What are the potential downsides of using the goto statement in structured programming?  
  A: Goto can make code hard to follow and debug, as it disrupts the natural flow of the program which leads to poor maintainability.
- Q: How could similar behavior be achieved without the use of goto?  
  A: Similar behavior can be obtained using structured loops (for, while) and control statements like break or continue, which are clearer and safer alternatives.

---
## 4. Functions  
### 4.1 Function Declaration & Definition

Functions in C++ are blocks of code designed to perform a specific task. They help in modularizing the code and reusing functionality. A function declaration (or prototype) provides the compiler with the function's name, return type, and parameters without its body, while the function definition includes the actual implementation.

#### Explanation

- A **function declaration** informs the compiler about the function signature. It allows functions to be defined later or in a separate file.
- A **function definition** contains the actual body of the code that executes when the function is called.
- Separating the declaration from the definition can improve code readability and maintainability, especially in larger projects.

#### Code Example

```cpp
#include <iostream>
using namespace std;

// Function declaration (prototype)
int add(int a, int b);

int main() {
    int sum = add(5, 3);  // Function call
    cout << "Sum: " << sum << "\n";
    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;
}
```

#### Interview Questions and Answers

1. Q: What is the primary difference between a function declaration and a function definition?  
   A: The declaration specifies the function signature without an implementation, while the definition includes the body of the function.

2. Q: Why are function declarations (prototypes) useful in C++?  
   A: They allow the compiler to understand the interface of functions before their actual definitions, enabling better code organization and separate compilation.

3. Q: What could happen if you call a function without providing its declaration?  
   A: The compiler may generate an error due to its inability to verify the function's signature before its definition.

4. Q: Can a function be declared multiple times?  
   A: Yes, you can declare the same function multiple times as long as the declarations are identical, but the definition should appear only once.

### 4.2 Call by Value

In call by value, a copy of the variable is passed to the function. Changes made inside the function do not affect the original variable.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int add(int a, int b) {  // 'a' and 'b' are copies
    a = a + 10; // modification only affects local copy
    return a + b;
}

int main() {
    int x = 5, y = 3;
    cout << "Result: " << add(x, y) << "\n"; // x remains 5
    cout << "x after function call: " << x << "\n";
    return 0;
}
```

**Interview Question:**
Q: What happens to the original variable when it is passed by value to a function?  
A: The function works with a copy, so any modifications do not affect the original variable.

---

### 4.3 Call by Reference

Call by reference passes the actual variable’s address to the function. Hence, any change to the parameter affects the original variable.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

void increment(int &num) {
    num++; // increment affects the original variable
}

int main() {
    int x = 5;
    increment(x);
    cout << "x after increment: " << x << "\n"; // x is now 6
    return 0;
}
```

**Interview Question:**
Q: How does call by reference differ from call by value?  
A: Call by reference passes the variable itself (its address), so changes affect the original variable. In call by value, only a copy is manipulated.

---

### 4.4 Inline Functions

An inline function suggests to the compiler to insert the function's code at the point of call to reduce the function call overhead. This is useful for small, frequently called functions.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

inline int square(int x) {
    return x * x;
}

int main() {
    int num = 4;
    cout << "Square of " << num << " is " << square(num) << "\n";
    return 0;
}
```

**Interview Question:**
Q: When would you use an inline function in C++?  
A: Inline functions are beneficial for small functions that are called frequently to reduce function call overhead, though the compiler makes the final decision.

---

### 4.5 Default Arguments

Default arguments allow you to specify default values for function parameters. If the caller omits those arguments, the default values are used.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

void greet(string name = "Guest") {
    cout << "Hello, " << name << "!\n";
}

int main() {
    greet("Alice");  // uses provided argument
    greet();         // uses default argument "Guest"
    return 0;
}
```

**Interview Question:**
Q: What is the advantage of using default arguments?  
A: They simplify function calls by allowing parameters to have default values, reducing the need for overloaded functions for different numbers of arguments.

---

### 4.6 Function Overloading

Function overloading enables multiple functions to share the same name but with different parameter types or numbers. The compiler distinguishes between them based on their signature.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

void display(int num) {
    cout << "Integer: " << num << "\n";
}

void display(double num) {
    cout << "Double: " << num << "\n";
}

void display(string text) {
    cout << "String: " << text << "\n";
}

int main() {
    display(10);
    display(3.14);
    display("Hello");
    return 0;
}
```

**Interview Question:**
Q: How does the compiler decide which overloaded function to call?  
A: The compiler selects the function that best matches the argument types based on function signature.

---

### 4.7 Recursion

Recursion occurs when a function calls itself to solve a problem by breaking it down into smaller subproblems. It requires a base case to avoid infinite recursion.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int factorial(int n) {
    if (n <= 1)
        return 1;  // Base case
    return n * factorial(n - 1);  // Recursive call
}

int main() {
    int num = 5;
    cout << "Factorial of " << num << " is " << factorial(num) << "\n";
    return 0;
}
```

**Interview Question:**
Q: What is crucial to include in a recursive function and why?  
A: A base case is crucial, as it provides a condition to end the recursion and prevents infinite recursive calls.

## 5. STL (Standard Template Library)

The STL is a powerful set of C++ template classes providing commonly used data structures and algorithms. It includes containers, iterators, algorithms, and functors. Below is an overview of some major components.

---

### 5.1 Vector

**Explanation:**  
A vector is a dynamic array that can change size during runtime. It provides random access to elements and methods for insertion, deletion, and traversal. Vectors handle memory allocation automatically.

**Predefined Methods:**

| Method | Description |
|--------|-------------|
| `push_back(value)` | Add an element at the end |
| `pop_back()` | Remove the last element |
| `size()` | Return the number of elements |
| `capacity()` | Return the current capacity of the vector |
| `empty()` | Returns true if vector has no elements |
| `at(index)` | Access an element with bounds checking |
| `front()` | Access the first element |
| `back()` | Access the last element |
| `begin()` | Returns iterator to first element |
| `end()` | Returns iterator to past-the-last element |
| `rbegin()` | Returns reverse iterator to last element |
| `rend()` | Returns reverse iterator to before-first element |
| `insert(iterator, value)` | Insert value at given position |
| `erase(iterator)` | Remove element at given position |
| `clear()` | Remove all elements |
| `resize(n)` | Resize vector to n elements |
| `shrink_to_fit()` | Reduce capacity to fit size |
| `assign(n, value)` | Assign n copies of value to vector |
| `swap(vector2)` | Swap contents with another vector |

---

**Code Example 1:**
```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> v = {1, 2, 3};

    // Add elements
    v.push_back(4);      // {1,2,3,4}

    // Access elements
    cout << v.at(2) << "\n";  // 3
    cout << v.front() << "\n"; // 1
    cout << v.back() << "\n";  // 4

    // Iterators
    for(auto it = v.begin(); it != v.end(); ++it)
        cout << *it << " ";
    cout << "\n";

    // Reverse iteration
    for(auto rit = v.rbegin(); rit != v.rend(); ++rit)
        cout << *rit << " ";
    cout << "\n";

    // Modify elements
    v.insert(v.begin()+1, 10);  // {1,10,2,3,4}
    v.erase(v.begin()+2);       // {1,10,3,4}

    // Size and capacity
    cout << "Size: " << v.size() << ", Capacity: " << v.capacity() << "\n";

    // Clear and check empty
    v.clear();
    cout << "Empty? " << v.empty() << "\n";
}
```

**Code Example 2:**
```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> numbers;
    numbers.push_back(10);
    numbers.push_back(20);
    numbers.push_back(30);

    cout << "Elements: ";
    for (int num : numbers) {
        cout << num << " ";
    }
    cout << "\nSize: " << numbers.size() << "\n";
    return 0;
}
```

**Interview Question:**  
Q: How does a vector manage its memory when new elements are added?  
A: Vectors automatically reallocate memory when their capacity is exceeded, often doubling the capacity to accommodate additional elements.

---

### 5.2 Map

**Explanation:**  
A map is an associative container that stores key-value pairs with unique keys. It keeps the elements ordered by their key using a balanced tree structure.

**Predefined Methods:**

| Method | Description |
|--------|-------------|
| `insert({key, value})` | Add a key-value pair |
| `find(key)` | Search for an element by key; returns iterator |
| `erase(key)` | Remove element by key |
| `erase(iterator)` | Remove element by iterator |
| `size()` | Return number of key-value pairs |
| `empty()` | Check if map is empty |
| `operator[](key)` | Access or create value for key |
| `count(key)` | Return 1 if key exists, else 0 |
| `clear()` | Remove all elements |
| `begin()` / `end()` | Iterator to first / past-last element |
| `rbegin()` / `rend()` | Reverse iterators |
| `key_comp()` | Return function object for key comparison |
| `value_comp()` | Return comparison object for value pairs |

---

**Code Example 1:**
```cpp
#include <iostream>
#include <map>
using namespace std;

int main() {
    map<int, string> mp;

    // Insert elements
    mp.insert({1, "One"});
    mp[2] = "Two";
    mp[3] = "Three";

    // Access elements
    cout << mp[2] << "\n";   // Two

    // Find element
    auto it = mp.find(3);
    if(it != mp.end())
        cout << it->first << " -> " << it->second << "\n";

    // Erase element
    mp.erase(1);              // removes key 1

    // Size and empty
    cout << "Size: " << mp.size() << "\n";
    cout << "Empty? " << mp.empty() << "\n";

    // Iterate through map
    for(auto p : mp)
        cout << p.first << " -> " << p.second << "\n";

    // Reverse iteration
    for(auto rit = mp.rbegin(); rit != mp.rend(); ++rit)
        cout << rit->first << " -> " << rit->second << "\n";
}
```
**Code Example 2:**
```cpp
#include <iostream>
#include <map>
using namespace std;

int main() {
    map<string, int> age;
    age["Alice"] = 30;
    age["Bob"] = 25;

    // Iterating over a map
    for (auto pair : age) {
        cout << pair.first << " is " << pair.second << " years old.\n";
    }
    return 0;
}
```

**Interview Question:**  
Q: What is the time complexity of search, insert, and delete operations in a map?  
A: These operations work in O(log n) time complexity because maps are typically implemented as red-black trees.

---

### 5.3 Set

**Explanation:**  
A set is an ordered collection of unique elements. It automatically sorts the elements and does not allow duplicates.
---

**Predefined Methods:**

| Method | Description |
|--------|-------------|
| `insert(value)` | Add an element |
| `erase(value)` | Remove an element by value |
| `erase(iterator)` | Remove element by iterator |
| `find(value)` | Search for an element; returns iterator |
| `count(value)` | Return 1 if element exists, else 0 |
| `size()` | Return number of elements |
| `empty()` | Check if set is empty |
| `clear()` | Remove all elements |
| `begin()` / `end()` | Iterator to first / past-last element |
| `rbegin()` / `rend()` | Reverse iterators |
| `lower_bound(value)` | Iterator to first element >= value |
| `upper_bound(value)` | Iterator to first element > value |
| `key_comp()` | Return function object for key comparison |

---

**Code Example 1:**
```cpp
#include <iostream>
#include <set>
using namespace std;

int main() {
    set<int> s;

    // Insert elements
    s.insert(10);
    s.insert(5);
    s.insert(20);
    s.insert(10); // Duplicate ignored

    // Iterate
    for(auto x : s)
        cout << x << " ";  // Output: 5 10 20
    cout << "\n";

    // Find element
    if(s.find(10) != s.end())
        cout << "10 exists\n";

    // Erase element
    s.erase(5);

    // Size and empty
    cout << "Size: " << s.size() << "\n";
    cout << "Empty? " << s.empty() << "\n";

    // Lower and upper bound
    auto lb = s.lower_bound(10);
    auto ub = s.upper_bound(10);
    cout << "Lower bound: " << *lb << ", Upper bound: " << *ub << "\n";
}
```

**Code Example 2:**
```cpp
#include <iostream>
#include <set>
using namespace std;

int main() {
    set<int> numbers;
    numbers.insert(5);
    numbers.insert(2);
    numbers.insert(8);
    numbers.insert(5); // Duplicate element; not added again

    cout << "Set elements: ";
    for (int num : numbers) {
        cout << num << " ";
    }
    cout << "\n";
    return 0;
}
```

**Interview Question:**  
Q: How does a set ensure that all elements are unique?  
A: A set uses a balanced binary search tree or hash table (in unordered_set) to perform insertions and automatically discard duplicates.

---

### 5.4 Queue

**Explanation:**  
A queue is a FIFO (first-in, first-out) data structure. It manages elements in a sequential order where insertion is at the back and deletion is from the front.

---

**Predefined Methods:**

| Method | Description |
|--------|-------------|
| `push(value)` | Insert element at the back |
| `pop()` | Remove element from the front |
| `front()` | Access the front element |
| `back()` | Access the last element |
| `empty()` | Check if queue is empty |
| `size()` | Return the number of elements |
| `swap(queue2)` | Swap contents with another queue |
| `emplace(value)` | Construct and insert element at the back |

---

**Code Example 1:**
```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    queue<int> q;

    // Insert elements
    q.push(10);
    q.push(20);
    q.push(30);

    // Access front and back
    cout << "Front: " << q.front() << "\n"; // 10
    cout << "Back: " << q.back() << "\n";   // 30

    // Remove front element
    q.pop();  // removes 10

    // Iterate (using copy)
    queue<int> temp = q;
    while(!temp.empty()) {
        cout << temp.front() << " ";
        temp.pop();
    }
    cout << "\n"; // Output: 20 30

    // Size and empty check
    cout << "Size: " << q.size() << "\n";   // 2
    cout << "Empty? " << q.empty() << "\n"; // 0 (false)
}
```

**Code Example 2:**
```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    queue<string> q;
    q.push("First");
    q.push("Second");
    q.push("Third");

    cout << "Front element: " << q.front() << "\n";
    q.pop();
    cout << "New front after pop: " << q.front() << "\n";
    return 0;
}
```

**Interview Question:**  
Q: What is the ideal use case for a queue?  
A: A queue is ideal when you need to process elements in the order they arrive, such as task scheduling or breadth-first search.

---

### 5.5 Stack

**Explanation:**  
A stack is a LIFO (last-in, first-out) data structure. Elements are added and removed from the top only.

---
**Predefined Methods:**

| Method | Description |
|--------|-------------|
| `push(value)` | Add an element to the top |
| `pop()` | Remove the top element |
| `top()` | Access the top element |
| `empty()` | Check if the stack is empty |
| `size()` | Return the number of elements |
| `swap(stack2)` | Swap contents with another stack |
| `emplace(value)` | Construct and push element at the top |

---

**Code Example 1:**
```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> st;

    // Push elements
    st.push(10);
    st.push(20);
    st.push(30);

    // Access top element
    cout << "Top: " << st.top() << "\n"; // 30

    // Remove top element
    st.pop(); // removes 30

    // Iterate (using copy)
    stack<int> temp = st;
    while(!temp.empty()) {
        cout << temp.top() << " ";
        temp.pop();
    }
    cout << "\n"; // Output: 20 10

    // Size and empty check
    cout << "Size: " << st.size() << "\n";   // 2
    cout << "Empty? " << st.empty() << "\n"; // 0 (false)
}
```

**Code Example 2:**
```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> s;
    s.push(5);
    s.push(10);
    s.push(15);

    cout << "Top element: " << s.top() << "\n";
    s.pop();
    cout << "New top after pop: " << s.top() << "\n";
    return 0;
}
```

**Interview Question:**  
Q: How is a stack used in function calls in C++?  
A: The call stack keeps track of active function calls, storing information such as local variables and return addresses.

---

### 5.6 Priority Queue (Heap)

**Explanation:**  
A priority queue is a **container adapter** that provides **fast access to the highest (or lowest) priority element**.  
- By default, it is a **max-heap** (largest element on top).  
- Can be customized as a **min-heap** using comparators.  
- Useful for **Dijkstra’s algorithm, task scheduling, and event simulation**.  

---

**Predefined Methods:**

| Method | Description |
|--------|-------------|
| `push(value)` | Insert an element |
| `pop()` | Remove the element with the highest priority |
| `top()` | Access the element with the highest priority |
| `empty()` | Check if the priority queue is empty |
| `size()` | Return the number of elements |
| `swap(pq2)` | Swap contents with another priority queue |
| `emplace(value)` | Construct and insert element efficiently |

---

**Example Code (Max-Heap):**
```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    priority_queue<int> pq;

    // Insert elements
    pq.push(10);
    pq.push(30);
    pq.push(20);

    // Access top element
    cout << "Top: " << pq.top() << "\n"; // 30

    // Remove top element
    pq.pop(); // removes 30

    // Iterate (by copying)
    priority_queue<int> temp = pq;
    while(!temp.empty()) {
        cout << temp.top() << " ";
        temp.pop();
    }
    cout << "\n"; // Output: 20 10

    // Size and empty check
    cout << "Size: " << pq.size() << "\n";   // 2
    cout << "Empty? " << pq.empty() << "\n"; // 0 (false)
}
```
**Example Code (Min-Heap):**
```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
priority_queue<int, vector<int>, greater<int>> minPQ;
minPQ.push(10);
minPQ.push(30);
minPQ.push(20);
cout << minPQ.top(); // 10
}
```

**Code Example:**
```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    // By default, priority_queue in C++ is a max-heap
    priority_queue<int> pq;
    pq.push(20);
    pq.push(15);
    pq.push(30);

    cout << "Top element (max): " << pq.top() << "\n";
    pq.pop();
    cout << "New top after pop: " << pq.top() << "\n";
    return 0;
}
```

**Interview Question:**  
Q: How can you turn a priority_queue into a min-heap?  
A: By using a custom comparator or by applying the greater<T> comparator, for example: priority_queue<int, vector<int>, greater<int>> minHeap;

---

### 5.7 Algorithms

**Explanation:**  
The STL provides a **rich set of generic algorithms** that operate on containers using iterators.  
- These include **sorting, searching, transforming, and more**.  
- Algorithms help reduce the need to write repetitive code.  
- Works with **vectors, arrays, sets, maps, and other containers**.  

---

**Common Functions:**

| Function | Description |
|----------|-------------|
| `sort(begin, end)` | Sort elements in ascending order |
| `sort(begin, end, cmp)` | Sort using custom comparator |
| `find(begin, end, value)` | Find an element in a range; returns iterator |
| `reverse(begin, end)` | Reverse elements in a range |
| `accumulate(begin, end, init)` | Sum elements starting from `init` |
| `count(begin, end, value)` | Count occurrences of a value |
| `binary_search(begin, end, value)` | Search in a **sorted** range; returns bool |
| `max_element(begin, end)` | Returns iterator to largest element |
| `min_element(begin, end)` | Returns iterator to smallest element |
| `next_permutation(begin, end)` | Transform to next lexicographical permutation |
| `prev_permutation(begin, end)` | Transform to previous permutation |
| `lower_bound(begin, end, value)` | Iterator to first element ≥ value |
| `upper_bound(begin, end, value)` | Iterator to first element > value |
| `count_if(begin, end, condition)` | Count elements satisfying condition |
| `for_each(begin, end, func)` | Apply function to each element |
| `copy(begin, end, dest)` | Copy elements to destination |
| `fill(begin, end, value)` | Fill range with value |
| `transform(begin1, end1, begin2, func)` | Apply function and store results in begin2 |

---

**Code Example 1:**
```cpp
#include <iostream>
#include <vector>
#include <algorithm>
#include <numeric>
using namespace std;

int main() {
    vector<int> v = {3, 1, 4, 1, 5, 9};

    // Sort
    sort(v.begin(), v.end());
    for(int x : v) cout << x << " "; // 1 1 3 4 5 9
    cout << "\n";

    // Reverse
    reverse(v.begin(), v.end());
    for(int x : v) cout << x << " "; // 9 5 4 3 1 1
    cout << "\n";

    // Find
    auto it = find(v.begin(), v.end(), 4);
    if(it != v.end()) cout << "Found: " << *it << "\n";

    // Count occurrences
    cout << "Count of 1: " << count(v.begin(), v.end(), 1) << "\n";

    // Accumulate (sum)
    int sum = accumulate(v.begin(), v.end(), 0);
    cout << "Sum: " << sum << "\n";

    // Binary search (requires sorted vector)
    sort(v.begin(), v.end());
    bool exists = binary_search(v.begin(), v.end(), 5);
    cout << "5 exists? " << exists << "\n";

    // Next permutation
    next_permutation(v.begin(), v.end());
    for(int x : v) cout << x << " "; 
    cout << "\n";
}
```

**Code Example 2:**
```cpp
#include <iostream>
#include <vector>
#include <algorithm>
#include <numeric>
using namespace std;

int main() {
    vector<int> nums = {5, 2, 9, 1, 5, 6};

    // Sorting the vector
    sort(nums.begin(), nums.end());
    cout << "Sorted: ";
    for (int n : nums) {
        cout << n << " ";
    }
    cout << "\n";

    // Finding an element
    auto it = find(nums.begin(), nums.end(), 5);
    if (it != nums.end())
        cout << "Element 5 found at index: " << distance(nums.begin(), it) << "\n";

    // Summing all elements
    int sum = accumulate(nums.begin(), nums.end(), 0);
    cout << "Sum of elements: " << sum << "\n";

    return 0;
}
```

**Interview Question:**  
Q: How do STL algorithms work with containers of different types?  
A: STL algorithms work generically using iterators, allowing them to perform operations on any container type as long as the container supports the required iterator operations.

## 6. Pointers & References

This section covers pointers in detail. Learn how to declare, use, and manipulate pointers along with their advanced forms.

---

### 6.1 Pointers Basics

Pointers store memory addresses and are declared using the asterisk (*) syntax. They allow direct memory access and manipulation.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 42;
    int *p = &x;  // p stores the address of x

    cout << "Value of x: " << x << "\n";
    cout << "Address of x: " << &x << "\n";
    cout << "Pointer p holds: " << p << "\n";
    cout << "Dereferenced pointer: " << *p << "\n";

    return 0;
}
```

**Interview Question:**
Q: What is the purpose of a pointer in C++?  
A: Pointers store memory addresses, allowing for dynamic memory management and efficient data manipulation.

---

### 6.2 Pointer Arithmetic

Pointer arithmetic allows you to navigate through contiguous memory (like arrays). Incrementing a pointer moves it to the next element based on its type size.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int *ptr = arr; // Pointer to the first element

    // Access array elements using pointer arithmetic
    for (int i = 0; i < 5; i++) {
        cout << "Element " << i << ": " << *(ptr + i) << "\n";
    }

    // Demonstrate pointer difference
    cout << "Distance between arr and &arr[3]: " << (&arr[3] - arr) << "\n";
    return 0;
}
```

**Interview Question:**
Q: How does pointer arithmetic work when incrementing a pointer?  
A: Incrementing a pointer moves it to the next memory location, offset by the size of the type it points to.

---

### 6.3 Pointer to Pointer

A pointer to pointer (double pointer) stores the address of another pointer. It is useful in dynamic memory allocation and multi-level indirection.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int value = 100;
    int *p = &value;     // pointer to int
    int **pp = &p;       // pointer to pointer

    cout << "Value: " << value << "\n";
    cout << "Through p: " << *p << "\n";
    cout << "Through pp: " << **pp << "\n";

    return 0;
}
```

**Interview Question:**
Q: When would you use a pointer to a pointer in C++?  
A: Pointer to pointer is useful when handling arrays of pointers or when dynamically allocating multi-dimensional arrays.

---

### 6.4 Null Pointer & Dangling Pointer

- **Null Pointer:** A pointer that does not point to any valid memory. It is good practice to initialize pointers to nullptr.
- **Dangling Pointer:** Occurs when a pointer points to memory that has been deallocated.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

int main() {
    // Null pointer example
    int *nullPtr = nullptr;
    if (nullPtr == nullptr) {
        cout << "nullPtr is nullptr\n";
    }

    // Dangling pointer example
    int *danglingPtr;
    {
        int temp = 50;
        danglingPtr = &temp; // temp goes out of scope after block
    }
    // Accessing danglingPtr now is unsafe and leads to undefined behavior
    // To prevent this, ensure pointers reference valid memory only.

    return 0;
}
```

**Interview Question:**
Q: How do you avoid creating a dangling pointer?  
A: Avoid dangling pointers by ensuring that pointers reference valid memory; for dynamically allocated memory, free it correctly and set the pointer to nullptr.



## 7. 🏛 OOP in C++

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects," which can contain data and methods. C++ supports OOP principles such as encapsulation, inheritance, polymorphism, and abstraction.

---

### 7.1 Class & Object

**Explanation:**  
- A **class** is a blueprint for creating objects. It defines properties (data members) and behaviors (member functions).  
- An **object** is an instance of a class.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;
    int speed;

    void display() {
        cout << "Brand: " << brand << ", Speed: " << speed << " km/h\n";
    }
};

int main() {
    Car car1;  // Object creation
    car1.brand = "Toyota";
    car1.speed = 120;
    car1.display();

    return 0;
}
```

**Interview Question:**  
Q: What is the difference between a class and an object?  
A: A class is a blueprint or template, while an object is an instance of a class.

---

### 7.2 Constructors & Destructors

**Explanation:**  
- A **constructor** is a special function automatically called when an object is created. It initializes the object.  
- A **destructor** is a special function automatically called when an object is destroyed. It cleans up resources.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;
    int speed;

    // Constructor
    Car(string b, int s) {
        brand = b;
        speed = s;
        cout << "Car created: " << brand << "\n";
    }

    // Destructor
    ~Car() {
        cout << "Car destroyed: " << brand << "\n";
    }

    void display() {
        cout << "Brand: " << brand << ", Speed: " << speed << " km/h\n";
    }
};

int main() {
    Car car1("Toyota", 120);
    car1.display();

    return 0;
}
```

**Interview Question:**  
Q: Can a constructor be overloaded in C++?  
A: Yes, constructors can be overloaded by defining multiple constructors with different parameter lists.

---

### 7.3 Inheritance

Inheritance allows a class (child) to acquire properties and behaviors of another class (parent).

#### 7.3.1 Single Inheritance
**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Vehicle {
public:
    void start() {
        cout << "Vehicle started\n";
    }
};

class Car : public Vehicle {
public:
    void drive() {
        cout << "Car is driving\n";
    }
};

int main() {
    Car car;
    car.start();
    car.drive();
    return 0;
}
```

**Interview Question:**  
Q: What is single inheritance?  
A: Single inheritance is when a class inherits from one parent class.

---

#### 7.3.2 Multiple Inheritance
**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Engine {
public:
    void engineType() {
        cout << "Engine type: V8\n";
    }
};

class Wheels {
public:
    void wheelCount() {
        cout << "Wheels: 4\n";
    }
};

class Car : public Engine, public Wheels {
public:
    void display() {
        cout << "Car details:\n";
    }
};

int main() {
    Car car;
    car.display();
    car.engineType();
    car.wheelCount();
    return 0;
}
```

**Interview Question:**  
Q: What is a potential issue with multiple inheritance?  
A: It can lead to ambiguity if two parent classes have methods with the same name.

---

#### 7.3.3 Multilevel Inheritance
**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Vehicle {
public:
    void start() {
        cout << "Vehicle started\n";
    }
};

class Car : public Vehicle {
public:
    void drive() {
        cout << "Car is driving\n";
    }
};

class SportsCar : public Car {
public:
    void turbo() {
        cout << "Turbo mode activated\n";
    }
};

int main() {
    SportsCar sc;
    sc.start();
    sc.drive();
    sc.turbo();
    return 0;
}
```

**Interview Question:**  
Q: What is multilevel inheritance?  
A: It is when a class inherits from a class that is already a child of another class.

---

#### 7.3.4 Hierarchical Inheritance
**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Vehicle {
public:
    void start() {
        cout << "Vehicle started\n";
    }
};

class Car : public Vehicle {
public:
    void drive() {
        cout << "Car is driving\n";
    }
};

class Bike : public Vehicle {
public:
    void ride() {
        cout << "Bike is riding\n";
    }
};

int main() {
    Car car;
    Bike bike;

    car.start();
    car.drive();

    bike.start();
    bike.ride();

    return 0;
}
```

**Interview Question:**  
Q: What is hierarchical inheritance?  
A: It is when multiple classes inherit from a single parent class.

---

### 7.4 Polymorphism

Polymorphism allows methods to behave differently based on the object that calls them.

#### 7.4.1 Compile-time Polymorphism (Function Overloading / Operator Overloading)
**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Calculator {
public:
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
};

int main() {
    Calculator calc;
    cout << "Int addition: " << calc.add(5, 3) << "\n";
    cout << "Double addition: " << calc.add(2.5, 3.5) << "\n";
    return 0;
}
```

**Interview Question:**  
Q: What is function overloading?  
A: It is defining multiple functions with the same name but different parameter lists.

---

#### 7.4.2 Run-time Polymorphism (Virtual Functions)
**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Vehicle {
public:
    virtual void start() {
        cout << "Vehicle started\n";
    }
};

class Car : public Vehicle {
public:
    void start() override {
        cout << "Car started\n";
    }
};

int main() {
    Vehicle *v = new Car();
    v->start();  // Calls Car's start method
    delete v;
    return 0;
}
```

**Interview Question:**  
Q: What is the purpose of the `virtual` keyword?  
A: It enables runtime polymorphism by allowing derived class methods to override base class methods.

---

### 7.5 Encapsulation & Abstraction

**Explanation:**  
- **Encapsulation** bundles data and methods into a single unit (class) and restricts access using access specifiers (`private`, `protected`, `public`).  
- **Abstraction** hides implementation details and exposes only essential features.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

class BankAccount {
private:
    double balance;

public:
    BankAccount(double initialBalance) {
        balance = initialBalance;
    }

    void deposit(double amount) {
        balance += amount;
    }

    double getBalance() {
        return balance;
    }
};

int main() {
    BankAccount account(1000);
    account.deposit(500);
    cout << "Balance: " << account.getBalance() << "\n";
    return 0;
}
```

**Interview Question:**  
Q: How does encapsulation improve code security?  
A: By restricting direct access to data members, encapsulation prevents unauthorized modifications.

---

### 7.6 Friend Functions & Classes

**Explanation:**  
- A **friend function** can access private and protected members of a class.  
- A **friend class** can access private and protected members of another class.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Box {
private:
    double width;

public:
    Box(double w) : width(w) {}

    friend void displayWidth(Box b);
};

void displayWidth(Box b) {
    cout << "Width: " << b.width << "\n";
}

int main() {
    Box b(10.5);
    displayWidth(b);
    return 0;
}
```

**Interview Question:**  
Q: Why use friend functions in C++?  
A: Friend functions allow external functions to access private members of a class, useful for operator overloading or utility functions.

---

### 7.7 Static Members

**Explanation:**  
- **Static data members** are shared across all objects of a class.  
- **Static member functions** can access only static data members.

**Example Code:**
```cpp
#include <iostream>
using namespace std;

class Counter {
private:
    static int count;

public:
    Counter() {
        count++;
    }

    static int getCount() {
        return count;
    }
};

int Counter::count = 0;

int main() {
    Counter c1, c2, c3;
    cout << "Count: " << Counter::getCount() << "\n";
    return 0;
}
```

**Interview Question:**  
Q: What is the purpose of static members in C++?  
A: Static members are shared across all objects of a class, making them useful for maintaining global state or counters.


## 👤 Author

**Name:** Nitish Kumar Upadhyay

**Email:** nitishapp9455@gmail.com  

*This C++ Cheat Sheet is curated and maintained by Nitish Kumar Upadhyay.*
