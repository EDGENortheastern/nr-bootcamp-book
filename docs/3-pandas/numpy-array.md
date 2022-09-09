---
sidebar_position: 1
---

# D3S1. NumPy Arrays

## NumPy

[NumPy](https://numpy.org/) NumPy stands for Numerical Python; it is a scientific computing package. It is mostly used for array computing, however, it also has many advanced mathematical functions.

The Data Science convention prescribes importing NumPy as so:

```python
import numpy as np
```

NumPy methods can then be used as so:

```python
rand_num = np.random.randint(0,10) #generates a random integer
```

## `np.array()`

**NumPy Array** is one of the key data structures for Data Analysts. It:

- is more efficient than a list (faster, more Pythonic, and has less memory footprint)
- homogenous
- allows operating on a set of values at one time (vectorized arithmetic operations)
- allows masking and filtering on a set of values without using loops or filter### Definition



## Vector arithmetics

If a plus sign is used on two lists, they get concatenated.

<iframe title="Embedded cell output" src="https://embed.deepnote.com/ff8ed217-77e5-445b-8d27-e9d948f86164/d3df9fff-7fb4-419a-bf26-61f6e4ba4bdc/eb498df3-dd65-4bb8-b355-dac133a1de81?height=171.1875" height="171.1875" width="500"/>

Data Analysts often need to operate on all values in a data set. To make it easier, NumPy arrays allow performing vectorised arithmetics, e.g., operations on all values in arrays.

<iframe title="Embedded cell output" src="https://embed.deepnote.com/ff8ed217-77e5-445b-8d27-e9d948f86164/d3df9fff-7fb4-419a-bf26-61f6e4ba4bdc/3f576c61-127b-41b9-858c-d6179e291695?height=171.1875" height="171.1875" width="500"/>

## Boolean NumPy arrays

Boolean NumPy arrays work as masks. They allow one-line filtering of array values. Pandas data frames are filtered in a similar way.

<iframe title="Embedded cell output" src="https://embed.deepnote.com/ff8ed217-77e5-445b-8d27-e9d948f86164/d3df9fff-7fb4-419a-bf26-61f6e4ba4bdc/09c4f2dc-3fba-4c28-bca3-3200faf9f4f7?height=171.1875" height="171.1875" width="500"/>

## Deepnote

Duplicate the Deepnote below, run or re-run the cells and try the tasks (signposted 🏋️).

[<img
    src="/img/icons/deepnote-logo.svg"
    alt="Deepnote link"
/>](https://deepnote.com/project/NumPy-KqjsNni3QSusyM2sOb-Tbg/%2Fnumpy.ipynb)
