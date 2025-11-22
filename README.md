
# Algorithm Design Solutions

![Python](https://img.shields.io/badge/python-3.8%2B-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-1.24%2B-013243?logo=numpy&logoColor=white)
![CVXPY](https://img.shields.io/badge/cvxpy-1.3%2B-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Data_Viz-orange?logo=matplotlib&logoColor=white)

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

# Complete Question Description and Tests


### 1. Hogwarts 3 

**Use Case:**
Harry needs to travel from a starting room (node $s$) to the exit (node $t$) in a graph representing the dormitory. The graph has $n$ rooms and $m$ weighted edges (hallways). There are $k$ guards stationed at specific nodes. Guards move randomly along edges. Moving across an edge takes $w$ time for both Harry and the guards. Harry wants to find a path to $t$ such that he is **never** in the same location (node or edge) as a guard at the same time, regardless of how the guards move. You need to determine the shortest time to reach $t$ safely, or output "impossible".

**Test Cases:**

  * **Test Case 1:**

      * **Input:**
        ```text
        5 8 1 3 2
        1 5 1
        1 4 1
        5 3 6
        4 3 7
        1 2 2
        2 5 5
        2 3 3
        4 2 5
        4 5
        ```
      * **Output:**
        ```text
        4
        ```

  * **Test Case 2:**

      * **Input:**
        ```text
        4 5 1 3 1
        1 2 5
        2 3 5
        1 4 1
        2 4 6
        4 3 10
        4
        ```
      * **Output:**
        ```text
        impossible
        ```

-----

### 2. Grumpy Pine

**Use Case:**
Professor Sprout presents a tree structure with $n$ vertices. Some vertices contain a "pine cone" (indicated by 1), and others do not (indicated by 0). To "kill" the tree safely, you must cut edges such that every resulting connected component contains **exactly one** pine cone. You need to calculate the number of valid ways to cut the edges to achieve this, modulo $10^9 + 7$.

**Test Cases:**

  * **Test Case 1:**

      * **Input:**
        ```text
        3
        0 0
        0 1 1
        ```
      * **Output:**
        ```text
        2
        ```

  * **Test Case 2:**

      * **Input:**
        ```text
        10
        0 1 2 1 4 4 4 0 8
        0 0 0 1 0 1 1 0 0 1
        ```
      * **Output:**
        ```text
        27
        ```

-----

### 3. Chess Revenge

**Use Case:**
You are given an $n \times n$ chessboard and $n$ rooks. For each rook $i$, there is a specific rectangular region defined by top-left $(a_i, b_i)$ and bottom-right $(c_i, d_i)$ within which it must be placed. You must place all $n$ rooks such that no two rooks attack each other (i.e., no two rooks share the same row or column) and every rook is inside its assigned rectangle. Output the coordinates for each rook or "impossible".

**Test Cases:**

  * **Test Case 1:**

      * **Input:**
        ```text
        4
        1 1 1 1
        1 3 2 4
        3 1 4 2
        2 2 4 4
        ```
      * **Output:**
        ```text
        1 1
        2 3
        3 2
        4 4
        ```

  * **Test Case 2:**

      * **Input:**
        ```text
        2
        1 1 1 1
        1 1 2 1
        ```
      * **Output:**
        ```text
        impossible
        ```

-----

### 4. Behind Hogwarts

**Use Case:**
Professor Umbridge wants to close as many hallways (edges) as possible in the Hogwarts graph while keeping the graph connected and minimizing the total length of the remaining edges (essentially finding a Minimum Spanning Tree - MST). Students have "hangout" spots, which are sets of specific edges. For each student, you need to determine if there exists *some* valid MST that includes *all* of their specific hangout edges. Output "YES" or "NO" for each student.

**Test Cases:**

  * **Test Case 1:**
      * **Input:**
        ```text
        5 7
        1 2 2
        1 3 2
        2 3 1
        2 4 1
        3 4 1
        3 5 2
        4 5 2
        4
        2 3 4
        3 3 4 5
        2 1 7
        2 1 2
        ```
      * **Output:**
        ```text
        YES
        NO
        YES
        NO
        ```

-----

### 5. Potion Duel

**Use Case:**
Professor Snape has two sequences of potions with specific power levels: sequence $A$ (Gryffindor) and sequence $B$ (Slytherin). He wants to select a subsequence of potions from each group such that the two subsequences are identical in power values and strictly increasing. You need to find the length of the **Longest Common Increasing Subsequence (LCIS)** between the two arrays.

**Test Cases:**

  * **Test Case 1:**

      * **Input:**
        ```text
        7
        2 3 1 6 5 4 6
        4
        1 3 5 6
        ```
      * **Output:**
        ```text
        3
        ```

  * **Test Case 2:**

      * **Input:**
        ```text
        5
        1 2 0 2 1
        3
        1 0 1
        ```
      * **Output:**
        ```text
        2
        ```

-----

### 6. Spell Casting Tournament

**Use Case:**
There are $n$ students divided into $m$ groups. Each student $i$ has a spell specialty $p_i$. A "worthy team" consists of exactly one member from every group that has at least one remaining student. The "diversity score" (MEX) of a team is the smallest non-negative integer *not* present in the set of their specialties. Every day, one specific student is removed from the competition. You must calculate the maximum possible diversity score of a worthy team after each removal.

**Test Cases:**

  * **Test Case 1:**

      * **Input:**
        ```text
        5 3
        0 1 2 2 0
        1 2 2 3 2
        5
        3
        2
        4
        5
        1
        ```
      * **Output:**
        ```text
        3
        1
        1
        1
        0
        ```

  * **Test Case 2:**

      * **Input:**
        ```text
        5 3
        0 1 2 2 1
        1 3 2 3 2
        5
        4
        2
        3
        5
        1
        ```
      * **Output:**
        ```text
        3
        2
        2
        1
        0
        ```

-----

### 7. Unicorn Hunting (Challenge Question, does not exist in answers)

**Use Case:**
The Forbidden Forest is represented as a tree with $n$ regions (nodes). A unicorn is hiding in one region. Harry can query a region: Hagrid will say "Yes" if the unicorn is there, or point to the adjacent edge that leads toward the unicorn. Each query costs 1 Galleon. Harry wants to find the strategy that minimizes the *worst-case* cost to find the unicorn. You need to output this minimum cost. This is effectively finding the height of the optimal centroid decomposition or separator tree.

**Test Cases:**

  * **Test Case 1:**

      * **Input:**
        ```text
        5
        1 2
        2 3
        4 3
        5 3
        ```
      * **Output:**
        ```text
        2
        ```

  * **Test Case 2:**

      * **Input:**
        ```text
        6
        1 2
        2 3
        3 4
        4 5
        5 6
        ```
      * **Output:**
        ```text
        2
        ```
