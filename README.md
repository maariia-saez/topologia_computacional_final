# Final Project: Computational Topology and Topological Data Analysis (TDA)

This repository contains a Python implementation of a library for the analysis and computation of simplicial homology, developed as part of the Computational Topology course.

## Implemented Features

The project is built around a core `SimplicialComplex` class that models topological objects and computes their algebraic invariants from scratch, without relying on external TDA libraries.

### 1. Basic Structures & Topology
- **Complex Management:** Simplex insertion with automatic face closure to ensure valid simplicial structures.
- **Topological Operations:** Computation of the *Star* and *Link* of a simplex.
- **Connectivity:** Calculation of connected components ($\beta_0$) using Disjoint Set Union (Union-Find) structures.
- **Euler Characteristic:** Computation of the topological invariant $\chi = \sum (-1)^k s_k$.

### 2. Homological Algebra
- **Homology Computation:** Implementation of the **Smith Normal Form** over $\mathbb{Z}_2$ to compute the rank of boundary matrices.
- **Betti Numbers:** General algorithm to obtain $\beta_p$ (number of $p$-dimensional holes/cycles) from the boundary matrices.

### 3. Filtrations & Geometric Complexes
- **Vietoris-Rips Complex:** Efficient construction from point clouds in $\mathbb{R}^n$ by computing pairwise distances and cliques.
- **Persistent Homology (Incremental Algorithm):** Computation of the birth and death of cycles to generate barcodes/diagrams as simplices are added to the filtration.
- **Alpha Complexes:** Implementation based on Delaunay Triangulation (via `scipy.spatial`) and geometric filtration using triangle and edge circumradii.

## Technical Requirements

This project relies on the following libraries for numerical and geometric computations:

- `numpy`: Matrix operations and linear algebra.
- `scipy`: Spatial algorithms (Delaunay, Voronoi, pdist) required for the geometric construction of complexes.
- `matplotlib`: Visualization of 2D simplicial complexes.

## Usage Examples

The main notebook (`TrabajoTopologia.ipynb`) includes practical case studies:
1. **Annulus Homology:** Topological verification of a space with 1 hole ($\beta_1=1$).
2. **Point Cloud Analysis:** Detection of underlying topology in scattered data through the construction of Rips and Alpha complexes.

---
*Future Work: Implementation of relative homology and sparse matrix optimization.*
