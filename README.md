# PEM Electrolyzer Diffusion Modeling

A simplified 2D numerical model of membrane hydration and diffusion-driven water transport in a PEM water electrolyzer, based on publicly available scientific literature.

## Project Scope

This project investigates membrane water transport in a simplified PEM electrolyzer domain.

The model focuses on the diffusion-driven contribution to membrane hydration and does not attempt to reproduce a full multiphysics electrolyzer model.

The workflow includes:

- 2D finite-difference discretization
- Hydration-dependent membrane diffusivity
- Iterative nonlinear solution
- Boundary-condition implementation
- Convergence monitoring
- Calculation of membrane hydration
- Calculation of local diffusivity
- Calculation of diffusion-driven water flux
- Comparison of two pore-pattern configurations

## Numerical Model

The model solves a steady diffusion equation in which the membrane water diffusivity depends on the local hydration state.

Because diffusivity changes with hydration, the numerical problem is nonlinear and is solved iteratively.

At each iteration:

1. The current solution field is converted to membrane water content.
2. Local hydration is calculated.
3. Hydration-dependent diffusivity is updated.
4. The discretized diffusion equation is solved.
5. Boundary conditions are reapplied.
6. Iterations continue until convergence.

## Main Outputs

The numerical model produces three main fields:

- Membrane hydration distribution
- Hydration-dependent diffusivity distribution
- Diffusion-driven water-flux field

The results show strong spatial dependence near the prescribed water-access regions and demonstrate how pore placement influences local membrane hydration and diffusion behavior.

## Interpretation

The comparison between the two pore-pattern configurations showed only a small difference in average hydration in the diffusion-only model.

This indicates that membrane diffusion alone is not sufficient to explain the full electrochemical performance differences reported for different porous transport layer architectures.

Additional coupled processes such as electro-osmotic drag, reaction kinetics, ionic-current distribution, liquid-water transport, and gas removal would be required for a full-cell model.

## Research Summary

A condensed project summary is available in the `docs` folder.

## Source and Scope Note

This is an independent numerical implementation based on publicly available scientific literature.

No proprietary HySON data, code, geometries, or confidential project material are included.

The repository presents a simplified diffusion-only model for research and portfolio purposes and should not be interpreted as a validated full PEM electrolyzer simulation.
