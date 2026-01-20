# Constraint Optimization with Programmatic Model Generation

## Overview

This project demonstrates how to model and solve a large-scale constrained optimization problem in Python using the Gurobi optimizer.

The original problem arose in the final stage of my PhD research in mathematics. While the mathematical context is highly specialized, the optimization and software engineering challenges are broadly applicable and are the focus of this repository.

At a high level, the task was to prove an upper bound for a high-degree polynomial over a constrained domain by solving a nonlinear optimization problem with hundreds of constraints.

---

## The Optimization Challenge

- **Objective:** Maximize a polynomial of degree 11  
- **Variables:** 22 continuous variables  
- **Polynomial terms:** 264  
- **Constraints:** Hundredds of linear and low-degree polynomial constraints  

Manually writing this model would have been:
- Extremely time-consuming
- Error-prone
- Difficult to verify or modify

---

## Programmatic Model Generation

To manage this complexity, I wrote a **meta-script** that generates large portions of the optimization model automatically.

The generator:
- Encodes the structural patterns of the polynomial and constraints
- Produces valid Gurobi-compatible expressions
- Eliminates manual transcription errors
- Makes experimentation and modification feasible

The generated output can then be directly inserted into the main optimization model.

This approach mirrors real-world scenarios where models are too large or structured to be written by hand and must instead be generated algorithmically.

---

## Why This Matters

Although this project originated in pure mathematics, the techniques demonstrated here are directly relevant to:

- Algorithmic problem solving  
- Optimization-based systems  
- Constraint modeling  
- Engine and evaluation logic  
- Using code to manage complexity at scale  

These same ideas appear in areas such as AI systems, scheduling engines, and game evaluation functions.

---

## Files in This Repository

- `model_generator.ipynb` – Generates polynomial terms and constraints programmatically  
- `optimization_model.ipynb` – Builds and solves the optimization model using Gurobi

---

## Academic Reference

The optimization problem solved here appears in my PhD dissertation:

> *On the Triangle-Free Inducibility of Paths*  
> University of Colorado Denver, 2025  

(Full dissertation to be available soon on ProQuest)

---

## Final Note

The mathematical background behind this optimization is intentionally not required to understand or reuse the software techniques demonstrated here. The goal of this repository is to highlight how code can be used to safely and efficiently construct large, structured optimization models.
