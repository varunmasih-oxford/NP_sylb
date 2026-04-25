
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

# NumPy Sessions 03–08

## Topic: Random Arrays, Indexing, Reshaping, Operations & Statistics


## Part A: Random Arrays

1. Create a 1D array of 5 random float values using `rand()`.  
2. Create a 3×3 matrix of random float values.  
3. Generate a 1D array of 5 random integers between 1 and 100 using `randint()`.  
4. Create a 1D array of 5 values from a normal distribution using `randn()`.

---

## Part B: Indexing and Slicing

5. Given the array:
```python
import numpy as np

arr = np.array([10, 20, 30, 40, 50])
````

Perform the following:

* Print the first and fourth element
* Slice elements from index 1 to 3
* Slice first three elements
* Slice elements from index 2 to end

---

## Part C: Advanced Indexing

6. Using the same array:

* Access elements at index positions [0, 2, 4]
* Print elements greater than 25 using boolean indexing
* Use fancy indexing with index list [1, 3, 4]

---

## Part D: Multi-Dimensional Indexing

7. Given the matrix:

```python
matrix = np.array([
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
])
```

Perform the following:

* Access element at row 0, column 1
* Print all elements of column 1
* Slice a sub-matrix (first 2 rows, last 2 columns)

---

## Part E: Reshaping Arrays

8. Create an array using `arange(12)` and:

* Reshape it into a 3×4 matrix
* Flatten the matrix using `flatten()`
* Flatten the matrix using `ravel()`

---

## Part F: Mathematical Operations

9. Given:

```python
arr = np.array([10, 20, 30])
```

Perform:

* Add 5 to each element
* Multiply each element by 2
* Square each element

Also perform element-wise operations:

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
```

* Add arrays
* Multiply arrays

---

## Part G: Statistical Functions

10. Given:

```python
arr = np.array([10, 20, 30, 40, 50])
```

Calculate:

* Mean
* Median
* Standard deviation
* Sum
* Minimum value
* Maximum value

---

## Part H: Axis Operations

11. Given:

```python
matrix = np.array([
    [1, 2, 3],
    [4, 5, 6]
])
```

Perform:

* Sum along columns (axis = 0)
* Sum along rows (axis = 1)

---
```
import numpy as np


for row in arr:
    for x in row:
        print(x, end=" ")
# Output: 1 2 3 4 


for x in arr.flat:
    print(x, end=" ")
# Output: 1 2 3 4 


# 1. COMBINING ARRAYS
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

# Stacking: vstack (vertical) and hstack (horizontal)
v_stack = np.vstack((a, b))  # Result: [[1,2,3], [4,5,6]]
h_stack = np.hstack((a, b))  # Result: [1,2,3,4,5,6]

# Concatenate along a specific axis (must be same dimensions)
c = np.array([[1, 2], [3, 4]])
d = np.array([[5, 6]])
concat = np.concatenate((c, d), axis=0) # Adds d as a new row

# 2. COPYING VS. VIEWING
original = np.array([10, 20, 30])

# Shallow Copy (View) - Shares memory
view_arr = original.view()
view_arr[0] = 99  # This ALSO changes 'original'

# Deep Copy - Independent memory
copy_arr = original.copy()
copy_arr[1] = 88  # This does NOT change 'original'

print(f"Original after mods: {original}") 
# Output: [99, 20, 30] (Index 0 changed via view, Index 1 stayed 20)
```
