# Algorithmic Problem Solving & Optimization

![Python](https://img.shields.io/badge/python-3.8%2B-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-1.24%2B-013243?logo=numpy&logoColor=white)
![CVXPY](https://img.shields.io/badge/cvxpy-1.3%2B-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Data_Viz-orange?logo=matplotlib&logoColor=white)


## Description
This repository contains a suite of Python solutions for classical and advanced problems in Algorithm Design. It explores efficient approaches to solving geometric problems, graph analysis, and mathematical optimization. The projects range from implementing a divide-and-conquer strategy for finding the closest pair of points to using convex optimization libraries for linear classification.

The code is structured as individual homework assignments (`HW1` through `HW5`), each targeting a specific algorithmic concept.

## Features

This repository includes solutions for the following 5 algorithmic challenges:

### 1. Closest Pair of Points (Divide & Conquer)
* **File:** `HW1.py`
* **Story:** In a vast 2D plane of stars, an astronomer needs to identify the two stars that are closest to each other to study their gravitational interaction.
* **Use Case:** Given $N$ coordinates on a 2D plane, efficiently find the minimum Euclidean distance between any two points. This implementation uses a **Divide and Conquer** approach to achieve better performance than the naive $O(N^2)$ method.
* **Test Case:**
    * *Input:*
        ```text
        5
        1 4
        2 6
        5 6
        4 2
        7 3
        ```
    * *Output:*
        ```text
        4 2 7 3
        ```
        *(Coordinates of the closest pair).*

### 2. Network Radius & Farthest Nodes (Graph Algorithms)
* **File:** `HW2.py`
* **Story:** A logistics company wants to place a distribution center at a specific node. They need to know the "worst-case" delivery time (distance to the farthest node) and how many cities are at that maximum distance.
* **Use Case:** Given a weighted graph and a set of start nodes (queries), run **Dijkstra's Algorithm** to find the shortest paths to all other nodes. Then, identify the maximum finite distance from the start node and count how many nodes share that maximum distance.
* **Test Case:**
    * *Input:*
        ```text
        4 4 1
        1 2 2
        2 3 1
        1 3 5
        3 4 1
        1
        ```
        *(4 nodes, 4 edges, 1 query. Edges: 1-2 (w=2), 2-3 (w=1), etc. Query start: 1)*
    * *Output:*
        ```text
        (1, 4, 1)
        ```
        *(From node 1, max distance is 4 (to node 4), and 1 node is at that distance).*

### 3. Parenthesis Balancing Cost (Greedy/Stack)
* **File:** `HW3.py`
* **Story:** A programmer has a corrupted code file with unbalanced parentheses. They need to calculate the "cost" (or number of swap operations) required to reorder the brackets into a valid configuration.
* **Use Case:** Analyze a string of parentheses `(` and `)`. The algorithm calculates a displacement metric, likely representing the minimum distance swaps needed to match open parentheses with closing ones.
* **Test Case:**
    * *Input:*
        ```text
        ))((
        ```
    * *Output:*
        ```text
        4
        ```

### 4. Matrix to Graph Reconstruction (Graph Theory)
* **File:** `HW4.py`
* **Story:** An archaeologist finds a distance table between ancient cities but the map of roads is lost. They need to determine if the table represents valid shortest paths and reconstruct the minimum road network (edges) that created it.
* **Use Case:** Given an $N \times N$ matrix representing All-Pairs Shortest Paths (APSP), verify if it forms a valid metric space (triangle inequality). If valid, reconstruct the underlying graph by identifying "direct" edges (edges that cannot be formed by a path through another node).
* **Test Case:**
    * *Input:*
        ```text
        3
        0 2 5
        2 0 3
        5 3 0
        ```
    * *Output:*
        ```text
        2
        ```
        *(Valid graph with 2 edges: 0-1 and 1-2. 0-2 is formed by 0-1-2).*

### 5. Linear Separator with SVM (Optimization)
* **File:** `HW5.py`
* **Story:** A biologist has data on two species of plants (White and Black) based on two characteristics. They need to find the widest possible linear path (margin) that separates these two species on a chart.
* **Use Case:** This script implements a **Support Vector Machine (SVM)** using `cvxpy`. It solves a convex optimization problem to find parameters $a, b$ for the line $y = ax + b$ that separates two classes of 2D points with the maximum vertical margin $t$. It also visualizes the result using Matplotlib.
* **Test Case:**
    * *Input:*
        ```text
        2 2
        1 1
        2 1
        1 3
        2 3
        ```
        *(2 white points at y=1, 2 black points at y=3)*
    * *Output:*
        ```text
        (0.0000, 2.0000)
        ```
        *(The separating line is horizontal at y=2).*

## Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/Algorithm-Design-Assignments.git](https://github.com/yourusername/Algorithm-Design-Assignments.git)
    cd Algorithm-Design-Assignments
    ```

2.  **Install dependencies:**
    The solutions rely on standard libraries and specific packages for optimization and plotting.
    ```bash
    pip install numpy matplotlib cvxpy
    ```

## Usage

You can run each script individually from the terminal. They accept input via standard input (stdin).

**Example: Running HW1 (Closest Pair)**
```bash
# Create input file
echo "5
1 4
2 6
5 6
4 2
7 3" > input.txt

# Run script
python HW1.py < input.txt
````

**Example: Running HW5 (SVM Visualization)**

```bash
python HW5.py
# Enter data manually or pipe from file.
# A plot window will appear showing the separation.
```

## Contributing

Contributions to optimize algorithms or add new test cases are welcome\!

1.  Fork the repository.
2.  Create a new branch (`git checkout -b optimize-dijkstra`).
3.  Commit your changes.
4.  Push to the branch and open a Pull Request.

## License

This project is open-source.

## Contact

  * **Maintainer:** [Your Name]

<!-- end list -->

```
```
