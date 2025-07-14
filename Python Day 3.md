# 📅 Day 3: NumPy, Pandas + Inheritance

## ✍️ Topics Covered
- NumPy arrays and vectorized operations
- Statistical functions
- Introduction to Pandas DataFrames
- Handling missing values
- Class Inheritance and method overriding

---

## ✅ NumPy Basics

**NumPy** is a fast, efficient library for numerical computing. It provides a high-performance array object and tools to work with them.

### Creating an Array:
```python
import numpy as np

arr = np.array([1, 2, 3, 4])
print(arr)           # [1 2 3 4]
print(arr.shape)     # (4,)
print(arr.mean())    # 2.5
```
Unlike Python lists, NumPy arrays support vectorized operations:

```python
arr2 = arr * 2
print(arr2)  # [2 4 6 8]
```

Use NumPy for mathematical operations on entire datasets.

---

## ✅ NumPy Statistical Functions

NumPy provides built-in functions for basic stats:
```python
print(arr.sum())       # 10
print(arr.mean())      # 2.5
print(arr.std())       # Standard deviation
print(np.median(arr))  # Median
```

You can also reshape, slice, and generate random data using:
```python
np.random.rand(3, 2)   # Random 3x2 matrix
```

---

## ✅ Pandas Basics

**Pandas** is a powerful library for data analysis. It provides two main data structures:

    Series: like a column in Excel

    DataFrame: like a full spreadsheet

### Loading a dataset:
```python
import pandas as pd

df = pd.read_csv("titanic.csv")
print(df.head())
print(df.info())
```
### Handling Missing Data

Missing data is common in real-world datasets.
#### Checking for missing values:
```python
print(df.isnull().sum())
```

#### Filling missing values:
```python
df["Age"].fillna(df["Age"].mean(), inplace=True)
```

#### Dropping missing data:
```python
df.dropna(inplace=True)
```
Cleaning your data is essential before analysis or modeling.

### Grouping and Aggregation

#### Use .groupby() to summarize data:
```python
df.groupby("Pclass")["Fare"].mean()
```
This example shows the average fare per passenger class.

---

## ✅ Inheritance in Classes

Inheritance lets you define a class that inherits from another class. It's useful for code reuse and specialization.
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(f"{self.name} makes a sound")
```

Subclass:
```python
class Dog(Animal):
    def speak(self):
        print(f"{self.name} says Woof!")

d = Dog("Buddy")
d.speak()  # Buddy says Woof!
```

You can override methods in the child class or extend functionality by adding new methods.

---

📋 Classwork: Day 3

- Create a NumPy array of numbers from 1 to 10. Compute the sum, mean, and standard deviation.

- Load the Titanic dataset and count how many values are missing in the Age column.

- Fill missing values in Age with the average age and show the result.

- Create a class Employee with name and salary. Then create a subclass Manager with an extra department attribute and a method to display full details.



