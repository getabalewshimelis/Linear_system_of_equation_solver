# Linear System Solver using Gauss-Jordan Elimination

![Python](https://img.shields.io/badge/Python-3.x-blue)
![NumPy](https://img.shields.io/badge/NumPy-supported-orange)


## Overview

This project implements a **linear system solver from scratch** using the
**Gauss-Jordan elimination algorithm with row pivoting**.

The goal of this project is to understand the mathematical foundations behind
linear algebra algorithms and how these operations are used in fields such as
machine learning, data science, and scientific computing.

Instead of relying directly on built-in linear algebra solvers, this project
implements the elimination process manually and compares the results and
performance against `numpy.linalg.solve`.

---

## Features

- ✅ Gauss-Jordan elimination implemented from scratch
- ✅ Row pivoting for improved numerical stability
- ✅ Solves systems of linear equations:

\[
Ax = b
\]

- ✅ Randomized correctness testing against NumPy
- ✅ Performance benchmarking
- ✅ Comparison across multiple matrix sizes
- ✅ Visualization of execution time

---

## Algorithm Explanation

The solver works using the following steps:

1. Create an augmented matrix:

\[
[A|b]
\]

2. Select pivot elements.

3. Swap rows when the pivot is zero or too small.

4. Eliminate values above and below each pivot.

5. Extract the final solution vector.

The algorithm transforms the matrix into reduced row echelon form:

\[
[I|x]
\]

where `x` is the solution.

---

## Requirements

Install the required libraries:

```bash
pip install numpy matplotlib 
```



---

## How to Run

Clone the repository:

```bash
git clone https://github.com/getabalewshimelis/Linear_system_of_equation_solver.git
```

Open the notebook:

```bash
jupyter notebook Linear_System_Solver.ipynb
```

Run all cells to reproduce:

- Solver implementation
- Correctness tests
- Benchmark results
- Performance graphs

---

# Correctness Testing

The solver was tested using random nonsingular matrices and compared with:

```python
numpy.linalg.solve()
```

Example:

```
Correct : 10000/10000
Wrong   : 0
Failed  : 0
```

This confirms that the implementation produces the same solutions as NumPy
for tested cases.

---

# Performance Benchmark

The solver was tested on different matrix sizes.

Example results:

| Matrix Size | Custom Solver | NumPy | Speed Ratio |
|------------|---------------|-------|-------------|
| 5 × 5 | 61.60 µs | 9.36 µs | 6.58x |
| 10 × 10 | 223.86 µs | 10.21 µs | 21.92x |
| 20 × 20 | 867.09 µs | 18.46 µs | 46.97x |
| 50 × 50 | 5492.84 µs | 44.54 µs | 123.31x |
| 100 × 100 | 22717.02 µs | 105.34 µs | 215.66x |

---

## Performance Analysis

The custom solver is slower than NumPy because NumPy uses optimized LAPACK
implementations written in compiled languages.

The custom implementation is written mainly for:

- Learning numerical algorithms
- Understanding matrix operations
- Studying the mathematics behind machine learning algorithms

For production-level computation, optimized libraries such as NumPy are
preferred.

---

## Technologies Used

- Python
- NumPy
- Matplotlib
- Jupyter Notebook

---



## Learning Outcomes

Through this project, I learned:

- How Gaussian elimination algorithms work internally
- How row pivoting improves stability
- How to test numerical algorithms
- How to benchmark implementations
- How linear algebra supports machine learning systems

---

## Author

**Getabalew Shimelis**

