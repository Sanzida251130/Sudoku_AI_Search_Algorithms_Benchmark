# Sudoku Solver Benchmarking & Comparison

This project implements, benchmarks, and compares three distinct artificial intelligence search algorithms on the **Rohan Rao Sudoku dataset** (sourced from Kaggle):
1. **Backtracking** (Complete / Optimized Search)
2. **A* Search** (Heuristic-based Complete Search)
3. **Hill Climbing with Restarts** (Incomplete Local Search)

---

## 🚀 Algorithms Overview

* **Backtracking**: A systematic depth-first search approach that recursively fills empty cells and backtracks upon hitting constraint violations. It guarantees completeness.
* **A* Search**: Uses a priority queue based on cost and a heuristic function (counting remaining empty cells) to guide the search toward optimal state expansion.
* **Hill Climbing**: An iterative local search algorithm initialized via box-filling strategies, utilizing conflict minimization and random restarts to escape plateaus and local minima.

---

## 📊 Benchmark Results Summary

Tested on subsets of the Rohan Rao Sudoku dataset, the algorithms yielded the following comparative performance metrics:

| Algorithm | Success Rate | Average Time (s) | Average Node Expansions |
| :--- | :---: | :---: | :---: |
| **A* Search** | 100% | 0.0050s | 177.8 |
| **Backtracking** | 100% | 0.0023s | 140.0 |
| **Hill Climbing** | 100% | 0.0444s | 3,179.4 |

> **Key Takeaway**: Complete algorithms (**Backtracking** and **A***) achieve fast execution times with minimal node expansions. **Hill Climbing** successfully converges via restarts, demonstrating the classic trade-offs of incomplete local search methods on tightly constrained constraint-satisfaction problems (CSPs).

---

## 🔒 Secure Configuration (Kaggle API)

To protect credentials during GitHub synchronization, this notebook utilizes **Google Colab's Secrets Manager** rather than hardcoding API tokens. 

If you want to run this notebook locally or in your own Colab environment:
1. Generate an API token from your [Kaggle Account Settings](https://www.kaggle.com/).
2. In Google Colab, open the **Secrets (Key icon)** tab on the left sidebar.
3. Create a secret named **`KAGGLE_TOKEN`** and paste your token value.
4. Ensure **Notebook access** is toggled **ON**.

---

## 🛠️ How to Run
1. Open the `.ipynb` file in **Google Colab**.
2. Configure your Kaggle secret as outlined above.
3. Click **Runtime > Run all** to execute the pipeline, dataset download, solver implementations, and benchmarking loop.
