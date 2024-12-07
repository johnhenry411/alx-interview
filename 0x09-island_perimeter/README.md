# Island Perimeter Problem 
## Overview
This Python script provides a function `island_perimeter(grid)` that calculates the perimeter of an island described in a 2D grid of integers. The grid consists of `0`s representing water and `1`s representing land. The function computes the total perimeter by counting the boundaries of land cells exposed to water or the edge of the grid.

## Function: `island_perimeter(grid)`

### Description
The function `island_perimeter` takes a 2D list `grid` where each element is either a `0` (representing water) or a `1` (representing land). The function calculates the perimeter of the island, which is the total length of the boundary where land cells are adjacent to water cells or the grid’s border.

### Arguments

- **grid**: `List[List[int]]`
  - A 2D list representing the map of the island.
  - Each cell in the grid is either:
    - `1`: Land
    - `0`: Water
  - The grid is non-empty and will contain at least one row and one column.

### Return Value
- **Returns**: `int`
  - The perimeter of the island (the number of land cell edges exposed to water or the boundary of the grid).

### Detailed Algorithm

1. **Initialization**:
   - The perimeter `p` is initialized to 0. This variable will store the total perimeter value as it is computed.

2. **Iterating through the grid**:
   - The function uses two nested loops to iterate through the 2D grid:
     - Outer loop (`for i in range(len(grid))`): Iterates through each row of the grid.
     - Inner loop (`for j in range(len(grid[i]))`): Iterates through each column within the current row.

3. **Checking each land cell**:
   - For every land cell (`grid[i][j] == 1`), the algorithm checks its four potential neighboring cells:
     - **Top neighbor**: The cell above (`grid[i-1][j]`), if `i > 0`.
     - **Bottom neighbor**: The cell below (`grid[i+1][j]`), if `i < len(grid) - 1`.
     - **Left neighbor**: The cell to the left (`grid[i][j-1]`), if `j > 0`.
     - **Right neighbor**: The cell to the right (`grid[i][j+1]`), if `j < len(grid[i]) - 1`.

   - **Perimeter Contribution**:
     - For each of the four neighbors, if the neighbor is either out of bounds (meaning it is at the edge of the grid) or is water (`grid[x][y] == 0`), the current edge of the land cell contributes to the perimeter.
     - The perimeter is increased by 1 for each exposed side.

4. **Return the result**:
   - After all grid cells are processed, the function returns the accumulated perimeter `p`.

### Complexity Analysis

- **Time Complexity**: `O(m * n)`
  - Where `m` is the number of rows and `n` is the number of columns in the grid. The function loops over each cell in the grid once and performs constant-time checks for each neighbor.

- **Space Complexity**: `O(1)`
  - The function uses only a fixed amount of extra space for variables (`p`, `i`, `j`), regardless of the size of the grid. Therefore, the space complexity is constant.

### Example Usage

```python
grid = [
    [0, 1, 0, 0],
    [1, 1, 1, 0],
    [0, 1, 0, 0]
]

print(island_perimeter(grid))  # Output: 8
```

### Explanation of the Example
For the given grid:

```
0 1 0 0
1 1 1 0
0 1 0 0
```

The perimeter is calculated as follows:
- The land cells (`1`s) are surrounded by water (`0`s) or are at the edge of the grid. Each exposed edge of the land cells is counted towards the perimeter.
- The total perimeter for this island is 8.

### Edge Cases
- **Empty grid**: If the grid is empty (`[]`), the perimeter is 0.
- **Grid with no land**: If the grid contains only water cells (`0`s), the perimeter is 0.
- **Grid with all land**: If the grid contains only land cells (`1`s), the perimeter is calculated based on the grid's boundary.

## Conclusion
This function is designed to efficiently calculate the perimeter of an island represented in a 2D grid, with a time complexity of O(m * n), making it well-suited for larger grids. The approach is straightforward, involving basic grid traversal and checking neighboring cells to determine the exposed perimeter.