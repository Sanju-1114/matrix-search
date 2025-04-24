# Matrix Search

This repository contains a solution to LeetCode Problem 240: Search a 2D Matrix II, implemented in C++.

## Problem Description

Write an efficient algorithm that searches for a value `target` in an `m x n` matrix `mat`. This matrix has the following properties:
- Integers in each row are sorted in ascending order from left to right.
- Integers in each column are sorted in ascending order from top to bottom.

## Solution

The solution is implemented in `twoD_vectors_SearchII.cpp`. It uses an efficient search algorithm starting from the top-right corner of the matrix and leverages the sorted properties to eliminate rows or columns in each step.

### Algorithm
- Start from the top-right corner (`row = 0`, `col = n-1`).
- Compare the target with the current element:
  - If equal, return `true`.
  - If the target is smaller, move left (eliminate the current column).
  - If the target is larger, move down (eliminate the current row).
- Continue until the target is found or the search goes out of bounds.
- Return `false` if the target is not found.

### Time Complexity
- **O(m + n)**, where `m` is the number of rows and `n` is the number of columns, as we traverse at most `m` rows and `n` columns.

### Space Complexity
- **O(1)**, as no extra space is used.

## Files
- `twoD_vectors_SearchII.cpp`: Contains the C++ implementation of the search algorithm and a sample test case.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/Sanju-1114/matrix-search.git
   ```
2. Compile and run the C++ code:
   ```bash
   g++ twoD_vectors_SearchII.cpp -o matrix_search
   ./matrix_search
   ```
3. The sample test case searches for `target = 5` in a predefined matrix and outputs `1` (true) if found, or `0` (false) if not.

## Example

For the matrix:
```
[[1, 4, 7, 11, 15],
 [2, 5, 8, 12, 19],
 [3, 6, 9, 16, 22],
 [10, 13, 14, 17, 24],
 [18, 21, 23, 26, 30]]
```
Searching for `target = 5` returns `true`.

## Author
- GitHub: [Sanju-1114](https://github.com/Sanju-1114)

## License
This project is licensed under the MIT License.