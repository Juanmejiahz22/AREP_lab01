# Stellar Luminosity Modeling  
## Linear and Polynomial Regression from First Principles
- Student: Juan Jose Mejia Celis
- Class: AREP

This laboratory explores the implementation of linear and polynomial regression
models **from first principles**, without using any high-level machine learning
libraries. The objective is to model stellar luminosity as a function of stellar
mass and temperature, inspired by simplified main-sequence stellar behavior.

The lab emphasizes not only model construction, but also the understanding of
loss functions, gradient-based optimization, feature engineering, and controlled
execution within a cloud environment using AWS SageMaker.

---

## Laboratory Overview

Astronomy is a data-driven science where empirical relationships between physical
quantities are inferred from observations. In this laboratory, regression models
are constructed explicitly to explore how stellar luminosity depends on stellar
mass and temperature.

Two models are developed:

- A **linear regression model** using stellar mass as a single feature
- A **polynomial regression model with interaction terms** using both mass and
  temperature

All models are implemented by explicitly defining:
- Hypothesis functions
- Loss functions (Mean Squared Error)
- Analytical gradients
- Gradient descent optimization

---

## Repository Structure
-/
-├── README.md
-├── 01_part1_linreg_1feature.ipynb
-└── 02_part2_polyreg.ipynb

---

## Notebook Summaries

### 1. Linear Regression with One Feature  
**File:** `01_part1_linreg_1feature.ipynb`

This notebook models stellar luminosity as a linear function of stellar mass:

\[
\hat{L} = wM + b
\]

Key components:
- Visualization of the mass–luminosity dataset and discussion of linearity
- Explicit implementation of the hypothesis function and MSE loss
- Visualization of the cost function surface \(J(w, b)\)
- Analytical derivation and implementation of gradients
- Gradient descent using both loop-based and vectorized approaches
- Convergence analysis for multiple learning rates
- Final model fit and discussion of systematic errors

This notebook highlights the limitations of linear models when applied to
intrinsically nonlinear physical phenomena.

---

### 2. Polynomial Regression with Interaction Terms  
**File:** `02_part2_polyreg.ipynb`

This notebook extends the linear model by incorporating polynomial and interaction
features to capture nonlinear effects:

\[
X = [M,\ T,\ M^2,\ M \cdot T]
\]

Key components:
- Multifeature dataset visualization with temperature encoding
- Polynomial feature engineering using NumPy vectorization
- Vectorized loss and gradient computation
- Gradient descent optimization
- Feature selection experiment comparing three models
- Sensitivity analysis of the interaction term
- Inference on a new stellar observation

This notebook demonstrates how feature engineering significantly improves model
expressiveness and predictive performance.

---

## AWS SageMaker Execution Evidence

All notebooks were uploaded and executed successfully in an **AWS SageMaker Studio**
environment using the integrated **Visual Studio Code interface**.

### SageMaker Environment Overview

screenshot 

```md
![SageMaker Studio Environment](PATH_TO_SAGEMAKER_OVERVIEW_IMAGE)


## Execution Evidence: Notebook 1
# Linear Regression with One Feature

Screenshot book 1

## Execution Evidence: Notebook 2
# Polynomial Regression with Interaction Terms

Screenshot book 2

## Cost Surface and 3D Visualization Evidence

The linear regression notebook includes a visualization of the cost function
surface 𝐽(𝑤,𝑏) illustrating the optimization landscape and the location of
the global minimum.

screenshot 3d

## Local vs AWS SageMaker Execution Comparison

The notebooks were executed both locally and within the AWS SageMaker environment.
The numerical results, convergence behavior, and visualizations were consistent
across both environments.

## Key observations:

- Identical loss convergence patterns

- Equivalent learned parameters

- No numerical instability observed

- SageMaker provides a controlled and scalable execution environment

This confirms that the implementation is portable and cloud-ready.

## Conclusion

This laboratory demonstrates how regression models can be built from first
principles to model physical phenomena such as stellar luminosity. Starting from
a simple linear model and progressing to polynomial regression with interaction
terms highlights the importance of model expressiveness and feature engineering.

Additionally, executing the models in AWS SageMaker reinforces the role of cloud
platforms as foundational infrastructure for modern data-driven and enterprise
systems. The lab successfully integrates theoretical understanding, practical
implementation, and cloud-based execution into a coherent workflow.

