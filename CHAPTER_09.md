# 1. Explain P, NP, NP complete and NP-Hard problems. Give examples of each.

## P

- The class p consists of those problem that are solvable in **polynomial time** by **deterministic algorithms**.
- More specifically, they are problems that can be solved in time O(n^k) for some constant k, where n is the size of the input to the problem.
- Examples of P class problems are:
  1. A set of decision problems with yes/no answer.
  2. Calculating the greatest common divisor.
  3. Sorting of n numbers in ascending or descending order.
  4. Searching of an element from the list, etc.

## NP

- The class p consists of those problem that are solvable in **polynomial time** by **Non-deterministic algorithms**.
- The class NP consists of those problems that are "verifiable" in polynomial time. 
- Examples of NP class problems are:
  1. Knapsack problem O(2^n/2)
  2. Travelling salesperson problem (O(n^2*2^n)).
  3. Graph coloring problem.
  4. Hamiltonian circuit problems, etc...

## NP-hard

- A problem is NP-hard if all problems in NP are polynomial time reducible to it.
- Example : 
  1. Hamiltonian Cycle
  2. The circuit-satisfiability problem
  3. Set Cover
  4. Vertex Cover
  5. Travelling Salesman Problem

## NP-complete

- The group of problems which are both in NP and NP-hard are known as NP-complete problem.
- Example :
 1. Boolean satisfiability problem (SAT)
 2. Knapsack problem.
 3. Hamiltonian path problem.
 4. Travelling salesman problem (decision version)
 5. Subgraph isomorphism problem.
 6. Subset sum problem.
 7. Clique problem.

<img src="https://miro.medium.com/max/828/0*nedxMbwYe3CzPGga.png" width=50%>




# 2. Explain polynomial reduction.
<img src="https://raw.githubusercontent.com/Jaydeep990/ADA/main/PNG/9.1.png" width=50%>
<img src="https://raw.githubusercontent.com/Jaydeep990/ADA/main/PNG/9.2.png" width=50% >
