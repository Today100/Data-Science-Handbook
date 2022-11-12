# NumPy

- Numeric Python Library.
- Working with **arrays** and perform numerical computations.

## NumPy array

- A grid of elements of the same type.
- Indexed by a tuple of nonnegative integers.
- Similar to Python Lists except they require lless memory and usually faster because of the use of optimized, precompiled C code.
- Supports *element-wise operations*.
  - Perform basic arithmetic on entire array using compact and readable code.

## Installing NumPy

```console
$ pip install Numpy
```

## Creating NumPy Array

- A 2d array:
```Python

import numpy as np

jeff_salary = [2700, 3000, 3000]
nick_salary = [2600, 2800, 2800]
tom_salary = [2300, 2500, 2500]

base_salary = np.array([jeff_salary, nick_salary, tom_salary])

print(base_salary)
# [[2700 3000 3000]
#  [2600 2800 2800]
#  [2300 2500 2500]]
```

# Performing Element-Wise Operations

```Python

jeff_bonus = [500, 400, 400]
nick_bonus = [600, 300, 400]
tom_bonus = [200, 500, 400]
bonus = np.array([jeff_bonus, nick_bonus, tom_bonus])

salary_bonus = base_salary + bonus

print(type(salary_bonus))
print(salary_bonus)


```

## Using NumPy Statistical Functions

```Python

print(salary_bonus.max())
# 3400

# axis=1 means to search the array horizontally.
print(np.amax(salary_bonus, axis=1))
# [3400, 3200, 3000]

print(np.amax(salary_bonus, axis=0))
# [3200, 3400, 3400]

```


