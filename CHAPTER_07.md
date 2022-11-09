# CHAPTER-7 (B & B&B)

## 1. Difference between Backtracking and Branch-N-Bound

| Parameter    | Backtracking                                                                                                                                                                                                                                             | Branch and Bound                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Approach     | Backtracking is used to find all possible solutions available to a problem. When it realises that it has made a bad choice, it undoes the last choice by backing it up. It searches the state space tree until it has found a solution for the problem.  | Branch-and-Bound is used to solve optimisation problems. When it realises that it already has a better optimal solution that the pre-solution leads to, it abandons that pre-solution. It completely searches the state space tree to get optimal solution. |
| Traversal    | Backtracking traverses the state space tree by DFS(Depth First Search) manner.                                                                                                                                                                           | Branch-and-Bound traverse the tree in any manner, DFS or BFS.                                                                                                                                                                                               |
| Function     | Backtracking involves feasibility function.                                                                                                                                                                                                              | Branch-and-Bound involves a bounding function.                                                                                                                                                                                                              |
| Problems     | Backtracking is used for solving Decision Problem.                                                                                                                                                                                                       | Branch-and-Bound is used for solving Optimisation Problem.                                                                                                                                                                                                  |
| Searching    | In backtracking, the state space tree is searched until the solution is obtained.                                                                                                                                                                        | In Branch-and-Bound as the optimum solution may be present any where in the state space tree, so the tree need to be searched completely.                                                                                                                   |
| Efficiency   | Backtracking is more efficient.                                                                                                                                                                                                                          | Branch-and-Bound is less efficient.                                                                                                                                                                                                                         |
| Applications | Useful in solving N-Queen Problem, Sum of subset.                                                                                                                                                                                                        | Useful in solving Knapsack Problem, Travelling Salesman Problem.                                                                                                                                                                                            |
| Solve        | Backtracking can solve almost any problem. (chess, sudoku, etc ).                                                                                                                                                                                        | Branch-and-Bound can not solve almost any problem.                                                                                                                                                                                                          |

## 2. N Queen Problem

- The N Queen is the problem of placing N chess queens on an N×N chessboard so that no two queens attack each other. 
- For example, the following is a solution for the 4 Queen problem.
<img src="https://media.geeksforgeeks.org/wp-content/uploads/N_Queen_Problem.jpg" width=20%>

- It can be solved using backtracking. 

##### Backtracking Algorithm 

- The idea is to place queens one by one in different columns, starting from the leftmost column. When we place a queen in a column, we check for clashes with already placed queens. 
- In the current column, if we find a row for which there is no clash, we mark this row and column as part of the solution.
- If we do not find such a row due to clashes, then we backtrack and return false.

##### Complexity

- Time Complexity: O(N!)
- Space Complexity: O(N)

###### PPT for Example

## 3.Explain Minimax principal.

- Minimax is a kind of backtracking algorithm.
- It is used in decision making and game theory to find the optimal move for a player, assuming that your opponent also plays optimally. 
- It is widely used in two player turn-based games such as Tic-Tac-Toe, Backgammon, Mancala, Chess, etc.
- In Minimax the two players are called **maximizer** and **minimizer**.
- The maximizer tries to get the highest score possible while the minimizer tries to do the opposite and get the lowest score possible.

#### Game tree:
<img src="https://www.baeldung.com/wp-content/uploads/2017/07/minimax.png">

#### minimax game tree in tic tac toe:
<img src="https://miro.medium.com/max/1100/1*lTRfOi9LUuwikeJ93xWOjA.png">




