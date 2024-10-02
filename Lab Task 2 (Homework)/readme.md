# Table of Contents
- [1. Display Multiplication Table](#display-multiplication-table)
  - [Purpose](#purpose)
  - [Code Breakdown](#code-breakdown)
  - [Example Output](#example-output)
  - [Conclusion](#conclusion)
- [2. Swap Two Numbers](#swap-two-numbers)
  - [Method 1: Simple Swapping (No Logic Swapping)](#method-1-simple-swapping-no-logic-swapping)
  - [Method 2: Logically Swapping Two Numbers](#method-2-logically-swapping-two-numbers)
  - [Conclusion](#conclusion-1)
- [3. Swapping Numbers Using Two Variables](#swapping-numbers-using-two-variables)
  - [Code](#code)
  - [Example](#example)
  - [Conclusion](#conclusion-2)

---

# Display Multiplication Table

This Python program allows the user to input a number, and it then displays the multiplication table of that number from 1 to 10.

---

## Purpose:

This Python program is designed to:
- Take user input for a number.
- Display the multiplication table for the input number from 1 to 10.

---

## Code Breakdown:

1. **Input Section**:
   ```python
   a = int(input('Enter a Number: '))
   ```
   - **Explanation**: 
     - The program prompts the user to enter an integer using the `input()` function.
     - The input is then converted from a string to an integer using `int()` and stored in the variable `a`.

2. **Initialization of the Iterator**:
   ```python
   i = 1
   ```
   - **Explanation**:
     - The variable `i` is initialized to 1, which will serve as the iterator for the loop, representing the numbers 1 to 10 in the multiplication table.

3. **While Loop**:
   ```python
   while i<=10:
       print (a, ' x ', i, ' = ', i*a)
       i+=1
   ```
   - **Explanation**:
     - This `while` loop runs as long as the value of `i` is less than or equal to 10.
     - Inside the loop, the program calculates the product of the user’s input (`a`) and the iterator (`i`), then prints the result in a formatted manner to show the multiplication table.
     - The `i+=1` increments `i` by 1 after each iteration, ensuring that the loop progresses from 1 to 10.

---

## Example Output:

For an input `a = 3`, the output will be:

```
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
3 x 6 = 18
3 x 7 = 21
3 x 8 = 24
3 x 9 = 27
3 x 10 = 30
```

---

## Conclusion:

This simple Python program demonstrates the use of:
- Loops
- User input
- Basic arithmetic operations

---

# Swap Two Numbers

This Python notebook demonstrates two methods to swap the values of two variables:
1. Simple swapping without logic.
2. Logical swapping using a temporary variable.

---

## Method 1: Simple Swapping (No Logic Swapping)

This is a basic method where the values of two variables are swapped by changing their assignments without any additional logic.

### Code:

```python
# Taking two numbers as input
a = int(input('Enter First Number: '))
b = int(input('Enter Second Number: '))

# Displaying numbers before swapping
print('Before Swapping First Number = ', a, ', Second Number = ', b)

# Swapping the values
temp = a
a = b
b = temp

# Displaying numbers after swapping
print('After Swapping First Number = ', a, ', Second Number = ', b)
```

### Explanation:
1. **Input**: The program asks the user to enter two numbers.
2. **Before Swap**: It prints the values of `a` and `b` before swapping.
3. **Swapping**: A third variable `temp` is used to hold the value of `a` while `a` is assigned the value of `b` and then `b` gets the value stored in `temp`.
4. **After Swap**: It prints the values of `a` and `b` after the swap.

### Example:

If the user inputs:
```
First Number = 2
Second Number = 5
```

The output will be:
```
Before Swapping First Number = 2, Second Number = 5
After Swapping First Number = 5, Second Number = 2
```

---

## Method 2: Logically Swapping Two Numbers

This method uses a temporary variable for the swapping process.

### Code:

```python
# Taking two numbers as input
a = int(input('Enter First Number: '))
b = int(input('Enter Second Number: '))

# Logical Swapping using a temporary variable
temp = a
a = b
b = temp

# Displaying swapped numbers
print("After swapping: First Number = {}, Second Number = {}".format(a, b))
```

### Explanation:
1. **Input**: The program asks the user to input two numbers.
2. **Swapping**: A temporary variable `temp` is used to facilitate swapping.
3. **Output**: The program displays the numbers after the swapping process is complete.

### Example:

If the user inputs:
```
First Number = 6
Second Number = 3
```

The output will be:
```
After swapping: First Number = 6, Second Number = 3
```

---

## Conclusion:

These two methods show how to swap two numbers:
- The first method directly changes the values without using a temporary variable (conceptually).
- The second method uses a temporary variable to hold one value during the swap.
Both approaches help learners understand basic concepts like variable assignment and swapping in Python.

---

# Swapping Numbers Using Two Variables

This Python notebook demonstrates how to swap two numbers without using a third variable. It uses basic arithmetic operations to swap the values of two variables.

---

## Code:

```python
# Taking two numbers as input
a = int(input("Enter the first number: "))
b = int(input("Enter the second number: "))

# Displaying numbers before swapping
print("Before swapping: a = {}, b = {}".format(a, b))

# Swapping the values using arithmetic operations
a = a + b
b = a - b
a = a - b

# Displaying numbers after swapping
print("After swapping: a = {}, b = {}".format(a, b))
```

### Explanation:
1. **Input**: The program prompts the user to input two numbers, `a` and `b`.
2. **Before Swap**: It prints the values of `a` and `b` before the swapping process.
3. **Swapping**: The program swaps the values using three arithmetic operations:
   - `a = a + b`: The sum of `a` and `b` is stored in `a`.
   - `b = a - b`: Now, `b` is set to the original value of `a` by subtracting the original `b` from the sum.
   - `a = a - b`: Finally, the original value of `b` is subtracted from the sum to get the original value of `b` stored in `a`.
4. **After Swap**: It prints the new values of `a` and `b` after the swapping process.

---

### Example:

If the user inputs:
```
First Number = 4
Second Number = 6
```

The output will be:
```
Before swapping: a = 4, b = 6
After swapping: a = 6, b = 4
```

---

## Conclusion:

This approach efficiently swaps two numbers without needing a third variable. It demonstrates how arithmetic operations can be used for value swapping and reinforces basic mathematical manipulation in programming.
