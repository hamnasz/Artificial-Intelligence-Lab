
# 8-Puzzle Problem Visualizer

This Python project visualizes the step-by-step solution of a randomly shuffled 8-puzzle problem using the A* search algorithm.

## Overview

The 8-puzzle is a sliding puzzle consisting of a 3x3 grid with eight numbered tiles and one empty space. The goal is to move the tiles until they are arranged in numerical order (1-8) with the empty space in the bottom-right corner.

This project implements a solution using the **A* search algorithm** and visualizes each step of the solution process.

### Example of the puzzle:

```
1  2  3
4  5  6
7  8  0
```

Where `0` represents the empty space.

## Features

- **Random Puzzle Generator**: The program randomly shuffles the puzzle into a solvable configuration.
- **Step-by-Step Visualization**: Each step of the puzzle's solution is displayed visually, allowing the user to follow the movement of the tiles until the puzzle is solved.
- **A* Search Algorithm**: The code uses the A* search algorithm with the Manhattan distance heuristic to efficiently solve the puzzle.

## Prerequisites

Before running the code, make sure you have the following installed:

- Python 3.x
- Matplotlib (for visualization)

You can install the necessary dependencies using the following command:

```bash
pip install matplotlib
```

## Code Structure

The project consists of the following key functions:

### 1. `draw_puzzle(puzzle, step)`
This function visualizes the current state of the puzzle as a 3x3 grid using Matplotlib. It takes the puzzle's current configuration and the step number as inputs and displays the puzzle at each step.

### 2. `is_solvable(puzzle)`
This function checks if the given 8-puzzle configuration is solvable. A puzzle is solvable if the number of **inversions** (pairs of tiles in the wrong order) is even.

### 3. `a_star(initial_state)`
This function solves the puzzle using the A* search algorithm. It uses the Manhattan distance as the heuristic to estimate how far each state is from the goal. The algorithm explores the puzzle states and finds the shortest path to the goal configuration.

### 4. `random_puzzle()`
This function generates a random solvable puzzle by shuffling the tiles and verifying if the resulting configuration is solvable.

## How It Works

1. The program starts by generating a random puzzle configuration.
2. It then visualizes the initial state of the puzzle.
3. Using the A* algorithm, it computes the solution, moving the empty space up, down, left, or right as needed.
4. After each move, the new state of the puzzle is visualized.
5. The process continues until the puzzle reaches the goal state.

### Puzzle Visualization

Each puzzle state is visualized in the terminal using a 3x3 grid. For example, after the initial puzzle is generated, the grid will be displayed, showing the number tiles in their current positions.

## Running the Code

1. Clone the repository or download the code.
2. Install the required dependencies (`matplotlib`).
3. Run the Python script:

```bash
python 8_puzzle_visualizer.py
```
