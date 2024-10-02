# Project: Python Basics - Number Operations

## Table of Contents
1. [Display Table](#1-display-table)
2. [Swap Two Numbers](#2-swap-two-numbers)
   - [Basic Swap](#basic-swap)
   - [Logical Swap](#logical-swap-(-using-temporary-variable-))
   - [String Formatting](#string-formatting)
3. [Swapping Numbers Using Two Variables](#3-swapping-numbers-using-two-variables)

---
### 1. Display Table

**Code:**
```python
a = int(input('Enter a Number: '))
i = 1
```
- **Explanation**: The user is prompted to enter a number `a`. The variable `i` is initialized to `1`, which will be used as a counter for the multiplication table.

#### With While Loop
```python
while i <= 10:
    print(a, ' x ', i, ' = ', i * a)
    i += 1
```
- **Explanation**:
  - A `while` loop runs while `i` is less than or equal to 10.
  - Each iteration prints the product of `a` and `i` (i.e., `a × i`).
  - After each iteration, `i` is incremented by 1.

#### With For Loop
```python
for i in range(1, 11):
    print(a, 'x', i, '=', i * a)
```
- **Explanation**:
  - A `for` loop iterates through the values 1 to 10.
  - For each value of `i`, the multiplication of `a` and `i` is printed in a formatted manner.
  - This loop achieves the same result as the `while` loop but with more concise code.

---

### 2. Swap Two Numbers

#### Basic Swap
**Code:**
```python
a = int(input('Enter first Number: '))
b = int(input('Enter second Number: '))
print('Before Swapping First Number = ', a, ', Second Number = ', b)
print('After Swapping First Number = ', b, ', Second Number = ', a)
```
- **Explanation**:
  - The user inputs two numbers `a` and `b`.
  - Before swapping, the values of `a` and `b` are printed.
  - After swapping, the value of `a` is printed as `b`, and `b` is printed as `a`. This is a manual swap (no logic involved, just printed in reverse).

#### Logical Swap (Using Temporary Variable)
**Code:**
```python
a = int(input('Enter first Number: '))
b = int(input('Enter second Number: '))
temp = a
a = b
b = temp
print('After swapping: First Number = {}, Second Number = {}'.format(a, b))
```
- **Explanation**:
  - The user inputs two numbers.
  - A temporary variable `temp` is used to store the value of `a`.
  - The value of `b` is then assigned to `a`, and `temp` (which holds the original value of `a`) is assigned to `b`, thereby swapping the values.
  - The result is printed using the `format()` method.

#### String Formatting
**Code:**
```python
print("After swapping: First Number = {}, Second Number = {}".format(a, b))
```
- **Explanation**:
  - This line uses Python's `str.format()` method to print the swapped values of `a` and `b` in a formatted string.

---

### 3. Swapping Numbers Using Two Variables (Without Temporary Variable)

**Code:**
```python
a = int(input("Enter the first number: "))
b = int(input("Enter the second number: "))
```
- **Explanation**:
  - The user is asked to input two numbers `a` and `b`.

#### Before Swapping
```python
print("Before swapping:")
print("a =", a)
print("b =", b)
```
- **Explanation**:
  - The original values of `a` and `b` are printed before any swapping occurs.

#### Swapping Logic
```python
a = a + b
b = a - b
a = a - b
```
- **Explanation**:
  - The swapping is done using arithmetic operations:
    1. `a = a + b`: Adds `a` and `b`, and stores the sum in `a`.
    2. `b = a - b`: Subtracts the original value of `b` from the new value of `a` (which is `a + b`), giving the original value of `a` and storing it in `b`.
    3. `a = a - b`: Subtracts the new value of `b` (which is the original `a`) from `a`, leaving the original value of `b` in `a`.
  - This efficiently swaps `a` and `b` without needing a temporary variable.

#### After Swapping
```python
print("After swapping:")
print("a =", a)
print("b =", b)
```
- **Explanation**:
  - After performing the swap, the new values of `a` and `b` are printed, showing that their values have been exchanged.

---
