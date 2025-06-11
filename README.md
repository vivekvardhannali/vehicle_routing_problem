# Vehicle Routing Optimization using Genetic Algorithms  

This project provides an end-to-end solution for the **Vehicle Routing Problem (VRP)** using **Genetic Algorithms**, implemented with the DEAP library. The goal is to optimize delivery routes from a depot to multiple customer locations using a fixed number of vehicles, minimizing total travel distance and improving load balancing.  

---

## Overview  

-> **Objective**: Optimize routing for 100 delivery locations using 10 vehicles, minimizing total distance and imbalance among vehicle routes.  
-> **Approach**: Applied a **genetic algorithm** for combinatorial optimization using custom crossover, mutation, and evaluation strategies.  
-> **Tech Stack**:  
   - Python  
   - DEAP (Evolutionary Computation)  
   - NumPy, Matplotlib (Visualization & Math)  

---

## Problem Description  

-> Each of the 100 randomly generated customer locations must be visited exactly once.  
-> Each of the 10 vehicles starts and ends at a common depot.  
-> The objective is twofold:  
   - Minimize total travel distance  
   - Maintain balanced workloads among vehicles (low standard deviation in route lengths)  

---

## Genetic Algorithm Design  

-> **Chromosome Encoding**: A permutation of location indices assigned across vehicles.  
-> **Fitness Function**:  
   - Total route distance  
   - Route imbalance penalty (standard deviation of vehicle distances)  
-> **Crossover**: Partially Matched Crossover (`cxPartialyMatched`)  
-> **Mutation**: Index shuffling (`mutShuffleIndexes`)  
-> **Selection**: Tournament selection (`selTournament`)  

---

## Results  

-> Successfully optimized routes across 400 generations  
-> Output visualizes optimized vehicle paths from depot to locations  
-> Achieved notable reduction in total travel distance and balanced routing among vehicles  

---

## Highlights  

-> Tackles a classic logistics and supply chain problem using evolutionary algorithms  
-> Demonstrates how **route optimization** can be automated with genetic search  
-> Fully visualized solution with customizable location count, vehicle count, and mutation rate  

---

## Future Improvements  

-> Integrate real-world map APIs (e.g., Google Maps distance matrix)  
-> Add capacity constraints per vehicle  
