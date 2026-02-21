# Day 02 — NumPy Fundamentals (Why Machine Learning = Math)

## 🎯 Objective

Understand why machine learning models use numerical arrays instead of normal Python lists and learn the basics of NumPy operations.

---

## 🧠 Key Idea

Machine Learning models do not understand Python objects.

They only understand **numbers organized in vectors and matrices**.

Example dataset:

| Height | Weight | Age |
| ------ | ------ | --- |
| 170    | 65     | 30  |
| 160    | 55     | 25  |
| 180    | 80     | 40  |

The model actually sees:

```
[
 [170,65,30],
 [160,55,25],
 [180,80,40]
]
```

This is called a **matrix**.

Python lists are slow for math operations.
NumPy uses optimized C code → much faster numerical computation.

All ML frameworks (scikit-learn, TensorFlow, PyTorch) depend on this concept.

---

## 🔢 Vectors vs Matrices

Vector (1-D array)

```
[10, 20, 30]
```

Matrix (2-D array)

```
[
 [10,20,30],
 [40,50,60]
]
```

---

## 💻 Hands-On Practice

Open your notebook `day02_numpy.ipynb`

### 1️⃣ Import NumPy

```python
import numpy as np
```

---

### 2️⃣ Create Arrays

```python
a = np.array([1,2,3,4])
print(a)
```

Matrix:

```python
b = np.array([[1,2,3],
              [4,5,6]])
print(b)
```

---

### 3️⃣ Shape of Data (Very Important)

```python
print(a.shape)   # vector
print(b.shape)   # matrix
```

ML models expect specific shapes.

---

### 4️⃣ Mathematical Operations

```python
a = np.array([1,2,3])
b = np.array([4,5,6])

print(a + b)
print(a * b)
print(a.mean())
```

No loops needed — vectorized computation.

---

### 5️⃣ Performance Comparison

```python
import time

python_list = list(range(1000000))
numpy_array = np.arange(1000000)

start = time.time()
sum(python_list)
print("Python list:", time.time() - start)

start = time.time()
numpy_array.sum()
print("NumPy array:", time.time() - start)
```

NumPy will be significantly faster.

---

## 🧠 Why This Matters in AI

Machine learning training = repeated large matrix operations.

Speed difference determines:

* training time
* inference latency
* scalability

NumPy is the mathematical foundation of ML.

---

## 🧩 Exercises

Try yourself before checking answers.

### Q1

Create a vector `[5,10,15,20]` and calculate its average.

### Q2

Create a 2×2 matrix and print its shape.

### Q3

Multiply two arrays element-wise:

```
[2,4,6] and [1,3,5]
```

---

## ✅ Answers

```python
# Q1
arr = np.array([5,10,15,20])
print(arr.mean())

# Q2
m = np.array([[1,2],[3,4]])
print(m.shape)

# Q3
a = np.array([2,4,6])
b = np.array([1,3,5])
print(a*b)
```

---

## 📌 Outcome

You now understand:

* vectors & matrices
* numerical computation
* why ML relies on linear algebra
* why NumPy is required before ML frameworks

---

## 🔜 Next

Day 03 — Pandas (Working with datasets)
