# 🐜 Ant Colony Optimization (ACO)

A Python implementation of the **Ant Colony Optimization (ACO)** algorithm for solving the **Traveling Salesman Problem (TSP)** using swarm intelligence. The project demonstrates how artificial ants collaboratively discover near-optimal routes by depositing and following pheromone trails while balancing exploration and exploitation.

## Features

* Ant Colony Optimization algorithm from scratch
* Traveling Salesman Problem (TSP) solver
* Probabilistic path selection using pheromone intensity and distance heuristic
* Configurable parameters (`alpha`, `beta`, evaporation rate, number of ants, iterations)
* Pheromone evaporation and reinforcement mechanism
* Easy-to-understand and modular implementation
* Suitable for learning bio-inspired optimization algorithms

## How It Works

The algorithm simulates the foraging behavior of ants:

1. Initialize pheromone levels uniformly across all paths.
2. Place multiple ants at random starting cities.
3. Each ant constructs a complete tour by selecting the next city based on:

   * Current pheromone concentration
   * Distance to neighboring cities
4. After completing a tour, ants deposit pheromones proportional to the quality of their solution (shorter routes receive more pheromone).
5. Existing pheromones gradually evaporate to prevent premature convergence.
6. Repeat the process for several iterations until the best route is found.

## Formula

The probability of selecting the next city is determined by:

```text
Score = (Pheromone)^α × (1 / Distance)^β
```

where:

* **α (alpha)** controls the influence of pheromone trails.
* **β (beta)** controls the influence of the distance heuristic.

## Applications

* Traveling Salesman Problem (TSP)
* Vehicle Routing Problems (VRP)
* Logistics and Supply Chain Optimization
* Network Routing
* Scheduling and Resource Allocation
* Robotics Path Planning

## Technologies

* Python
* NumPy
* Matplotlib (optional for visualization)

## Repository Structure

```text
├── aco.py               # Ant Colony Optimization implementation
├── tsp.py               # Traveling Salesman Problem utilities
├── utils.py             # Helper functions
├── datasets/            # Sample distance matrices
├── results/             # Output routes and visualizations
└── README.md
```

## Future Improvements

* Dynamic parameter tuning
* Parallel ant simulation
* Visualization of pheromone evolution
* Support for asymmetric TSP
* Benchmarking against Genetic Algorithms and Simulated Annealing

## License

This project is intended for educational purposes and research in swarm intelligence and optimization algorithms.
