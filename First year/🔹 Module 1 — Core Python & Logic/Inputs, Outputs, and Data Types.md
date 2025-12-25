
# 💡 Core Python: Input, Output, and Basic Data Types

---

## Overview ✨
This lesson introduces how Python programs communicate with the user (Input / Output) and how data is categorized and stored using fundamental data types.

---

## 🎯 Learning Objectives
- ✅ Understand how to display output in Python using `print()`.  
- ✅ Learn how to capture user input with `input()` and know its default type.  
- ✅ Recognize and use three basic data types: `str`, `int`, and `float`.  
- ✅ Convert (cast) string input into numeric types for calculations.  
- ✅ Apply simple examples and small exercises to reinforce concepts.

---

## A. Output Function: `print()` 🖨️
The `print()` function is the primary way to show information to the user on the console. It accepts strings, numbers, or expressions.

```python
# Displays a direct message
print("Starting my Python journey.")

# Displays the value of a calculation
print(10 * 5)

# Multiple items and formatted output
name = "Alex"
total_cost = 23.5
print("Name:", name, "Total:", total_cost)
print(f"Hello {name}, total cost is {total_cost:.2f}")
```

Tips:
- Use commas to print multiple values: `print("Value:", x)`
- Use f-strings (Python 3.6+) for readable formatting: `print(f"Total: {total_cost}")`

---

## B. Input Function: `input()` ⌨️
`input()` pauses the program, shows an optional prompt, and waits for the user to type a value and press Enter. The returned value is always a string (`str`).

```python
user_response = input("What is your favorite color? ")
print("You chose:", user_response)
```

Important: The value returned by `input()` is always `str`. To use the input in numeric operations, convert it with `int()` or `float()`.

---

## C. Basic Data Types 🧱
Python classifies stored information into types that determine how the data is handled:

- String (`str`): Text data. Enclosed in single or double quotes.
  - Examples: `"Name"`, `'hello'`

- Integer (`int`): Whole numbers without decimals.
  - Examples: `10`, `-5`

- Float (`float`): Numbers with decimal points.
  - Examples: `3.14`, `0.5`

Type checking example:
```python
x = "hello"
print(type(x))  # <class 'str'>
```

---

## D. Type Casting (Explicit Conversion) 🔁
To perform math on values from `input()`, convert the string to `int` or `float`.

- `int()` converts to integer (if the input is whole).
- `float()` converts to floating-point number.

```python
number_of_items = int(input("How many items? "))
price = float(input("Enter the price: "))
total_cost = number_of_items * price
print("Total calculated cost:", total_cost)
```

Be careful: converting non-numeric strings raises a `ValueError`. Validate input or use `try` / `except`.

---

## ⚠️ Common Mistakes & Quick Tips
- Mistake: Thinking `input()` returns a number — it returns a string.  
  Example: `"2" + "3"` results in `"23"` (concatenation), not `5`.

- Tip: Validate before casting. `str.isdigit()` is limited (doesn't handle negatives or decimals). Use `try/except` for robust handling.

Example validation:
```python
value = input("Enter a number: ")
try:
    num = float(value)  # handles integers and decimals
except ValueError:
    print("Please enter a valid number.")
```

---

## 🧪 Examples (Interactive)
```python
# Example 1: Sum two integers entered by the user
a = int(input("Enter first integer: "))
b = int(input("Enter second integer: "))
print("Sum:", a + b)

# Example 2: Calculate area of rectangle using floats
width = float(input("Width (m): "))
height = float(input("Height (m): "))
area = width * height
print(f"Area: {area} square meters")
```

---

## ✍️ Exercises (Practice)
1. Ask the user for their name and age. Print:  
   "Hello, <name> — next year you will be <age+1> years old." ✅

2. Ask for the radius of a circle (decimal allowed). Calculate and print the area (use `3.14159`). ✅

3. Create a mini shopping snippet: ask for quantity (int) and unit price (float), then print total cost formatted to 2 decimal places. ✅

---

## ✅ Solutions (Short)
1.
```python
name = input("Name: ")
age = int(input("Age: "))
print(f"Hello, {name} — next year you will be {age + 1} years old.")
```

2.
```python
r = float(input("Radius: "))
area = 3.14159 * r * r
print(f"Area: {area}")
```

3.
```python
qty = int(input("Quantity: "))
price = float(input("Unit price: "))
total = qty * price
print(f"Total: {total:.2f}")
```



--- 

_End of Lesson 1 — Input, Output, and Basic Data Types._  


----------------------------------You will find the supporting exercises on Wiki's Repository page.---------------------------

