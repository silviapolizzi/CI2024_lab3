# Lab 3 Computational Intelligence
## n-Puzzle description
The n-Puzzle is a sliding puzzle that consists of a frame of numbered square tiles in random order with one tile missing. The puzzle also exists in other sizes, particularly the smaller 8-puzzle. If the size is 3×3 tiles, the puzzle is called the 8-puzzle or 9-puzzle, respectively, for the number of tiles and the number of spaces. The goal of the puzzle is to place the tiles in order by making sliding moves that use the empty space.
It's a (n^2-1)-puzzle, where n is the number of rows and columns.

## Algorithms implemented
### Informed Search
#### Best-First Search
Best-First Search is a search algorithm that explores a graph by expanding the most promising node chosen according to a specified rule. The algorithm uses a priority queue to keep track of the nodes that need to be explored.

#### A* Search
A* Search is a search algorithm that finds the shortest path between the initial and the final node. It uses a heuristic function to estimate the cost of the cheapest path through a node. The algorithm uses a priority queue to keep track of the nodes that need to be explored.

The main difference between Best-First Search and A* Search is that A* Search uses both the cost to reach a node and the heuristic function to estimate the cost of the cheapest path through a node, while Best-First Search only uses the heuristic function.

### Heuristic Function
The heuristic function is used to estimate the cost of the cheapest path from the current node to the goal node. In this laboratory task, the heuristic function used is the Manhattan distance, which is the sum of the horizontal and vertical distances between the current node and the goal node.
#### Manhattan Distance
The Manhattan distance is the sum of the horizontal and vertical distances between the current node and the goal node. It is calculated as the absolute difference between the x-coordinates and the y-coordinates of the current node and the goal node.

## Results
The initial state is generated randomly performing 1000 steps from the goal state.
The following results correspond to a 3x3 puzzle:

| Algorithm | Time (s) | Path Length (Quality) | N. actions evaluated (Cost) | Efficiency (Quality/Cost) |
|-----------|----------|-----------------------|-----------------------------| ------------------------- |
| Best-First| 0.0151  | 42                    | 502                          |  0.0837                 |
| A*        | 0.0732    | 24                   | 3010                        |  0.0080                  |



## Discussion

From the result we can see that the Best-First Search algorithm is more efficient than the A* Search algorithm. The Best-First Search algorithm evaluates fewer actions and has a higher efficiency than the A* Search algorithm. The Best-First Search algorithm is faster than the A* Search algorithm because it evaluates fewer actions and has a higher efficiency. However, A* find the optimal path, while Best-First Search does not guarantee the optimal path. The A* is also infeasible for large problems (e.g. 5x5) because it evaluates a large number of actions and become very slow.
