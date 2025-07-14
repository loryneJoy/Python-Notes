# 📅 Day 1: Python Essentials + Functions

## ✍️ Topics Covered
- Variables and data types
- Input/output
- Arithmetic and logical operations
- Control flow (if-else, loops)
- List comprehensions
- Functions: `def`, `return`, arguments, `lambda`

---

## ✅ Variables and Data Types
Variables store information in your program. Python supports types like:
- **Strings**: text data (e.g. "hello")
- **Integers**: whole numbers (e.g. 3)
- **Floats**: decimal numbers (e.g. 3.14)
- **Booleans**: `True` or `False` values

Python uses dynamic typing—this means you don’t need to declare a variable’s type in advance:

```python
name = "Alice"      # string
age = 25            # integer
height = 5.6        # float
is_student = True   # boolean
```

---


## ✅ Input and Output

You can use the input() function to get user input and print() to display output. Note that input() always returns a string, so convert it when needed:

name = input("What is your name? ")
print("Hello,", name)

Example with conversion:

```python
year = int(input("What year were you born? "))
age = 2025 - year
print("You are", age, "years old.")
```

## ✅ Arithmetic and Logical Operations

Python supports arithmetic like:

    + (add), - (subtract), * (multiply), / (divide), ** (power), % (modulus)

Comparison operators include:

    ==, !=, <, >, <=, >=

Logical operators:

    and, or, not

Example:
```python
a = 10
b = 3
print(a + b, a ** b, a % b)      # 13, 1000, 1
print(a > b and b < 5)           # True
```

---

## ✅ Control Flow

Control flow helps you make decisions and repeat tasks.
### If-Else Statement
```python
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

You can chain multiple conditions with elif.
### For Loop

Use for to iterate over a range or list:

```python
for i in range(5):
    print(i)
```

### While Loop

```python
count = 0
while count < 3:
    print("Counting:", count)
    count += 1
```
Make sure to update the condition to avoid infinite loops.

---

## ✅ List Comprehensions

List comprehensions are a shortcut for creating lists from loops:

```python
squares = [i**2 for i in range(1, 6)]
print(squares)  # [1, 4, 9, 16, 25]
```
You can also filter with a condition:

```python
evens = [i for i in range(10) if i % 2 == 0]
```
List comprehensions are powerful for data cleaning and transformation.

---

## ✅ Functions

Functions allow you to group code into reusable blocks.

```python
def greet(name):
    return f"Hello {name}!"

def add(x, y):
    return x + y

print(greet("Wycliffe"))
```

Use lambda for simple one-line functions:

```python
square = lambda x: x**2
print(square(5))  # 25
```
Functions help break your program into manageable, testable parts.


📋 Classwork: Day 1

- Ask the user for their birth year. Calculate and print their age.

- Write a function that checks if a number is even or odd.

- Create a list of all numbers divisible by 3 between 1 and 50 using list comprehension.

- Write a function that takes a name and prints Hello, <name>!.

- Use a while loop to print numbers from 1 to 5.
