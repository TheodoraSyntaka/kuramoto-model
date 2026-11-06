# Kuramoto model: particle simulation vs. mean-field theory

A numerical study of the Kuramoto model of coupled oscillators, 
comparing particle simulations with the predictions of mean-field 
theory.

![Animation of the Kuramoto model](kuramoto(1).gif)

## The problem
N oscillators, each with its own natural frequency, influence each 
other through a coupling strength K. Above a critical coupling K_c 
they spontaneously synchronise. In the limit of infinitely many 
oscillators, mean-field theory predicts the degree of synchronisation 
r exactly. For a Lorentz distribution of frequencies with width γ: 
K_c = 2γ and r = sqrt(1 - K_c/K) for K > K_c.

## Method
- Simulation in Python (numpy), Runge-Kutta 4 time stepping
- The mean-field form of the equation makes each step cost O(N)
- Comparison with theory for different K and different N

## Results
1. **Synchronisation transition:** the simulations reproduce the 
   predicted transition at K_c and the curve r(K).
2. **Finite-size effects:** below K_c the mean r decays like 1/sqrt(N), 
   as expected from the central limit theorem. Near K_c the 
   transition is rounded for finite N.

## Files
- `kuramoto.ipynb`: the full notebook with code, plots and explanations
- `kuramoto.gif`: animation of the oscillators on the unit circle

## Background
This project illustrates concepts from my PhD research in kinetic 
theory and interacting particle systems (mean-field limits and 
propagation of chaos), applied to a numerical example.
