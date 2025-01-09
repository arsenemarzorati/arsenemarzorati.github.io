---
layout: archive
title: "Talks"
permalink: /talks/
author_profile: true
redirect_from:
  - /talks
---

[CANUM](https://canum2024.math.cnrs.fr/en/) (2024)
=======

**Mixed precision and local error in ordinary differential equations**

<FONT size="2pt"> In computational biology, many problems are modelled using individual-based or agent-based modelling. 
When expressed as ordinary differential equations (ODEs), these models lead to high-dimensional systems. 
The computational cost increases supra-linearly with the size of these systems. Accordingly, the solving of full-scale systems is intractable in terms of computational cost.

Given that biological problems often have high empirical uncertainties, it could be possible to take advantage of the trade-off between computational speed and accuracy.

Mixed precision consists in using different levels of arithmetic precision within one computational task. Several fields already use this technique, such as geophysics [1] or machine learning [2]. Mixed precision methods have also attracted attention for problems involving differential equations [3].

Our study deals with a population of heterogeneous agents of size $N$,  with $N \gg 1$, where each agent is described by a state variable $X_i \in \mathbb{R}^{d}$, which evolves according to an autonomous term ($F_i$, $i=1,...,N$) and a term accounting for complex pairwise interactions ($G_{ij}$, $i,j=1,...,N$). The following system of equations describes the general framework. For $i = 1,...,N$,

$$\dot{X}_i = F_i(X_i)+\frac{1}{N}\sum_{j=1}^{N} G_{ij}(X_i,X_j).$$

The evaluation of the $N$ right-hand sides requires the sum of $N$ nonlinear terms, leading to a $O(N^2)$ complexity. Reducing the precision used during the sum could accelerate the whole evaluation process by a considerable amount, as performed with iterative refinement solvers in [4].

To reduce the degradation of the global accuracy, mixing the precision inside the evaluations could allow minimizing the impact of the numerical error due to the insertion of low precision [5]. 

We performed tests on two benchmarks, and our results show that as the size of the system increases, the error introduced by low precision is absorbed by numerical compensation in high-dimensional systems. Moreover, the local error (in comparison with a double precision solver) measured by the solver is more robust to low tolerances in the case of mixed precision than a full low precision solver.


[1] J. Ackmann, P. D. Dueben, T. Palmer, P. K. Smolarkiewicz.Mixed-PrecisionforLinearSolversinGlobalGeophysicalFlows. J Adv Model Earth Syst, 2022.\
[2] M. Croci, G. R. de Souza.Mixed-precisionexplicitstabilizedRunge-Kuttamethodsforsingle-andmulti-scaledifferentialequations. J Comput Phys, 2022.\
[3] A. Haidar, S. Tomov, J. Dongarra, N. J. Higham.Harnessinggputensorcoresforfastfp16arithmetictospeedupmixed-precisioniterativerefinementsolvers. InSC18:Int.Conf.HighPerform.Comput.Netw.StorageAnal. IEEE, 2018.\
[4] J. Hayford, J. Goldman-Wetzler, E. Wang, L. Lu Speedingupandreducingmemoryusageforscientificmachinelearningviamixedprecision. arXiv preprint, 2024.\
[5] N. J. Higham, T. Mary.Mixedprecisionalgorithmsinnumericallinearalgebra. Acta Numerica, 2022
</FONT>