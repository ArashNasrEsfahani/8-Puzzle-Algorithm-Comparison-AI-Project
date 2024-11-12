# 8-Puzzle Algorithm Comparison Project

A comprehensive comparison of different search algorithms solving the classic 8-puzzle problem, analyzing their performance, optimality, and resource usage.

## 📝 Table of Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Problem Description](#problem-description)
- [Algorithms](#algorithms)
- [Usage](#usage)
- [Performance Analysis](#performance-analysis)
- [Project Structure](#project-structure)

## ✨ Features
- **Multiple Search Algorithms**: Implements BFS, DFS, IDS, UCS, and A* search
- **Performance Metrics**: Tracks execution time, memory usage, and solution path length
- **Memory Tracking**: Uses `tracemalloc` for accurate memory usage monitoring
- **Optimal Solutions**: Most algorithms find the shortest possible path to the goal
- **Visualization**: Clear output of moves and performance statistics

## ✅ Prerequisites
Before running the algorithms, ensure you have:
- Python 3.7+
  
## 🧩 Problem Description
The 8-puzzle consists of a 3×3 grid with eight numbered tiles and one blank space. The goal is to rearrange the tiles to match a target configuration by sliding tiles into the blank space.

Example:
```
Initial State    Goal State
-------------   -------------
| 0 1 2 |       | 1 2 3 |
| 4 5 3 |  →    | 4 5 6 |
| 7 8 6 |       | 7 8 0 |
-------------   -------------
```

## 🔍 Algorithms

### 1. Breadth-First Search (BFS)
- **Properties**: Complete, Optimal
- **Time Complexity**: O(b^d)
- **Space Complexity**: O(b^d)
- **Performance**: Moderate time and space usage
- **Solution Quality**: Always finds optimal solution

### 2. Depth-First Search (DFS)
- **Properties**: Complete with depth limit
- **Time Complexity**: O(b^m)
- **Space Complexity**: O(bm)
- **Performance**: High time complexity
- **Solution Quality**: Not guaranteed optimal

### 3. Iterative Deepening Search (IDS)
- **Properties**: Complete, Optimal
- **Time Complexity**: O(b^d)
- **Space Complexity**: O(bd)
- **Performance**: Best space efficiency
- **Solution Quality**: Finds optimal solution

### 4. Uniform Cost Search (UCS)
- **Properties**: Complete, Optimal
- **Time Complexity**: O(b^(C*/ε))
- **Space Complexity**: O(b^(C*/ε))
- **Performance**: Moderate overall
- **Solution Quality**: Guarantees optimal solution

### 5. A* Search
- **Properties**: Complete, Optimal
- **Time Complexity**: O(b^d)
- **Space Complexity**: O(b^d)
- **Performance**: Best time efficiency
- **Solution Quality**: Optimal with admissible heuristic

## 💡 Usage
```python
# Define initial and goal states
start = [0, 1, 2, 4, 5, 3, 7, 8, 6]
end = [1, 2, 3, 4, 5, 6, 7, 8, 0]

# Run desired algorithm
result = bfs_8puzzle(start, end)
# Or
result = astar_8puzzle(start, end)

# Get execution metrics
print('Solution:', result)
print('Execution time:', execution_time, 'seconds')
print('Memory usage:', memory_usage, 'MB')
```

## 📊 Performance Analysis

Algorithm | Time (s) | Memory (MB) | Path Length | Optimality
----------|----------|-------------|-------------|------------
BFS       | 0.002    | 0.02        | 4           | Optimal
DFS       | 0.001    | 0.02        | 10          | Not Optimal
IDS       | 0.000    | 0.01        | 4           | Optimal
UCS       | 0.000    | 0.02        | 4           | Optimal
A*        | 0.001    | 0.01        | 4           | Optimal

## 📁 Project Structure
```
/8-Puzzle-Algorithm-Comparison

├── Algorithms-Comparison.xlsx
├── Algorithms-Implementations.ipynb
└── README.md

