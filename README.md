# Stellar Luminosity Modeling  
## Linear and Polynomial Regression from First Principles
- Student: Juan Jose Mejia Celis
- Class: AREP

This laboratory explores the implementation of linear and polynomial regression
models **from first principles**, without using any high-level machine learning
libraries. The goal is to model stellar luminosity based on stellar mass and
temperature, using simplified main-sequence stellar behavior.

The lab covers model construction, loss functions, gradient optimization,
feature engineering, and cloud execution using AWS SageMaker.

---

## Laboratory Overview

Astronomy uses data to find relationships between physical quantities from
observations. In this lab, regression models are built to explore how stellar
luminosity relates to stellar mass and temperature.

Two models are developed:

- A **linear regression model** using stellar mass as a single feature
- A **polynomial regression model with interaction terms** using both mass and
  temperature

All models are implemented by defining:
- Hypothesis functions
- Loss functions (Mean Squared Error)
- Analytical gradients
- Gradient descent optimization

---

## Repository Structure
- /
- ├── README.md
- ├── 01_part1_linreg_1feature.ipynb
- └── 02_part2_polyreg.ipynb

---

## Notebook Summaries

### 1. Linear Regression with One Feature  
**File:** `01_part1_linreg_1feature.ipynb`

This notebook models stellar luminosity as a linear function of stellar mass:

\[
\hat{L} = wM + b
\]

Key components:
- Visualization of the mass–luminosity dataset and linearity discussion
- Implementation of the hypothesis function and MSE loss
- Visualization of the cost function surface \(J(w, b)\)
- Derivation and implementation of gradients
- Gradient descent using loop-based and vectorized methods
- Convergence analysis for different learning rates
- Final model fit and systematic error discussion

This notebook shows the limitations of linear models when applied to nonlinear
physical phenomena.

---

### 2. Polynomial Regression with Interaction Terms  
**File:** `02_part2_polyreg.ipynb`

This notebook extends the linear model by adding polynomial and interaction
features to capture nonlinear effects:

\[
X = [M,\ T,\ M^2,\ M \cdot T]
\]

Key components:
- Multifeature dataset visualization with temperature encoding
- Polynomial feature engineering using NumPy
- Vectorized loss and gradient computation
- Gradient descent optimization
- Feature selection experiment comparing three models
- Sensitivity analysis of the interaction term
- Inference on new stellar observations

This notebook shows how feature engineering improves model expressiveness and
predictive accuracy.

---

## AWS SageMaker Execution Evidence

All notebooks were uploaded and executed successfully in an **AWS SageMaker Studio**
environment using the integrated **Visual Studio Code interface**.

### SageMaker Environment Overview

<img width="1318" height="683" alt="image" src="https://github.com/user-attachments/assets/e8af5be9-bd95-48df-a20f-08a0beb4b25b" />

## Execution Evidence: Notebook 1
# Linear Regression with One Feature

<img width="1309" height="672" alt="image" src="https://github.com/user-attachments/assets/00c15275-1456-4c11-9851-83d65839e6f2" />
<img width="1316" height="677" alt="image" src="https://github.com/user-attachments/assets/638feb04-bbee-4ba4-9dba-c9c54fae9a39" />

## Execution Evidence: Notebook 2
# Polynomial Regression with Interaction Terms

<img width="1311" height="677" alt="image" src="https://github.com/user-attachments/assets/52ee44f8-a521-4000-9dad-a2ebef865209" />
<img width="1315" height="675" alt="image" src="https://github.com/user-attachments/assets/d3aa1fdf-c675-44db-9936-ef4c4bf1ce98" />

## Local vs AWS SageMaker Execution Comparison

The notebooks were executed both locally and in AWS SageMaker. Results,
convergence behavior, and visualizations were consistent across environments.

## Key observations:

- Same loss convergence patterns
- Same learned parameters
- No numerical instability
- SageMaker provides a controlled and scalable execution environment

This confirms the implementation is portable and cloud-ready.

## Conclusion

This lab shows how regression models can be built from first principles to
model physical phenomena like stellar luminosity. Starting from a simple linear
model and moving to polynomial regression with interaction terms demonstrates
the importance of model expressiveness and feature engineering.

Executing the models in AWS SageMaker shows the role of cloud platforms as
infrastructure for modern data-driven systems. The lab integrates theoretical
understanding, practical implementation, and cloud execution into a complete
workflow.







