
# Algorithm Design Solutions

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![NumPy](https://img.shields.io/badge/numpy-1.24+-013243.svg)
![CVXPY](https://img.shields.io/badge/cvxpy-1.3+-green.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Data%20Viz-orange.svg)

**Algorithm Design Solutions** is a repository containing efficient Python implementations of various algorithmic problems. Developed as part of a Design of Algorithms (DA) course curriculum, this project covers a wide range of topics from classical geometry problems to modern optimization techniques using Support Vector Machines (SVM).

## Description

This repository houses solutions to specific algorithmic challenges, demonstrating the practical application of theoretical concepts. It includes custom implementations of graph traversal algorithms, geometric divide-and-conquer strategies, and mathematical optimization using industry-standard libraries like `cvxpy`.

## Features

* **Closest Pair of Points (Divide & Conquer):** An $O(n \log n)$ implementation to find the closest pair of points in a 2D plane (`HW1.py`).
* **Graph Shortest Paths (Dijkstra):** Custom implementation of Dijkstra's algorithm using a priority queue to solve shortest path problems in weighted graphs (`HW2.py`).
* **Parenthesis Balancing:** A stack-based algorithm to analyze and correct bracket sequences (`HW3.py`).
* **Graph Reconstruction:** Logic to validate a distance matrix and reconstruct the underlying graph edges based on all-pairs shortest path properties (`HW4.py`).
* **Linear Classification (SVM):** A Support Vector Machine implementation using `cvxpy` to separate data points (white vs. black) with a margin maximization objective (`HW5.py`).

## Installation

To run these scripts, you need Python installed along with specific scientific computing libraries.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/nikelroid/algorithm-design-solutions.git](https://github.com/nikelroid/algorithm-design-solutions.git)
    cd algorithm-design-solutions
    ```

2.  **Install Dependencies:**
    The projects rely on standard libraries and external packages for optimization and plotting.
    ```bash
    pip install numpy cvxpy matplotlib
    ```

## Usage

Each file is a standalone script designed to solve a specific problem. You can run them directly via the command line. Input formats generally follow standard competitive programming styles (reading from `stdin`).

**Example: Running the SVM Optimization**
```bash
python HW5.py
# Input:
# 2 2       (Number of white and black points)
# 1.0 2.0   (White Point 1)
# 2.0 3.0   (White Point 2)
# 5.0 5.0   (Black Point 1)
# 6.0 1.0   (Black Point 2)
````

**Example: Closest Pair of Points**

```bash
python HW1.py
# Input:
# 3         (Number of points)
# 1 1
# 10 10
# 1 2
```

## Contributing

Contributions to optimize the algorithms or add new solutions are welcome.

1.  Fork the repository.
2.  Create your feature branch (`git checkout -b feature/Optimization`).
3.  Commit your changes.
4.  Push to the branch and open a Pull Request.

## License

Distributed under the MIT License.

## Contact

**Nima Kelidari**
Project Link: [https://github.com/nikelroid/algorithm-design-solutions](https://www.google.com/search?q=https://github.com/nikelroid/algorithm-design-solutions)

```
```
