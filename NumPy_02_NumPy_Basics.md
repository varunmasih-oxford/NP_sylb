
# Session 01 – Introduction and Setup

## What is NumPy

NumPy (Numerical Python) is a Python library used for:

* Numerical computing
* Working with arrays and matrices
* Fast mathematical calculations
* Scientific computing

NumPy is the **foundation of many data science libraries** such as:

* Pandas
* SciPy
* Scikit‑learn
* TensorFlow

---

## Installing NumPy

```bash
pip install numpy
```

In Jupyter Notebook:

```python
!pip install numpy
```

---

## Importing NumPy

```python
import numpy as np
```

---

## NumPy vs Python Lists

Python List

```python
a = [10,20,30]
b = [1,2,3]

print(a + b)
```

Output

```
[10,20,30,1,2,3]
```

NumPy Array

```python
import numpy as np

a = np.array([10,20,30])
b = np.array([1,2,3])

print(a + b)
```

Output

```
[11 22 33]
```

NumPy performs **element‑wise operations**.

---

## Checking NumPy Version

```python
import numpy as np

print(np.__version__)
```

---

# Session 02 – Array Creation

## Creating Arrays from Lists

```python
import numpy as np

arr = np.array([1,2,3,4])
print(arr)
```

---

## Creating Arrays from Tuples

```python
arr = np.array((10,20,30))
print(arr)
```

---

## Creating 2D Arrays

```python
matrix = np.array([
    [1,2,3],
    [4,5,6]
])

print(matrix)
```

---

## arange()

Works like Python range but returns a NumPy array.

```python
arr = np.arange(0,10)
print(arr)
```

Step example

```python
arr = np.arange(0,20,2)
```

---

## linspace()

Creates evenly spaced numbers.

```python
arr = np.linspace(0,10,5)
print(arr)
```

---

## logspace()

Creates numbers spaced evenly on a logarithmic scale.

```python
arr = np.logspace(1,3,5)
print(arr)
```

---

## zeros()

```python
arr = np.zeros(5)
print(arr)
```

2D example

```python
matrix = np.zeros((3,3))
```

---

## ones()

```python
arr = np.ones(4)
```

---

## empty()

```python
arr = np.empty(5)
```

Values are not initialized.

---

## full()

```python
arr = np.full(5,7)
```

2D example

```python
matrix = np.full((3,3),9)
```

---

## Identity Matrix

```python
matrix = np.eye(3)
```

---

## Diagonal Matrix

```python
matrix = np.diag([1,2,3,4])
```

---

# Session 03 – Random Arrays

## rand()

```python
arr = np.random.rand(5)
```

2D

```python
matrix = np.random.rand(3,3)
```

---

## randint()

```python
arr = np.random.randint(1,100,5)
```

---

## randn()

Normal distribution values.

```python
arr = np.random.randn(5)
```

---

# Session 04 – Indexing and Slicing

## Basic Indexing

```python
arr = np.array([10,20,30,40,50])

print(arr[0])
print(arr[3])
```

---

## Basic Slicing

```python
print(arr[1:4])
print(arr[:3])
print(arr[2:])
```

---

## Advanced Indexing

```python
print(arr[[0,2,4]])
```

---

## Boolean Indexing

```python
print(arr[arr > 25])
```

---

## Fancy Indexing

```python
index = [1,3,4]
print(arr[index])
```

---

## Indexing in Multi‑Dimensional Arrays

```python
matrix = np.array([
 [1,2,3],
 [4,5,6],
 [7,8,9]
])

print(matrix[0,1])
print(matrix[:,1])
print(matrix[0:2,1:3])
```

---

# Session 05 – Reshaping Arrays

## reshape()

```python
arr = np.arange(12)

matrix = arr.reshape(3,4)
print(matrix)
```

---

## flatten()

```python
flat = matrix.flatten()
```

---

## ravel()

```python
flat = matrix.ravel()
```

---

# Session 06 – Mathematical Operations

```python
arr = np.array([10,20,30])

print(arr + 5)
print(arr * 2)
print(arr ** 2)
```

Element‑wise operations

```python
a = np.array([1,2,3])
b = np.array([4,5,6])

print(a + b)
print(a * b)
```

---

# Session 07 – Statistics Functions

```python
arr = np.array([10,20,30,40,50])

print(np.mean(arr))
print(np.median(arr))
print(np.std(arr))
print(np.sum(arr))
print(np.min(arr))
print(np.max(arr))
```

---

# Session 08 – Axis Operations

```python
matrix = np.array([
 [1,2,3],
 [4,5,6]
])

print(np.sum(matrix, axis=0))
print(np.sum(matrix, axis=1))
```

---

# Mini Data Science Example

Student marks analysis.

```python
marks = np.array([72,65,80,90,55,60])

print("Average", np.mean(marks))
print("Highest", np.max(marks))
print("Lowest", np.min(marks))
```

---

# Practice Exercises

## Exercise 1

Create an array using `arange()` from **1 to 20 with step 2**.

---

## Exercise 2

Create a **3x3 matrix filled with 5** using `full()`.

---

## Exercise 3

Generate **5 random integers between 10 and 50**.

---

## Exercise 4

Create the matrix below and print the **second column**.

```
[[1,2,3]
 [4,5,6]
 [7,8,9]]
```

---
