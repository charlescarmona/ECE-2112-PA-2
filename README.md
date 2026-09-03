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

``` python
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
print(div_by_4)
print(div_by_4.size)

np.save("div_by_4.npy", div_by_4)
‘’’
# **C. Above-mean Squares Problems**

Create a 6 x 6 array containing the squares of numbers from 1 to 36, calculate its mean, and select only the values greater than the mean.

The functions used in this problem are the following :
- ‘(np.arange(1,37) ** 2).reshape(6,6) - This squares the numbers 1 to 36 and shapes them into a 6 x 6 array.
- ‘S.mean()’ - Calculates the mean of the array.
- ‘S[S > S_mean] - This Filters the values that are greater than the mean

‘’’python
S = (np.arange(1,37) ** 2).reshape(6,6)
S_mean = S.mean()

above_mean = S[S > S_mean]

print(S)
print(S_mean)
print(above_mean)
print(above_mean.size)

np.save(“above_mean.npy”, above_mean)
‘’’

I appreciate that you read this.

Click the link below to see the full main python program:

https://github.com/charlescarmona/ECE-2112-PA-2/blob/main/ProgrammingAssignment2.ipynb

# **Readme File Version History:**

September 3, 2026 - initial Readme Content uploaded

September 3, 2026 - final Readme Content uploaded
