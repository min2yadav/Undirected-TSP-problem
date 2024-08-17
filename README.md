# Undirected-TSP-problem

Introduction:
The Traveling Salesman Problem (TSP) is a classic optimization problem that involves finding the shortest possible route that visits a set of cities exactly once and returns to the starting city. We explore the process of solving the Undirected TSP using different optimization techniques and tools.

1. Gekko Solver Approach: \
The initial part of the code demonstrates the use of the GEKKO optimization library to solve a mixed-integer nonlinear programming (MINLP) problem. The given code defines a mathematical model to minimize a non-linear objective function while satisfying constraints. The variables are restricted to integer values within specified bounds. The objective function involves cubic terms, and the constraints ensure that the sum of variables equals a constant value. The GEKKO solver is used to find the solution. The provided solution is compared against known optimal values to verify correctness.


3. Pyomo Solver Approach: \
The next section of the code utilizes the Pyomo library to solve the same optimization problem. The Pyomo code formulates the problem as a mixed-integer linear programming (MILP) model. It introduces binary variables and relaxation coefficients (λ) to linearize the non-linear terms in the objective function. The constraints are defined to ensure that the relaxation coefficients and binary variables satisfy certain conditions. The Pyomo model is then solved using the CBC solver. The obtained objective value is compared with the previous solutions to validate the approach.


5. TSP Problem with Pyomo: \
The report proceeds to address the classic TSP using the Pyomo library. The code reads a distance matrix from an external source and constructs a ConcreteModel to model the TSP. The variables represent binary decisions indicating whether a route exists between cities. Constraints are defined to ensure that each city is visited exactly once and that sub-tour elimination constraints are enforced to prevent cycles. The objective function aims to minimize the total distance traveled. The CBC solver is applied to solve the TSP model.

4. Conclusion: \
We explored different approaches to solving the Undirected Traveling Salesman Problem. We showcased the use of GEKKO and Pyomo libraries to solve optimization problems with both non-linear and linear components. The provided code snippets demonstrated how to formulate and solve problems related to optimizing routes and minimizing distances while considering variousconstraints. The CBC solver effectively resolved the TSP instances, providing optimal or near-optimal solutions within a reasonable time frame.
