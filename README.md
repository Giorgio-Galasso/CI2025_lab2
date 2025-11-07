🧭 __Travelling Salesman Problem (TSP)__

The Travelling Salesman Problem (TSP) asks for the shortest route that visits all cities exactly once and returns to the starting city.
It is an NP-hard optimization problem widely used in logistics and route planning.

__Techniques Used__

- Representation: each individual is a permutation of the nodes (TSP tour).

- Initialization: random population with fixed size.

- Evaluation: tour costs computed in a vectorized way using NumPy (and parallelized with Numba).

- Selection: tournament selection (best among k randomly chosen individuals).

- Crossover: Inver-Over operator, combining two parents by inverting segments guided by the second parent’s adjacency.

- Mutation: simple swap of two random nodes.

- Early stopping: stops evolution after a fixed number of generations without improvement.

- Reproducibility: fixed random seed for consistent results.

- Flow type: uses a hyper-modern Genetic Algorithm flow, where a genetic operator is selected probabilistically, the correct number of parents is chosen, and offspring are generated accordingly.

- Generational approach with elitism, where each new population replaces the previous one while preserving a small fraction of the best individuals.

__Final Considerations__

Unfortunately, I forgot to include the final numerical results in this report.
However, the algorithm achieved fairly good performance on the “g” problems by considering "Lab2 Best so far" table, while the results were not as good on the “r1” and “r2” problems.
One issue I noticed is that the convergence toward the optimal solution is quite slow, meaning the population often requires many generations to significantly improve.
Overall, the Genetic Algorithm provides reasonable solutions for structured instances, but further parameter tuning (e.g., mutation rate, crossover probability, or population size) would likely improve its performance on more complex or random cases.
Currently, no plots or visualizations are included to illustrate the convergence or the obtained tours.