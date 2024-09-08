# EXPERIMENT 2 - NUMERICAL PYTHON

This repository feautures Python scripts designed to solve varipus problems in ECE2112. Below is a summary of each script included. 

### 1. Normalization Problem

###### This problem involves normalizing a random 5x5 array. The task is to create a random 5x5 array, normalize it by centering (subtracting the mean), scaling (dividing by the standard deviation), and saving the normalized array as a file named X_normalized.npy.

**Function:**

```python

import numpy as np

#create a random 5x5 array
X = np.random.random((5,5))

#declare variables to be normalized
X_mean=np.mean(X)
X_std=np.std(X)

#normalize values from array
X_normalized = (X - X_mean)/(X_std)

#save array into ".npy" file
np.save('X_normalized.npy', X_normalized)

#output the saved file
print("\nOriginal Array:\n", X)
print("\nNormalized Array:\n", X_normalized)

```
**Output:**

![image](https://github.com/user-attachments/assets/084a052b-61ad-4b27-a765-a493d0cf7880)


### 2. Divisible by 3 Problem

###### This problem involves creating a 10x10 array containing the squares of the first 100 positive integers. The task is to identify all elements in this array that are divisible by 3 and save the resulting elements as a file named div_by_3.npy.


**Function:**

```python

import numpy as np

#create an array of the first 100 positive integers
squares = np.arange(1, 101) ** 2

#reshape to a 10x10 array
squares_10x10 = squares.reshape(10, 10)

#find all values that are divisible by 3
div_by_3 = squares_10x10[squares_10x10 % 3 == 0]

#save array into ".npy" file
np.save('div_by_3.npy', div_by_3)

#output the saved file
data = np.load('div_by_3.npy')
data

```

**Output:**

![image](https://github.com/user-attachments/assets/5aec10a3-eaa1-48f8-ba41-53cea75c7351)
