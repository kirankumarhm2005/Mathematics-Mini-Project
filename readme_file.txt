# 🚗 Matrix-Optimized Smart Parking Grid

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![NumPy](https://img.shields.io/badge/NumPy-Linear%20Algebra-green.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange.svg)

## 📌 Project Overview
The **Matrix-Optimized Smart Parking Grid** is a Python-based spatial allocation engine that models physical parking infrastructure as a mathematical vector space. 

Instead of relying on random array looping, this system uses strict linear algebra concepts—specifically **Vector Norms ($\ell_1$ Manhattan Distance)** and **Scalar Capacity Arithmetic**—to instantly calculate the optimal parking slot for incoming vehicles based on vehicle type and driving distance.

## 🧮 Mathematical Foundations (MFAD Integration)
This project was built applying core concepts from Mathematical Foundations for AI & Data Science:

* **Vector Spaces & Matrices (Unit 1):** The physical parking lot is mapped into $4 \times 4$ matrices representing slot types and occupancy states.
* **Scalar Capacity Arithmetic (Unit 1):** Matrix indices are managed using scalar fractions. Cars occupy a full integer (`1.0`), while 2-wheelers occupy a fraction (`0.5`). This allows a single vector space index to dynamically hold two distinct vehicles (horizontally split).
* **Vector Norms / Manhattan Distance (Unit 2):** To simulate real-world driving along perpendicular road aisles, the distance from the entrance to the parking slot is calculated using the **$\ell_1$ Vector Norm** rather than the standard $\ell_2$ Euclidean distance.
* **Linear Combinations:** The allocation algorithm optimizes placement by evaluating a linear combination of normalized driving distance and vehicle compatibility criteria.

## ✨ Key Features
- **Dynamic Slot Allocation:** Supports Normal Cars, EVs, Accessible/Handicap vehicles, and 2-Wheelers.
- **$\ell_1$ Norm Pathfinding:** Calculates actual driveway distances rather than "as the crow flies."
- **Horizontal Matrix Splitting:** Visually and mathematically splits a single parking bay to accommodate two bikes side-by-side.
- **Live GUI Visualization:** Uses `matplotlib.patches` to render a top-down view of the parking lot, complete with asphalt roads, yellow dashed lines, and dynamic green pathfinding routes.

## 🛠️ Prerequisites & Installation

To run this project, you need Python installed on your system along with the `numpy` and `matplotlib` libraries.
