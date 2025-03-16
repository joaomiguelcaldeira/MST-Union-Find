# MST-Union-Find

## How to Run the project
`gcc project.c -o project` <br>
`./project {input_file}`

Note that there are sample inputs in `tests/` that you can use to test the code.

## Project Details

A transportation network problem is given with the objective of maximum connection at the lowest cost possible. The solution presented implements the Kruskal Algorithm with Sorting and Union-Find by ranks structure to solve as a Minimum Spanning Tree problem by designing it as a graph.

## The Problem
In this project, you must design a cost-effective transportation network connecting multiple cities using highways and shipping ports.

You have a map of city locations and costs for building highways between cities and constructing shipping ports at individual cities.

The objective is to ensure there is a viable route between every pair of cities, either directly or indirectly through intermediate cities. At least one city must construct a shipping port, and any city capable of building a port must do so, given its strategic importance. Cities with shipping ports are directly connected to other port cities. Cities without ports must be interconnected by highways. All connections operate in both directions.

The solution must determine the optimal placement of shipping ports and highways to minimize the overall construction cost while ensuring connectivity for all cities.

## Input Format

The input file is structured as follows:

- The first line contains an integer `N` (where `N ≥ 2`), representing the number of cities.
- The second line contains an integer `A` (`0 ≤ A ≤ N`), indicating the number of cities eligible to build shipping ports.
- The next `A` lines each contain two integers, `a` and `c`, separated by a space, where `c` is the cost to build a shipping port in city `a`.
- The next line contains an integer `E`, indicating the number of potential highway connections.
- The next `E` lines each contain three integers, `a`, `b`, and `c`, separated by spaces, representing a highway connection between cities `a` and `b` with construction cost `c`.
Cities are numbered from `1` to `N`.

## Output Format
- If constructing the required network is impossible, the output must contain a single line with the word `Impossible`.
- Otherwise, the first line contains the total cost of the network.
- The second line contains two integers separated by a space: the number of shipping ports built and the number of highway connections used.

## Example

### Input
4<br>
3<br>
1 1<br>
2 5<br>
3 1<br>
4<br>
1 2 1<br>
1 3 6<br>
2 4 2<br>
3 4 3<br>

### Output
9
3 1
