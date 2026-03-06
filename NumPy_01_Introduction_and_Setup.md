# NumPy Training 

## Session 01 – Introduction and Setup

### 1. What is NumPy?

NumPy stands for **Numerical Python**. It is a core Python library used for **numerical computing** and working with **arrays and matrices**.

NumPy is widely used in:

* Data Science
* Machine Learning
* Scientific Computing
* Data Analysis

Many Python libraries such as **Pandas, SciPy, TensorFlow, and Scikit‑learn** depend on NumPy.

### Key Feature

NumPy provides a powerful object called **ndarray (N‑Dimensional Array)** that allows fast mathematical operations on large datasets.

Example:

```python
import numpy as np

arr = np.array([10,20,30,40])

print(arr)
print(type(arr))
```

Output

```
[10 20 30 40]
<class 'numpy.ndarray'>
```

---

## 2. Installing NumPy

If NumPy is not installed:

```bash
pip install numpy
```

Inside Jupyter Notebook:

```python
!pip install numpy
```

---

## 3. Importing NumPy

Standard import convention:

```python
import numpy as np
```

Why use `np`?

Because NumPy functions are used frequently and the alias makes code shorter.

Example

```python
np.array([1,2,3])
```

---

## 4. NumPy vs Python Lists

### Python List Example

```python
a = [10,20,30]
b = [1,2,3]

print(a + b)
```

Output

```
[10,20,30,1,2,3]
```

Lists **concatenate** instead of performing mathematical operations.

---

### NumPy Array Example

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

NumPy performs **element‑wise mathematical operations**.

---

## 5. Performance Comparison

Python List

```python
import time

size = 1000000

list1 = list(range(size))
list2 = list(range(size))

start = time.time()

result = [list1[i] + list2[i] for i in range(size)]

print("List Time:", time.time() - start)
```

NumPy Version

```python
import numpy as np

arr1 = np.arange(size)
arr2 = np.arange(size)

start = time.time()

result = arr1 + arr2

print("NumPy Time:", time.time() - start)
```

NumPy is significantly **faster** because it is implemented in **C internally**.

---

## 6. NumPy Version and Configuration

Check installed version:

```python
import numpy as np

print(np.__version__)
```

Check configuration:

```python
np.show_config()
```

This shows system optimization details such as BLAS and LAPACK libraries.

---

## 7. Creating NumPy Arrays

### From Python List

```python
import numpy as np

arr = np.array([5,10,15,20])

print(arr)
```

---

### 2D Array (Matrix)

```python
matrix = np.array([
    [1,2,3],
    [4,5,6]
])

print(matrix)
```

---

## 8. Basic NumPy Workflow

Typical data science workflow:

```
Raw Data → NumPy Array → Analysis → Result
```

Example

```python
import numpy as np

data = [45,50,60,55,70]

arr = np.array(data)

print("Mean:", np.mean(arr))
print("Max:", np.max(arr))
print("Min:", np.min(arr))
```

---

# Session 02 – Array Creation Methods

## 1. Creating Arrays Using NumPy Functions

NumPy provides several built‑in functions to generate arrays quickly.

---

## 2. zeros()

Creates an array filled with **0**.

```python
import numpy as np

arr = np.zeros(5)
print(arr)
```

Output

```
[0. 0. 0. 0. 0.]
```

2D Example

```python
matrix = np.zeros((3,3))
print(matrix)
```

---

## 3. ones()

Creates an array filled with **1**.

```python
arr = np.ones(5)
print(arr)
```

2D Example

```python
matrix = np.ones((2,4))
print(matrix)
```

---

## 4. arange()

Works similar to Python's `range()` but returns a NumPy array.

```python
arr = np.arange(10)
print(arr)
```

Output

```
[0 1 2 3 4 5 6 7 8 9]
```

Example with step

```python
arr = np.arange(0,20,2)
print(arr)
```

Output

```
[0 2 4 6 8 10 12 14 16 18]
```

---

## 5. linspace()

Creates evenly spaced numbers between two values.

```python
arr = np.linspace(0,10,5)
print(arr)
```

Output

```
[0. 2.5 5. 7.5 10.]
```

---

## 6. random() Arrays

NumPy can generate random numbers.

Random values between 0 and 1:

```python
arr = np.random.rand(5)
print(arr)
```

Random integers:

```python
arr = np.random.randint(1,100,5)
print(arr)
```

---

## 7. Array Shape and Dimensions

Example array

```python
arr = np.array([
    [1,2,3],
    [4,5,6]
])
```

Shape

```python
print(arr.shape)
```

Output

```
(2,3)
```

Dimensions

```python
print(arr.ndim)
```

Output

```
2
```

Size

```python
print(arr.size)
```

Output

```
6
```

---

# Practice Exercises

## Exercise 1

Create a NumPy array containing:

```
[5,10,15,20,25]
```

---

## Exercise 2

Create two arrays:

```
A = [2,4,6]
B = [1,3,5]
```

Add them using NumPy.

Expected Output

```
[3 7 11]
```

---

## Exercise 3

Create a NumPy array for temperatures:

```
[30,32,35,40,28]
```

Find:

* Average temperature
* Maximum temperature

---

