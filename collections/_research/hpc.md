---
title: High-performance computing
code: hpc
feature_row:
  - image_path: "/assets/pics/CubedSphereSm.png" 
  - class: "ndsa"
---
{% include feature_row type="center" %}

Many areas of science and engineering rely on the fast solution of very large systems of equations with millions or even billions of unknowns. For example, in numerical weather- and climate-prediction, the equations of fluid dynamics are discretised and solved on a computational grid with hundreds of millions of grid points. They have to be solved in less than an hour—tomorrow's weather forecast would be useless if it took a week to produce it!

Computational problems of this size can only be solved with the fastest available numerical algorithms and on massively parallel supercomputers with a hundred thousand or more compute cores.
In collaboration with the UK Met Office, we develop fast and massively parallel geometric multigrid solvers for partial differential equations (PDEs) in numerical weather prediction. We design new multilevel methods for solving stochastic partial differential equations (SDEs) in atmospheric-dispersion modelling. We have a strong interest in the implementation of these algorithms on novel chip architectures such as GPUs, which require the application of state-of-the-art software development techniques to achieve performance-portability.