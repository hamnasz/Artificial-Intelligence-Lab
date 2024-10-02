# Display Multiplication Table

This Python program takes an input number from the user and displays its multiplication table from 1 to 10.

## Code

```python
# Prompt the user to enter a number
a = int(input('Enter a Number: '))

# Initialize iterator
i = 1

# Loop to display multiplication table
while i <= 10:
    print(a, ' x ', i, ' = ', i * a)
    i += 1
