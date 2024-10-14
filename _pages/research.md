---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research focuses on computing the fundamental equation in kinetic plasma physics---the Vlasov-Landau equation:

$$ \partial_t f + v \cdot \nabla_x f + (E + v \times B) \cdot \nabla_v f = \frac{1}{\varepsilon} Q(f, f) , $$

where $f=f(t,x,v)$ is the mass distribution function of charged particles in the phase space, such as electrons or ions. $E$ and $B$ represent the electric and magnetic fields, which can be prescribed or obtained self-consistently through the Maxwell's equation. The parameter $\varepsilon$ is the Knudsen number describing the collision strength. When $\varepsilon \to 0$, one obtains the hydrodynamic limit Euler-Maxwell equation. The collision operator $Q(f,f)$ is known as the Landau / Fokker-Planck-Landau collision operator, and is defined by:

$$ Q(f,f) = \nabla_v \cdot \left\{ \int_{\mathbb{R}^{d_v}} |v-v_* |^{2+\gamma} \Pi(v-v_* ) [f(v_* )\nabla_v f(v) - f(v) \nabla_{v_* } f(v_* ) ] \mathrm{d}v_* \right\} , $$

where 
$$\Pi(z)= I_{d_v} - \frac{z \otimes z}{ |z|^2 } $$
denotes the projection into the orthogonal complement of $$\left\{ z \right\}$$. The parameter $\gamma$ determines the type of interaction between particles. In the case of inverse power law, i.e., when two particles at distance $r$ interact with a force propotional to $$\frac{1}{r^s}$$, $\gamma=\frac{s-5}{s-1}$. The most physically relevant case is $\gamma=-3$, which corresponds to the Coulomb interaction ($s=2$). 

Solving the Vlasov-Landau equation presents significant challenges, primarily due to its high dimensionality, as it lives in a six-dimensional phase space. Besides, the strong nonlinearity, non-locality and mutilple scales of the Landau collision operator $Q(f,f)$ further complicate the problem. Finally, the numerical solution must be structure-preserving, meaning it should maintain the conservation of mass, momentum, and energy, while also ensuring entropy dissipation. Given these challenges, most existing research approaches the Vlasov-Landau equation in isolation, typically focusing on either the collisionless Vlasov-type equation or the spatial homogeneous Landau equation. For the Vlasov-type equation, the particle-in-cell (PIC) method being the most popular. However, relatively few methods have been developed for solving the Landau equation. Among these limited approaches, the deterministic particle method integrates seamlessly with PIC, offering a promising tool for tackling the Vlasov-Landau equation. However, a major bottleneck is its poor scalability with increasing dimensionality.


In my first paper \cite{huang2024scorebasedparticlemethodhomogeneous}, we introduce a score-based particle method for the homogeneous Landau equation, combining structure-preserving particle methods with the score-matching technique, which is popular in generative artificial intelligence. Our method is not only structure-preserving and accurate but also significantly faster than the deterministic particle method, making it promising for solving the Vlasov-Landau equation where a large number of particles are commonly needed. 

In real plasma simulations, the stability of numerical algorithms is crucial. To achieve this, in my second paper \cite{huang2024jkolandauvariationalparticle}, we introduce a variational particle method by leveraging the non-trivial gradient flow structure of the homogeneous Landau equation. The gradient flow structure enables us to develop a solution using the seminal Jordan-Kinderlehrer-Otto (JKO) scheme, which guarantees desirable exact entropy dissipation and unconditional stability that are lacking in both deterministic and score-based particle methods. In addition, we also design a tailored stochastic optimization algorithm to further reduce computational cost. Therefore, this approach is suitable for plasma simulations over large-scale time periods.


