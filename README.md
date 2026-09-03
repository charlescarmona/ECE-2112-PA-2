# ECE-2112-PA-2

** Made by: Charles John M. Carmona | 2ECE-B**

The content of this repository contains the Programming Assignment for the course " Advance Computer Programming " this S.Y. 2026-2027.

# **A. REPRODUCIBLE NORMALIZATION PROBLE**

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
```
