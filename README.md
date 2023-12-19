# Numerical Computation Coursework: Solving Predator-Prey Models

This repository contains a solution to the final coursework for the **Numerical Computation** module (COMP/XJCO2421). The project explores and analyzes various numerical methods for solving the differential equations that describe predator-prey models.

---

## Problem Description

The core of this project is the predator-prey model, which is defined by the following system of differential equations:

\[
\frac{dx}{dt} = \alpha x - \beta xy + f(t)
\]
\[
\frac{dy}{dt} = \delta xy - \gamma y + g(t)
\]

Where:
- \( x(t) \): prey population  
- \( y(t) \): predator population  
- \( \alpha, \beta, \gamma, \delta \): positive real parameters  
- \( f(t), g(t) \): external migration functions  

The analysis is based on two test cases:
1. A case with a known exact solution, used to evaluate the accuracy of the numerical methods.
2. A case without a known exact solution, where the consistency of the population maxima over time is used as a measure of stability and accuracy.

---

## Numerical Methods Analyzed

This project implements and compares the following numerical methods:

- **Euler's Method**: A first-order numerical procedure for solving ODEs with a given initial value.
- **Heun's Method**: An improved version of Euler's method (second-order Runge-Kutta method).
- **SSPRK3**: A third-order Strong Stability Preserving Runge-Kutta method, known for its enhanced stability.

---

## Implementation

The solution is implemented in a **Jupyter Notebook** (`template.ipynb`). The core logic for the numerical solvers is contained in the `solvers.py` file. The implementation allows for the simulation of the predator-prey models with arbitrary initial conditions, time steps, and model parameters.

### Python Libraries Used

- `numpy` – for numerical operations  
- `matplotlib` – for plotting results  
- `pandas` – for data manipulation and table creation  
- `tabulate` – for formatting tables  
- `scipy` – for identifying local maxima

---

## Results and Analysis

### Accuracy

- For the test case with a known solution: the **absolute error** of each method was computed and compared.
- For the second case (no known solution): the **consistency of the maxima** in predator and prey populations was evaluated.

### Efficiency

- The **execution time** of each method was measured across various time steps to assess computational efficiency.

---

## Conclusion

- **Heun's method** is recommended as the most suitable solver for this predator-prey model.
- While **SSPRK3** occasionally showed slightly better accuracy, Heun's method offers a better **balance of accuracy, stability, and efficiency**.
- **Euler's method** is the least accurate, particularly with larger time steps.

---

## How to Run the Code

To run this project, you will need Python and the libraries listed above.

1. Clone the repository.
2. Ensure `solvers.py` is in the same directory as the Jupyter Notebook.
3. Open and run `solution.ipynb` in a Jupyter environment.

---
