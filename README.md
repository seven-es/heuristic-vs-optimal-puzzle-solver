# 🧩 NxN Sliding Puzzle Solver (Micro-Hillary vs. A*)

This project implements a solver for the classic **NxN sliding tile puzzle** (e.g., 8-puzzle), where the goal is to arrange tiles into the correct order by sliding them into the blank space.

It compares two solving strategies:
- 🧠 A\* Search (Optimal)
- 🔀 Micro-Hillary Algorithm (Heuristic-based with macros)

---

## ✅ Objectives

- Solve the NxN puzzle using:
  1. **A\*** Search with Manhattan distance heuristic
  2. **Micro-Hillary** algorithm using a custom heuristic and move macros

- Evaluate both methods by:
  - Number of steps taken
  - Time required
  - Whether the final state matches the goal

---

## 🧠 Micro-Hillary Algorithm

A heuristic-driven greedy search that:
- Identifies the next tile out of place
- Tries basic moves first (up, down, left, right)
- Falls back on predefined macros (multi-step sequences) if no improving move is found
- Heuristic is a combination of:
  - Number of correctly placed tiles
  - Distance of blank tile to the misplaced tile
  - Distance of that tile to its goal

---

## 🔍 A* Search (Baseline)

- Standard A* implementation
- Uses Manhattan distance heuristic
- Always finds the shortest solution path
- Used to benchmark against Micro-Hillary

---

## 📦 Features

- Supports any NxN puzzle (default is 3x3)
- Solvability check using inversion count
- Times each algorithm's performance
- Uses macros derived from common move patterns
- Side-by-side comparison of optimal vs. heuristic solutions

---

## 🧪 Test Cases

Predefined test cases for evaluation:

```python
test1 = [1, 2, 3,
         4, 5, 6,
         7, 0, 8]  # Nearly solved

test2 = [1, 8, 2,
         0, 4, 3,
         7, 6, 5]  # Medium difficulty

test3 = [2, 5, 3,
         1, 6, 8,
         7, 0, 4]  # Challenging case

test4 = [4, 1, 3,
         7, 2, 5,
         0, 8, 6]  # Demonstration test
