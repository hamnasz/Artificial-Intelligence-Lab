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
