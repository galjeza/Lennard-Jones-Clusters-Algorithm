# Lennard-Jones Clusters with jDE Algorithm

This repository contains an implementation of the jDE algorithm to solve the Lennard-Jones Clusters problem. The goal is to determine the arrangement of atoms in 3D space that minimizes the potential energy.

## Problem Description

Atoms are placed in a 3D space within an interval `[-6, 6]`. The objective is to find the minimum value of the function:

    f(Xi,G)=4∗∑_{i=1}^{N-1}∑_{j=i+1}^N(d^{-12}_{i,j}(Xi,G)−d^{-6}_{i,j}(Xi,G))
    Xi,G={P1,i,x,P1,i,y,P1,i,z,...,PN,i,x,PN,i,y,PN,i,z}

Where `d_{i,j}` is the Euclidean distance between atoms `i` and `j`.

## Algorithm

The jDE algorithm uses a population-based approach where solutions are mutated, crossed over, and selected to form the next generation. The algorithm stops based on certain stopping criteria like the target solution quality, runtime limit, or the number of solution evaluations.

## Usage

To run the program:

```bash
g++ main.cpp -o ljclusters
./ljclusters N <unsign int> -seed<unsigned int> -target <double> [-nfesLmt | -runtimeLmt] <unsigned int>

## Output

The program outputs:
- Number of atoms (N)
- Seed used for randomness
- Number of function evaluations
- Runtime of the algorithm in seconds
- Speed (evaluations per second)
- Energy of the best-found solution
- Coordinates of the best solution



