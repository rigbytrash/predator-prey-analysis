# Numerical Computation Coursework: Solving Predator-Prey Models

This repository contains a solution to the final coursework for the **Numerical Computation** module (COMP/XJCO2421). The project explores and analyzes various numerical methods for solving the differential equations that describe predator-prey models.

---

## Problem Description

The core of this project is the predator-prey model, defined by the following system of differential equations:

<img width="217" height="135" alt="image" src="https://github.com/user-attachments/assets/afe8f1aa-7aed-4b50-b1b7-e72d3bff14d0" />



Where:
- `x(t)`: prey population  
- `y(t)`: predator population  
- `α`, `β`, `γ`, `δ`: positive real parameters  
- `f(t)`, `g(t)`: external migration functions  

The analysis is based on two test cases:
1. A case with a known exact solution, used to evaluate the accuracy of the numerical methods.
2. A case without a known exact solution, where the consistency of the population maxima over time is used as a measure of stability and accuracy.

---

## Numerical Methods Analyzed

This project implements and compares the following numerical methods:

- **Euler's Method** – A first-order numerical procedure for solving ODEs with a given initial value.
- **Heun's Method** – An improved version of Euler's method (a second-order Runge-Kutta method).
- **SSPRK3** – A third-order Strong Stability Preserving Runge-Kutta method, known for its enhanced stability.

---

## Implementation

The solution is implemented in a **Jupyter Notebook** (`template.ipynb`). The core logic for the numerical solvers is contained in the `solvers.py` file. The implementation allows for the simulation of the predator-prey models with arbitrary initial conditions, time steps, and model parameters.

### Python Libraries Used

- `numpy` – numerical operations  
- `matplotlib` – plotting results  
- `pandas` – data manipulation and table creation  
- `tabulate` – formatting tables  
- `scipy` – identifying local maxima

---

## Results and Analysis

### Accuracy

- **Test Case 1 (known solution)** – Absolute error of each method was computed and compared.
- **Test Case 2 (unknown solution)** – Consistency of the population maxima was evaluated as a proxy for accuracy and stability.

### Efficiency

- Execution time of each method was measured for various time steps to evaluate computational cost.

---

## Conclusion

- **Heun's method** is the most balanced in terms of accuracy, stability, and efficiency.
- **SSPRK3** offered slightly better accuracy in some scenarios but at a higher computational cost.
- **Euler's method** was significantly less accurate, especially for larger time steps.

---

## How to Run the Code

1. Clone the repository.
2. Ensure `solvers.py` is in the same directory as `template.ipynb`.
3. Open and run `template.ipynb` in a Jupyter Notebook environment with the required Python libraries.

---
