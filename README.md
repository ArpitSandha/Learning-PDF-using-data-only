# Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model

## Assignment Overview

This project estimates the parameters of a probability density function (PDF) using a non-linear transformation of NO₂ air quality data.

Dataset used:
India Air Quality Dataset (Kaggle)

Feature:
NO₂ concentration (x)

---

## Step 1: Non-Linear Transformation

Each NO₂ value (x) is transformed into z using:

z = x + a_r sin(b_r x)

where:

a_r = 0.05 × (r mod 7)  
b_r = 0.3 × (r mod 5 + 1)  

r = University Roll Number

---

## Step 2: Probability Density Function

We estimate parameters of:

p̂(z) = c · exp(−λ (z − μ)²)

Parameters learned:
- μ (mean)
- λ (spread parameter)
- c (normalization constant)

---

## Estimation Method

Parameters are estimated using Maximum Likelihood Estimation (MLE).

μ = mean(z)  
σ² = variance(z)  
λ = 1 / (2σ²)  
c = 1 / √(2πσ²)

---

## Final Output

The learned parameters (λ, μ, c) are submitted as required in the assignment.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Google Colab

---

## Learning Outcome

- Understanding probability density functions
- Non-linear transformations
- Parameter estimation using MLE
- Gaussian distribution modeling
