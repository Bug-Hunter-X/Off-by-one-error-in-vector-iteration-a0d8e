# Off-by-one error in vector iteration

This repository demonstrates a common off-by-one error in C++ when iterating over a vector. The error occurs when the loop condition incorrectly includes the last element's index, leading to accessing memory outside the vector's bounds.

## Bug Description

The `bug.cpp` file contains a `for` loop that iterates through a vector. The loop condition uses `i <= vec.size()`, which causes an out-of-bounds access when `i` reaches the size of the vector. This results in undefined behavior and potential crashes or unexpected output.

## Bug Solution

The `bugSolution.cpp` file demonstrates the corrected code. The loop condition is changed to `i < vec.size()`, ensuring that the loop iterates only up to the last valid index of the vector. 