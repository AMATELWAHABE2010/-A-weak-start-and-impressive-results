💡 Core Python: Arithmetic Operations and Variables
Overview ✨

This lesson explores how Python performs mathematical calculations and the rules for managing variables effectively. It moves beyond basic types to handle complex formulas and operational logic.
🎯 Learning Objectives

    ✅ Master basic arithmetic operators and the exponentiation operator (**).

    ✅ Understand the importance of Operator Precedence (PEMDAS).

    ✅ Learn the rules and best practices for naming variables (Snake Case).

    ✅ Use the Modulo operator (%) for parity checks and cycles.

    ✅ Apply physics-based formulas (Kinetic Energy, Distance) in code.

A. Arithmetic Operators ➕➖

Python supports standard math operations and some specialized ones for programming logic:
Operator	Description	Example	Result
+	Addition	10 + 5	15
-	Subtraction	10 - 5	5
*	Multiplication	10 * 5	50
/	Division (Float)	10 / 3	3.333...
//	Floor Division	10 // 3	3
%	Modulo (Remainder)	10 % 3	1
**	Exponentiation (Power)	2 ** 3	8
B. Operator Precedence (PEMDAS) 🧠

When multiple operators appear in one expression, Python follows a specific order. Failing to use parentheses () often leads to logical errors in physics formulas.

    Parentheses ()

    Exponents **

    Multiplication & Division *, /, //, %

    Addition & Subtraction +, -

Physics Example (The Barycenter Error):
Python

# WRONG: Result = 25 (it divides m2*x2 by m1 only)
xG = m1*x1 + m2*x2 / m1 + m2 

# CORRECT: Result = 5 (proper grouping)
xG = (m1 * x1 + m2 * x2) / (m1 + m2) 

C. Variable Naming & Best Practices 🏷️

Naming variables correctly is crucial for code readability and avoiding SyntaxError.

    Rules:

        Must start with a letter or underscore _.

        Cannot contain spaces.

        Cannot be a Python keyword (like print or if).

    Naming Conventions:

        Snake Case (Recommended): initial_velocity, total_mass.

        Camel Case: initialVelocity, totalMass.

⚠️ Common Mistakes & Quick Tips

    The ^ Trap: In many languages ^ means power, but in Python it is a Bitwise XOR. Always use ** for exponents.

    Integer Division: Use // if you only want the whole part of the division, but be careful in physics where decimals (floats) are usually required.

    Tip: Use the modulo % 2 to check if a number is even (result is 0) or odd (result is 1).

🧪 Examples (Physics Applications)
Python

# Example 1:# ⚡ Kinetic Energy Calculator
This script calculates the energy of an object in motion using the classic physics formula:
$$E_c = \frac{1}{2}mv^2$$

### 💻 Python Implementation
```python
# Taking inputs from the user
mass = float(input("Mass (kg): "))
velocity = float(input("Velocity (m/s): "))

# Applying the formula: 0.5 * m * v^2
kinetic_energy = 0.5 * mass * (velocity ** 2)

# Displaying the result
print(f"Kinetic Energy: {kinetic_energy} Joules")

# ⭕ Exercise 2: Circular Path Area
In this exercise, we calculate the area of a circular path using the mathematical constant $\pi$ and the exponent operator.

### 📐 The Formula
$$Area = \pi \times r^2$$

### 💻 Python Code
```python
# Constants and Inputs
PI = 3.14159
radius = float(input("Enter the Radius (m): "))

# Calculation using the power operator (**)
area = PI * (radius ** 2)

# Output with 2 decimal places formatting
print(f"Path Area: {area:.2f} m^2")

✍️ Exercises (Practice)

    The Displacement Formula: Ask for v0​ (initial velocity), a (acceleration), and t (time). Calculate distance using: d=v0​t+21​at2. ✅

    Parity Checker: Ask the user for an integer and use the modulo operator to print True if it's even and False if it's odd. ✅

    Temperature Converter: Convert Fahrenheit to Celsius: C=(F−32)×95​. ✅

✅ Solutions (Short)

1.
Python

v0 = float(input("v0: "))
a = float(input("a: "))
t = float(input("t: "))
d = (v0 * t) + (0.5 * a * (t ** 2))
print(f"Distance: {d}")

2.
Python

num = int(input("Enter number: "))
print(f"Is even? {num % 2 == 0}")

3.
Python

f = float(input("Fahrenheit: "))
c = (f - 32) * (5/9)
print(f"Celsius: {c:.2f}")

End of Lesson 2 — Arithmetic Operations and Variables.
