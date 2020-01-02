# 2 - Leveraging Pre-Trained Models

__1. What is the use of `.transpose` and `.reshape` in the pre-processing ?__

`reshape` is more intuitive to explain, simply put when you try to have a different matrix/array/tensor shape from the one you originally have, say 4 by 4, and you would want to reshape it into 2 by 8, then you will need to use .reshape. On the other hand, `transpose` is inherently a matrix operation. It is an operation to interchange each row with the corresponding column. But in both cases the dimensionalities before and after the so-called "transformation" has to conform to some conservation rule like the number of elements contained in the case of .reshape. Here it's an [article](https://lihan.me/2018/01/numpy-reshape-and-transpose/) that compare both methods
