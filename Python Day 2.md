# 📅 **Day 2: Data Structures + Classes**

## ✍️ Topics Covered
- Lists, Tuples, Sets, Dictionaries
- Indexing and Slicing
- File Input/Output (File I/O)
- Classes and Objects
- `__init__` method and instance attributes
- Methods inside classes
- Intro to Decorators

---

## ✅ Lists, Tuples, Sets, and Dictionaries

Python offers several built-in data structures. These are the foundation of data manipulation:

### Lists
Ordered and changeable (mutable).
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits[1])  # banana
```

### Tuples
Ordered but immutable (cannot be changed after creation).
```python
dimensions = (1920, 1080)
print(dimensions[0])  # 1920
```

### Sets
Unordered and only contain unique items.
```python
unique_numbers = {1, 2, 2, 3, 4}
print(unique_numbers)  # {1, 2, 3, 4}
```

### Dictionaries
Key-value pairs. Great for structured data.
```python
person = {"name": "Alice", "age": 30}
print(person["name"])  # Alice
```

---

## ✅ Indexing and Slicing

You can access parts of lists or strings using indices:
```python
numbers = [10, 20, 30, 40, 50]
print(numbers[1])      # 20
print(numbers[1:4])    # [20, 30, 40]
```
Slicing returns a new list without modifying the original.

---

## ✅ File Input/Output (File I/O)

Python allows you to read and write files. Always use the with statement to avoid forgetting to close the file.

### Writing to a file:
```python
with open("sample.txt", "w") as f:
    f.write("Hello World")
```

### Reading from a file:
```python
with open("sample.txt", "r") as f:
    content = f.read()
    print(content)
```
This is useful when working with datasets or saving results.

---

## ✅ Classes and Objects

A class is a blueprint for creating objects (instances). Think of it like a custom data type that bundles data (attributes) and behavior (methods).
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hi, I'm {self.name} and I'm {self.age} years old.")
```

### Creating an object:
```python
p1 = Person("Wycliffe", 28)
p1.greet()
```
The __init__() method runs automatically when an object is created. The self keyword refers to the current object.

---

## ✅ Methods and Attributes

    Attributes: Variables that hold data for the object

    Methods: Functions that belong to the class
```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        return f"{self.name} says Woof!"
```

---

## ✅ Intro to Decorators

A decorator is a function that takes another function and adds extra behavior to it.
```python
def logger(func):
    def wrapper():
        print("Function is being called...")
        func()
    return wrapper

@logger
def say_hello():
    print("Hello!")

say_hello()
```
Here, @logger adds behavior to say_hello() without modifying its core logic.

---

📋 Classwork: Day 2

- Create a list of your three favorite books and print the second one.

- Write a tuple to store your screen resolution.

- Make a dictionary that stores your name, age, and favorite color.

- Write a class Car with attributes brand and year. Add a method display() that prints a formatted string.

- Write a decorator that prints "Before calling" and "After calling" around any function you decorate.



