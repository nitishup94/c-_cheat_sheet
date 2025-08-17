# 📘 C++ Programming Cheat Sheet

Welcome to the **C++ Quick Reference** 🚀  
This repo contains **syntax, examples, and STL functions** you need for coding interviews, DSA, and competitive programming.  

---

## 📑 Table of Contents
1. [Basic Input/Output](#-basic-inputoutput)  
2. [Data Types](#-data-types)  
3. [Control Statements](#-control-statements)  
4. [Functions](#-functions)  
5. [STL (Standard Template Library)](#-stl-standard-template-library)  
   - [Vector](#-vector)  
   - [Map](#-map)  
   - [Set](#-set)  
   - [Queue](#-queue)  
   - [Stack](#-stack)  
   - [Priority Queue (Heap)](#-priority-queue-heap)  
   - [Algorithms](#-algorithms)  
6. [Pointers & References](#-pointers--references)  
7. [OOP in C++](#-oop-in-c)  

---

## 🖥 Basic Input/Output
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
## 🔢 Data Types  

**Primitive Data Types in C++**  
- `int` → 4 bytes (usually, platform-dependent)  
- `float` → 4 bytes (single precision)  
- `double` → 8 bytes (double precision)  
- `char` → 1 byte (single character)  
- `bool` → 1 byte (true/false)  
- `void` → no value  

**Derived Types**  
- `array`, `pointer`, `reference`, `function`  

**User-defined Types**  
- `struct`, `class`, `enum`, `typedef`, `using`  

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    int a = 10;
    float b = 5.6;
    double c = 9.87654321;
    char d = 'A';
    string s = "C++";
    bool flag = true;

    cout << "int: " << a << endl;
    cout << "float: " << b << endl;
    cout << "double: " << c << endl;
    cout << "char: " << d << endl;
    cout << "string: " << s << endl;
    cout << "bool: " << flag << endl;
}
```
