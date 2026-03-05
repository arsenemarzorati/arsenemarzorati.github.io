---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
redirect_from:
  - /publications
---

## *Mixed-precision for solving large ODEs systems*

<FONT size="2pt">
Al-Sayed Ali M, Bernard S, Marzorati A, Rouzaud-Cornabas J. (In writing)
</FONT>

### *Mixed precision implicit numerical schemes for systems of ordinary differential equations*

<FONT size="2pt">
Al-Sayed Ali M, Bernard S, Marzorati A, Rouzaud-Cornabas J. Numerical Algorithms. (2025)

<br> Ordinary differential equations (ODEs) are widely used to model complex systems in biology, which result from the interactions of a large number of cells or organisms. This can lead to a substantial system size. These complex interactions can quickly alter their behavior, and some biological systems are stiff when represented as ODEs [59]. Therefore, these stiff ODEs could benefit from implicit numerical schemes. However, each iteration of these schemes involves solving a large nonlinear system, typically using the Newton method. To guarantee the global convergence of this method, we use line search (LS) and trust region (TR) algorithms. In this paper, we introduce a new approach to accelerate the computation of the implicit schemes by using mixed precision arithmetic, combining float and double precision, within the LS and TR algorithms, as well as in the Newton method. This approach aims at balancing the performance of lower precision arithmetic with the accuracy of higher precision arithmetic. We give theoretical results that show the efficiency of our approach. Numerical experiments show that our approach, running in either sequential or in parallel with MPI, is up to twice as fast as the double precision approach with the same level of accuracy. These experiments also show that increasing the size of the ODEs does not impact the quality of our mixed precision solution.
</FONT>

### *Bifurcation analysis of spontaneous flows in active nematic fluids*

<FONT size="2pt">
Marzorati A, Turzi S. Journal of Physics A: Mathematical and Theoretical. (2023 Jul)

<br> Continuum models of active nematic gels have proved successful to describe a number of biological systems consisting of a population of rodlike motile subunits in a fluid environment. One of the prominent features of active systems is their ability to sustain, above a critical threshold of the active parameter, an autonomous collective motion that results in a spontaneous flow of particles. In this paper we show that in a simple channel geometry, the characteristics of this spontaneous motion are largely independent of the model that is used to describe the dynamics of the active system, but are dictated by material symmetry. The natural symmetry for active nematics in a channel is found to be described by the Klein four-group $K_4 \simeq \mathbb{Z}_2 \times \mathbb{Z}_2$. We perform a Lyapunov–Schmidt reduction and an equivariant bifurcation analysis to show that the $K_4$-equivariance of the problem generically results in two pitchfork bifurcations with four solution branches.
</FONT>

### *Discrete maturity and delay differential-difference model of hematopoietic cell dynamics with applications to acute myelogenous leukemia*
<FONT size="2pt">

Adimy M, Chekroun A, El Abdllaoui A, Marzorati A. Journal of Biological Systems. (2022 Sep 5)

<br> In the last few years, many efforts were oriented towards describing the hematopoiesis phenomenon in normal and pathological situations. This complex biological process is organized as a hierarchical system that begins with primitive hematopoietic stem cells (HSCs) and ends with mature blood cells: red blood cells, white blood cells and platelets. Regarding acute myelogenous leukemia (AML), a cancer of the bone marrow and blood, characterized by a rapid proliferation of immature cells, which eventually invade the bloodstream, there is a consensus about the target cells during the HSCs development which are susceptible to leukemic transformation. We propose and analyze a mathematical model of HSC dynamics taking into account two phases in the cell cycle, a resting and a proliferating one, by allowing just after division a part of HSCs to enter the resting phase and the other part to come back to the proliferating phase to divide again. The resulting mathematical model is a system of nonlinear differential-difference equations. Due to the hierarchical organization of the hematopoiesis, we consider n stages of HSCs characterized by their maturity levels. We obtain a system of 2n nonlinear differential-difference equations. We study the existence, uniqueness, positivity, boundedness and unboundedness of the solutions. We then investigate the existence of positive and axial steady states for the system, and obtain conditions for their stability. Sufficient conditions for the global asymptotic stability of the trivial steady state as well as conditions for its instability are obtained. Using neutral differential equation associated to the differential-difference system, we also obtain results on the local asymptotic stability of the positive steady state. Numerical simulations are carried out to show the influence of variations of the differentiation rates and self-renewal coefficients of the HSCs on the behavior of the system. In particular, we show that a blocking of differentiation at an early stage of HSC development can lead in an overexpression of very immature cells. Such situation corresponds to the observation in the case of AML.
</FONT>
