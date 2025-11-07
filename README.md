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

- Elitism: a fraction of the best individuals is preserved in each generation.

- Early stopping: stops evolution after a fixed number of generations without improvement.

- Reproducibility: fixed random seed for consistent results.

- Flow type: uses a hyper-modern Genetic Algorithm flow, where a genetic operator is selected probabilistically, the correct number of parents is chosen, and offspring are generated accordingly.