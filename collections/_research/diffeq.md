---
title: Differential equations
code: de
feature_row:
  - image_path: "/assets/pics/helmholtz.jpg" 
    btn_label: "Scattering"
    url: "/research/diffeq.html#scattering"
  - image_path: "/assets/pics/seuler_cat.png" 
    btn_label: "Geometric integration"
    url: "/research/diffeq.html#gi"
  - image_path: "/assets/pics/mov_mesh.png" 
    btn_label: "Moving meshes"
    url: "/research/diffeq.html#mm"
---
{% include feature_row %}

<p>We have a long-standing and broad interest in the numerical analysis of differential equations.</p>

<p class="notice--info" id="scattering"><strong>High-frequency scattering </strong> Our understanding of acoustic and electromagnetic wave scattering underpins technologies such as radar, sonar, telecommunications, ultrasound, and seismic imaging. Many of these applications require the accurate computation of high-frequency waves. However, standard numerical methods become increasingly expensive as the frequency increases, putting very high-frequency problems out of range of standard methods. Recent research in Bath has looked at ways to combat this, including the design of 'hybrid numerical-asymptotic methods', and novel preconditioners for use in conjunction with domain decomposition methods.</p>

<p class="notice--info" id="gi"><strong>Geometric integration </strong>
The second image shows snapshots of the evolution of a cat shape under a Hamiltonian flow map. The map is symplectic and while the shape of the cat changes its area is preserved. To explore the delicate dynamics of such systems, it is necessary that such geometric features are preserved by the numerical approximation in order to respect the underlying physics. The group in Bath looks at developing general linear methods for Hamiltonian differential equations and adaptive numerical methods for capturing shocks and singularities in PDEs with conservation laws.</p>

 <p class="notice--info" id="gi"><strong>Moving-mesh methods </strong> 
Numerical methods for PDEs usually require the construction of a mesh on which the PDE is then discretised. However, if a fixed mesh is used during the computation then this can lead to poor resolution of the evolving features of the PDE and also the loss of important qualitative formation such as conservation and balance laws. This is a major problem in many areas of computation of the inherently multi-scale problems that arise in nature, a particular example being meteorology. Budd is actively working in the construction of moving meshes in 3D which progressively move mesh points to resolve emergent features. These have already proved very effective for a wide range of problems and are now used as part of a data assimilation calculation in the UK Met Office Operational Code. Much new work needs to be done to extend these methods to work on the whole sphere and to study the complex PDEs encountered in nature. Moving mesh methods are a lovely mix of differential geometry, dynamical systems theory and numerical analysis with major practical applications.</p>