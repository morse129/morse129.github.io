---
title: "A simulation framework for nanodroplet breakup in top-down nanoparticle production"
collection: publications
category: conference_abstracts
permalink: /publication/2024-10-31-a-simulation-framework-for-nanodroplet-breakup-in-top-down-nanoparticle-production
excerpt: 'Development of a boundary-element method for small-scale droplet breakup.'
date: 2024-10-31
venue: 'AIChE Annual Meeting'
teaser: 
slidesurl: 
paperurl: 
citation: 'Morse, N., Remmelgas, J., & Khinast, J. (2024). &quot;A simulation framework for nanodroplet breakup in top-down nanoparticle production&quot; <i>AIChE Annual Meeting</i>. San Diego, USA.'
---

## Abstract 

### Introduction

Nanoparticles have shown great promise as a pharmaceutical carrier, evidenced most strongly by the success of lipid nanoparticles as carriers for mRNA vaccines during the COVID-19 pandemic. However, the fundamental processes that govern nanoparticle formation are still not well understood and particle size predictions are generally reliant on empiricism. Numerical simulations offer the potential to inform a variety of nanoparticle production methods, such as fragmentation of particle suspensions in impinging jets, turbulent mixing for flash nanoprecipitation and nanoparticle self-assembly, and nanoemulsion formation. However, simulations are impeded by the vast separation of length and time scales between the pharmaceutical processing scale and the nanoparticle scale: the nanoscale is around one million times smaller than the production scale, and the disparity in timescales one million times greater still. Accordingly, the resolution of all scales in a single simulation is computationally infeasible.

In order to overcome this computational hurdle, a coupling framework between simulations of the macroscale production device and mesoscale behavior is required. Considering nanoemulsion formation, one may take advantage of the fact that nanodroplet sizes are smaller than the smallest turbulent (Kolmogorov) scales of the flow [1], which results in a low droplet Reynolds number based on the shear rate, diameter, and carrier fluid kinematic viscosity. This, combined with the small Stokes number of the droplets, permits a coupled macroscale-mesoscale simulation framework.

### Methodology

The simulation framework consists of two parts: on the macroscale, the nanoparticle production device is simulated using a traditional finite volume method computational fluid dynamics (CFD) solver. Massless tracers are advected through the flow to record the strain rate histories along the Lagrangian trajectories of the droplets. Since the strain rates are dominated by the smallest turbulent scales, computationally-intensive direct numerical simulations (DNS) or large-eddy simulations (LES), combined with a strain rate reconstruction technique [2], are required.

These Lagrangian strain histories are used as input to an ensemble of auxiliary simulations of the droplet deformation. The droplet shape deformation is calculated using a boundary element method (BEM) to resolve the viscously-dominated flow around the droplets. In the BEM, only the droplet interface is tracked, reducing the computational expense for each calculation. In this framework, the effect of differing droplet/carrier viscosities, surface tensions, and surfactants are readily investigated [3,4], and the breakup of droplets can be attributed to specific regions of the mixing device.

### Results

We discuss results from both the macroscopic and mesoscopic simulations. On the macroscale, the flow-fields in nanoparticle production devices are investigated, including the insights simulations provide into the physics of the most critical regions in these devices. On the nanodroplet scale, we present results of droplet deformation and discuss the incorporation more complex nanoscale effects in the simulation framework.

### Literature

1. Gupta, A., Eral, H. B., Hatton, T. A., & Doyle, P. S. (2016). "Controlling and predicting droplet size of nanoemulsions: Scaling relations with experimental validation". *Soft Matter*, 12(5).

2. Johnson, P. L., & Meneveau, C. (2018). "Predicting viscous-range velocity gradient dynamics in large-eddy simulations of turbulence". *Journal of Fluid Mechanics*, 837, 80–114.

3. Pozrikidis, C. (1992). "Boundary integral and singularity methods for linearized viscous flow". *Cambridge University Press*.

4. Cristini, V., Bławzdziewicz, J., Loewenberg, M., & Collins, L. R. (2003). "Breakup in stochastic Stokes flows: Sub-Kolmogorov drops in isotropic turbulence". *Journal of Fluid Mechanics*, 492, 231–250.