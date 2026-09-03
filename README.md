# ECE-2112-PA-2

** Made by: Charles John M. Carmona | 2ECE-B**

The content of this repository contains the Programming Assignment for the course " Advance Computer Programming " this S.Y. 2026-2027.

# **A. REPRODUCIBLE NORMALIZATION PROBLEM**

Create a 5 x 5 array with random integers from 10 to 100, then normalize it using the Z-score formula.

The functions used for this are the following;
- `np.random.seed(2112)` - This sets the starting point for random numbers.
- `np.random.randint(10,101, size=(5, 5))` - Generates a 5 x 5 array of random integers.
- `X.std()` and `X.mean()` - These calculates the mean and standard deviation of the array.
- `(X - X.mean()) / X.std()` - This one normalizes the array
- `np.save()` - This saves the array as an `.npy` file

```python
import numpy as np
np.random.seed(2112)
X = np.random.randint(10,101, size=(5, 5))
X_normalized = (X - X.mean()) / X.std()

print (X)
print (X_normalized)
print (X_normalized.std)
print (X_normalized.mean)

np.save(“X_normalized.npy”, X_normalized)
```

# **B. Cubes Divisible by 4 Problem**

Create n array of the first positive 100 integers then cube each value. The integers will be then reshaped into a 10x10 array and the only number that are divisible by 4 will be selected.

The functions used in this problem are the following:
- ‘np.arange(1,10)’ - This Creates an array from 1 to 100.
- ‘(N ** 3).reshape(10,10)’ - This is responsible for cubing and reshaping the array into 10 rows and columns.
- ‘C[C % 4 == 0]’ - This filters and returns the values that satisfies the condition.

‘’’python
N = np.arange(1,101)
C = (N ** 3).reshape(10,10)

div_by_4 = C[C % 4 == 0]

print(C.shape)
