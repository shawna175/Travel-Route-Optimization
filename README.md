# Travel Route Optimization

A C-based algorithm implementation project that explores travel-route selection under a budget constraint and compares the execution time of different algorithms.

## Overview

The program generates a set of sample travel routes between predefined cities. Each route is assigned a distance and a cost. Given a travel budget, the program applies algorithmic techniques to process and evaluate the generated routes.

The project demonstrates three algorithms:

- **Merge Sort** — sorts routes by distance in ascending order.
- **0/1 Knapsack (Dynamic Programming)** — selects a subset of routes to maximize the total distance without exceeding the budget.
- **Coin Change (Dynamic Programming)** — computes the minimum number of route-cost values needed to make the specified budget exactly, when an exact combination is possible.

The program also measures the execution time of the algorithms and writes route-selection results and timing information to output files.

## Features

- Generates random routes between predefined city names.
- Assigns each generated route a distance and a cost.
- Sorts routes by distance using Merge Sort.
- Uses dynamic programming for budget-based route selection.
- Measures algorithm execution time.
- Saves generated input, selected-route output, and timing results in text files.

## Algorithms and Complexity

| Algorithm | Purpose | Time Complexity |
|---|---|---|
| Merge Sort | Sort routes by distance | `O(n log n)` |
| 0/1 Knapsack (DP) | Maximize total distance within the budget | `O(n × budget)` |
| Coin Change (DP) | Minimize the number of route-cost values for an exact budget | `O(n × budget)` |

Here, `n` is the number of generated routes. The dynamic-programming running times also depend on the numeric budget.

## How It Works

1. The user enters the number of routes to generate and a positive travel budget.
2. The program generates route records with source, destination, distance, and cost values and writes them to `input.txt`.
3. It reads the generated data and sorts the routes by distance.
4. It runs the Knapsack and Coin Change procedures using the entered budget.
5. It writes selected-route information to `output.txt` and execution-time measurements to `time_results.txt`.

**Note:** The routes are generated independently as sample records. The program does not compute a connected path through a real map or verify that consecutive routes form a continuous journey.

## Requirements

- A C compiler such as GCC.
- A POSIX-compatible environment for the high-resolution timing function used in the source code.

## Build and Run

Compile the source file:

```bash
gcc travel_route_optimization.c -o travel_route_optimization
```

Run the program:

```bash
./travel_route_optimization
```

Follow the prompts to enter the number of routes and the budget.

## Generated Files

The program creates the following files in its working directory:

- `input.txt` — the budget and generated route records.
- `output.txt` — route-selection output for the Knapsack and Coin Change procedures.
- `time_results.txt` — measured execution times for the algorithms.

These files are generated when the program runs; they do not need to be present in the repository beforehand.

## Repository Structure

```text
Travel-Route-Optimization/
├── README.md
├── src/
│   └── travel_route_optimization.c
└── docs/
    └── Project_Report.pdf
```

## Academic Context

- **Course:** CSE246 — Algorithms
- **Project:** Algorithm Implementation for Travel Route Optimization
- **Language:** C

## Authors

- Shawna Akter
- Tabassum Nahar Yeah
