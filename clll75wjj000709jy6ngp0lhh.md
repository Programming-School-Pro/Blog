---
title: "Learning numpy The best library to analyze your data part 1"
datePublished: Mon Aug 21 2023 18:14:57 GMT+0000 (Coordinated Universal Time)
cuid: clll75wjj000709jy6ngp0lhh
slug: learning-numpy-the-best-library-to-analyze-your-data-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/npxXWgQ33ZQ/upload/0342039f54a30956d5d3910a8075f827.jpeg
tags: python, numpy, python-beginner

---

Hello Everyone

Today I will talk about numpy and How to analyze data using it.

# Introduction

What is NumPy? NumPy is **a Python library used for working with arrays**. It also has functions for working in domain of linear algebra, Fourier transform, and matrices. NumPy was created in 2005 by Travis Oliphant. It is an open source project and you can use it freely.

# How to use it?

First you must install it using pip(Python must be installed and pip must be added to the path)

Run The following command in the terminal or the command prompt:

```bash
pip install numpy
```

Then if you want to use it you must call it as following:

```python
import numpy as np # To be easy to call it
```

# Numpy Intro

Now First Thing you must know that numpy creates its own array as following:

```python
import numpy as np

arr = np.array([1,2,3,4,5,6])

print(arr)

# Output: [1 2 3 4 5 6]
```

And If you want to call one index you call it as usual !

## Array Slicing

You can take a part of the array very easy as following:

```python
import numpy as np

# indexes       0,1,2,3,4,5
arr = np.array([1,2,3,4,5,6])

print(arr[:2]) # To get first two values 
# Output: [1,2]
print(arr[2:]) # To get the values from index 2 to the last
# Output: [3,4,5,6]
print(arr[2:5]) # To get the values from index 2 to 5
# Output: [3,4,5,6]
```

# End

Thank you for reading and if you like this please follow

Bye