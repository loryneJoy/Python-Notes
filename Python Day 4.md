# 📅 Day 4: Data Wrangling + Visualization

## ✍️ Topics Covered
- Filtering and sorting DataFrames
- Feature engineering
- Grouping and aggregation
- Merging/joining DataFrames
- Data visualization with Matplotlib and Seaborn

---

## ✅ Filtering and Sorting Data

### Filtering
Use **boolean indexing** to filter rows based on conditions:
```python
import pandas as pd

df = pd.read_csv("titanic.csv")
adults = df[df["Age"] >= 18]
print(adults.head())
```

### Sorting:
```python
df_sorted = df.sort_values(by="Fare", ascending=False)
print(df_sorted.head())
```
Filtering and sorting are critical for focusing on relevant parts of your data.

---

## ✅ Feature Engineering

Feature engineering means creating new columns that help improve your analysis or model.

### Example: Creating age groups
```python
df["AgeGroup"] = pd.cut(df["Age"], bins=[0, 12, 19, 59, 100], labels=["Child", "Teen", "Adult", "Senior"])
```

### Extracting titles from names:
```python
df["Title"] = df["Name"].apply(lambda name: name.split(",")[1].split(".")[0].strip())
```
These new features can be very valuable in predictions or segmentation.

---

## ✅ Grouping and Aggregation

Use .groupby() and .agg() to compute statistics for subgroups:
```python
grouped = df.groupby("Pclass")["Survived"].agg(["count", "mean"])
print(grouped)
```
This tells us how many people survived from each passenger class and the survival rate.

---

## Merging DataFrames

Sometimes, your dataset is split across multiple files or tables. You can join them using:
```python
df1 = pd.DataFrame({"ID": [1, 2], "Name": ["Alice", "Bob"]})
df2 = pd.DataFrame({"ID": [1, 2], "Age": [25, 30]})

merged = pd.merge(df1, df2, on="ID")
print(merged)
```
This is similar to SQL joins and essential in real-world analytics.

---

## ✅ Data Visualization with Matplotlib

Matplotlib is Python’s basic plotting library.

### Line and bar charts:
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [2, 4, 6, 8]
plt.plot(x, y)
plt.title("Line Chart")
plt.show()
```
### Histogram:
```python
plt.hist(df["Age"].dropna(), bins=20)
plt.title("Age Distribution")
plt.xlabel("Age")
plt.ylabel("Count")
plt.show()
```

---

## ✅ Data Visualization with Seaborn

Seaborn builds on Matplotlib and adds beautiful default styles.

### Count plot:
```python
import seaborn as sns

sns.countplot(data=df, x="Pclass")
```

### Box plot:
```python
sns.boxplot(data=df, x="Pclass", y="Fare")
```

### Correlation heatmap:
```python
sns.heatmap(df.corr(), annot=True, cmap="coolwarm")
```
Visuals help communicate insights quickly and effectively.


📋 Classwork: Day 4

- Load the Titanic dataset and filter rows where Fare > 50. Sort by Age.

- Create a new column FarePerPerson by dividing Fare by the number of parents/children (Parch + 1).

- Group the data by Sex and show the average age and survival rate.

- Merge two DataFrames: one with names and IDs, another with ages and IDs.

- Plot a histogram of the Age column and a count plot of the Pclass.


