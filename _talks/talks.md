---
layout: archive
title: "Talks"
permalink: /talks/
author_profile: true
redirect_from:
  - /talks
---

### [SMAI Biennal](https://smai2025.math.cnrs.fr/en/) (2025)

<FONT size="3pt">
<i> Mixed-Precision for solving large biological models </i>
</FONT>

<FONT size="2pt">
<br>
In computational biology, agent-based models (ABM) are a computational modelling approach for complex living systems, enabling heterogeneity across agents. ABMs are often better aligned with data from real large systems [2]. However, the computational cost, which can increase supra-linearly with size, is a major challenge that limits applicability. In our work, we suggest to tackle this problem with the use of mixed-precision.

Mixed-precision methods consist in using two or more numerical formats, usually floating point numbers [5], inside a single numerical method, to find a good trade-off between the accuracy and speed. These methods are developed in several fields that encounter similar dimensional computing problems such machine-learning [3], linear algebra [1] or meteorology [4].

Here, we consider an ABM of $N$ heterogeneous agents described by  a state variable in $X \in \mathbb{R}^{d N}$, where each agent is described by the $d$-dimensional sub-vector $\mathbf{X}_i$ in $\mathbb{R}^{d}$, extracted from $\mathbf{X}_i=\Big(X_{(i-1)d+1},...,X_{id}\Big)$. We assume that the dynamical dependence is split into two parts, an agent-centered term $F_i:\mathbb{R}\times\mathbb{R}^d\to\mathbb{R}^d$ and a term $G_{ij}:\mathbb{R}\times\mathbb{R}^d\times\mathbb{R}^d\to\mathbb{R}^d$ accounting for complex pairwise interactions, which are weighted by a vector $M_{ij} \in \mathbb{R}^d$. The state of each agent follows the nonlinear ODE:
\begin{equation*}
	\dot{\mathbf{X}_i}(t) = F_i(t,\mathbf{X}_i) + \sum_{j=1}^N M_{ij}(t,\mathbf{X}_i)\odot G_{ij}(t,\mathbf{X}_i,\mathbf{X}_j), \,i\in{1,...,N},
\end{equation*} 
where $\odot$ is the Hadamard, or element-wise, product.
We make no assumption on the form of  $G_{ij}$, except that all the $N$ agents can  interact heterogeneously with each other.  This leads to a right-hand side with a complexity in $N^2$ that is difficult to reduce.

We show that accuracy of numerical scheme is improved with the mixed-precision tuning as the system size increases. As the size of the population ($N$) increases, rounding errors coming from low precision terms are absorbed by the large number of interactions. This result is highlighted by a study exploring the parameters of three benchmarks. In addition, the complexity of non-linear functions used in modeling and the increasing size tend to increase the speed-up of low precision. This leads to an interesting gain in performance with a limited degradation in accuracy, particularly for interaction evaluations.
<br>
<br> [1] A. Abdelfattah, H. Anzt, A. Ayala, E. Boman, E. Carson, S. Cayrols, T. Cojean, J. Dongarra, R. Falgout,
M. Gates, et al. Advances in mixed precision algorithms : 2021 edition. Tech. rep., Lawrence Livermore
National Lab.(LLNL), Livermore, CA (United States), 2021.
<br> [2] C. M. Glen, M. L. Kemp, E. O. Voit. Agent-based modeling of morphogenetic systems : Advantages and
challenges. PLoS Comput. Biol, 15(3), e1006577, 2019.
<br> [3] J. Hayford, J. Goldman-Wetzler, E. Wang, L. Lu. Speeding up and reducing memory usage for scientific
machine learning via mixed precision. Comput. Methods Appl. Mech. Eng., 428, 117093, 2024.
<br> [4] T. N. Palmer. More reliable forecasts with less precise computations : A fast-track route to cloud-resolved
weather and climate simulators? Philos. Trans. R. Soc. London, Ser. A, 372(2018), 20130391, 2014.
<br> [5] D. Zuras, M. Cowlishaw, A. Aiken, M. Applegate, D. Bailey, S. Bass, D. Bhandarkar, M. Bhat, D. Bindel,
S. Boldo, et al. IEEE standard for floating-point arithmetic. IEEE Std, 754(2008), 1–70, 2008.
</FONT>



### [CANUM](https://canum2024.math.cnrs.fr/en/) (2024)

<FONT size="3pt">
<i> Mixed precision and local error in ordinary differential equations </i>
</FONT>

<FONT size="2pt">
<br>
In computational biology, many problems are modelled using individual-based or agent-based modelling. 
When expressed as ordinary differential equations (ODEs), these models lead to high-dimensional systems. 
The computational cost increases supra-linearly with the size of these systems. Accordingly, the solving of full-scale systems is intractable in terms of computational cost.

Given that biological problems often have high empirical uncertainties, it could be possible to take advantage of the trade-off between computational speed and accuracy.

Mixed precision consists in using different levels of arithmetic precision within one computational task. Several fields already use this technique, such as geophysics [1] or machine learning [2]. Mixed precision methods have also attracted attention for problems involving differential equations [3].

Our study deals with a population of heterogeneous agents of size $N$,  with $N \gg 1$, where each agent is described by a state variable $X_i \in \mathbb{R}^{d}$, which evolves according to an autonomous term ($F_i$, $i=1,...,N$) and a term accounting for complex pairwise interactions ($G_{ij}$, $i,j=1,...,N$). The following system of equations describes the general framework. For $i = 1,...,N$,

$$\begin{equation*}\dot{X}_i = F_i(X_i)+\frac{1}{N}\sum_{j=1}^{N} G_{ij}(X_i,X_j).\end{equation*}$$

The evaluation of the $N$ right-hand sides requires the sum of $N$ nonlinear terms, leading to a $O(N^2)$ complexity. Reducing the precision used during the sum could accelerate the whole evaluation process by a considerable amount, as performed with iterative refinement solvers in [4].

To reduce the degradation of the global accuracy, mixing the precision inside the evaluations could allow minimizing the impact of the numerical error due to the insertion of low precision [5]. 

We performed tests on two benchmarks, and our results show that as the size of the system increases, the error introduced by low precision is absorbed by numerical compensation in high-dimensional systems. Moreover, the local error (in comparison with a double precision solver) measured by the solver is more robust to low tolerances in the case of mixed precision than a full low precision solver.
<br>
<br> [1] J. Ackmann, P. D. Dueben, T. Palmer, P. K. Smolarkiewicz.Mixed-PrecisionforLinearSolversinGlobalGeophysicalFlows. J Adv Model Earth Syst, 2022.
<br> [2] M. Croci, G. R. de Souza.Mixed-precisionexplicitstabilizedRunge-Kuttamethodsforsingle-andmulti-scaledifferentialequations. J Comput Phys, 2022.
<br> [3] A. Haidar, S. Tomov, J. Dongarra, N. J. Higham.Harnessinggputensorcoresforfastfp16arithmetictospeedupmixed-precisioniterativerefinementsolvers. InSC18:Int.Conf.HighPerform.Comput.Netw.StorageAnal. IEEE, 2018.
<br> [4] J. Hayford, J. Goldman-Wetzler, E. Wang, L. Lu Speedingupandreducingmemoryusageforscientificmachinelearningviamixedprecision. arXiv preprint, 2024.
<br> [5] N. J. Higham, T. Mary.Mixedprecisionalgorithmsinnumericallinearalgebra. Acta Numerica, 2022
</FONT>
