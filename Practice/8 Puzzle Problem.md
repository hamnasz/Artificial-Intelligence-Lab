---

# 8-Puzzle Solver and Visualizer

This project solves and visualizes the **8-puzzle problem** step by step using the **A* algorithm**. The 8-puzzle problem consists of a 3x3 grid with 8 numbered tiles and one empty space. The goal is to slide the tiles to reach the correct configuration, where tiles are ordered from 1 to 8, with the empty space at the bottom-right corner.

## Features
- **Random Puzzle Generation**: The program generates a random but solvable puzzle configuration.
- **Puzzle Solver**: The A* algorithm is used to find the optimal solution for the puzzle.
- **Visualization**: Each step of the solution is visualized using Matplotlib, showing how the puzzle configuration changes until the goal state is reached.

## Dependencies
- **Python 3.x**
- **Matplotlib**: For visualizing the puzzle at each step.
- **Numpy**: For matrix-like handling of the puzzle grid.

To install the required libraries, use:

```bash
pip install matplotlib numpy
```

## Code Overview

### 1. `draw_puzzle(puzzle, step)`
This function visualizes the current state of the puzzle using `Matplotlib`. It displays a 3x3 grid with the tile numbers. The empty space is represented by `0`. The `step` parameter is used to label each step of the solution.

### 2. `is_solvable(puzzle)`
The 8-puzzle problem is only solvable if the number of **inversions** (pairs of tiles that are out of order) is even. This function checks whether a given puzzle configuration is solvable by counting the inversions.

### 3. `a_star(initial_state)`
This function implements the **A* algorithm** to find the optimal solution to the 8-puzzle problem. It uses the **Manhattan distance** heuristic to estimate the cost from the current state to the goal state. The function returns the sequence of states from the initial configuration to the solution.

### 4. `neighbors(state)`
This helper function generates all possible valid moves (up, down, left, right) from the current state of the puzzle by swapping the empty space (`0`) with its adjacent tiles.

### 5. `random_puzzle()`
This function randomly shuffles the puzzle until it generates a solvable configuration, ensuring that the puzzle can be solved using the A* algorithm.

### 6. `main logic`
- The initial puzzle is generated using `random_puzzle()`.
- The initial state of the puzzle is visualized using `draw_puzzle()`.
- The solution path is computed by `a_star()` and then visualized step by step, showing how the puzzle transitions from the initial state to the solved state.

## How to Run

1. Clone or download the project.

2. Make sure all dependencies are installed:
   ```bash
   pip install matplotlib numpy
   ```

3. Run the Python script:

   ```bash
   python 8_puzzle_solver.py
   ```

4. The program will:
   - Generate a random 8-puzzle configuration.
   - Solve it using the A* algorithm.
   - Visualize each step of the puzzle until the solution is reached.

## Example

Here's an example of a random puzzle and its step-by-step solution:

1. **Initial Puzzle**:

```
5  2  3
1  0  6
4  7  8
```

2. **Intermediate Steps**:
   - After a few moves, the puzzle might look like:

```
1  2  3
5  7  6
4  0  8
```

3. **Solved Puzzle**:

```
1  2  3
4  5  6
7  8  0
```

The program will display each step until it reaches the goal configuration.

## Notes
- The puzzle is guaranteed to be solvable due to the `is_solvable()` function.
- The A* algorithm ensures an optimal solution (i.e., the shortest sequence of moves).

---
