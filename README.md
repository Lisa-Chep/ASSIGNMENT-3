# ASSIGNMENT-3
# Pointer Concepts in C – Assignment

## Student Information
- Name: __LISA CHEPKOECH KIPYEGO ENE 211-0016/2024____________________
- Course: ___EEE_________________
- Assignment Title: Pointer Concepts
- Programming Language: C

---

## Description
This repository contains short notes and examples explaining pointer concepts in the C programming language.  
The aim of this assignment is to understand how pointers work, when they are used, and their advantages and risks.

---

## Pointer Concepts – Short Notes

### 1. What is a Pointer?
A pointer is a variable that stores the memory address of another variable.  
Instead of storing a value directly, it stores the location where the value is kept in memory.

```c
int x = 10;
int *p = &x;
Here, p stores the address of x.

2. Pointer Declaration and Dereferencing

Pointer declaration specifies the type of data the pointer will point to.
Dereferencing (*) is used to access the value stored at the memory address.
int *p;
printf("%d", *p);   // Access value at the address stored in p
3. Address Operator (&)

The address-of operator (&) is used to obtain the memory address of a variable.
int x = 5;
int *p = &x;
When Are Pointers Preferred Over Normal Variables?

Pointers are preferred when direct memory access, efficiency, or shared data manipulation is required.

Examples
Example 1: Modifying Variables Inside Functions

Pointers allow functions to modify the original variable.
void update(int *p) {
    *p = 50;
}
Without pointers, changes would not reflect outside the function.

Example 2: Dynamic Memory Allocation

Pointers are required when allocating memory dynamically using malloc().
int *arr = (int *)malloc(5 * sizeof(int));
Dynamic memory allocation is not possible using normal variables.

Limitations and Risks of Using Pointers

Memory Errors – Dereferencing uninitialized or NULL pointers can cause crashes.

Memory Leaks – Forgetting to free dynamically allocated memory wastes system resources.

Dangling Pointers – Accessing memory after it has been freed leads to undefined behavior.

Complexity – Pointer-based code is harder to read and debug.

Call by Value vs Call by Reference
Call by Value

A copy of the variable is passed to the function.
Changes do not affect the original variable.void change(int x) {
    x = 20;
}
Practical Scenarios
When Call by Value Is Preferred

When the original data must remain unchanged

For simple data types (integers, floats)

When simplicity and safety are important

Example: Mathematical calculations

When Call by Reference Is Preferred

When a function must modify original data

When passing large data structures such as arrays

To improve performance by avoiding copying

Example: Sorting an array, updating user records
