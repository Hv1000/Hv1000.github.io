---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research focuses on computing the fundamental equation in kinetic plasma physics---the Vlasov-Landau equation:

$$ \partial_t f + v \cdot \nabla_x f + (E + v \times B) \cdot \nabla_v f = \frac{1}{\varepsilon} Q(f, f) , $$

where $f=f(t,x,v)$ is the mass distribution function of charged particles in the phase space, such as electrons or ions. $E$ and $B$ represent the electric and magnetic fields, which can be prescribed or obtained self-consistently through the Maxwell's equation. The parameter $\varepsilon$ is the Knudsen number describing the collision strength. When $\varepsilon \to 0$, one obtains the hydrodynamic limit Euler-Maxwell equation. The collision operator $Q(f,f)$ is known as the Landau / Fokker-Planck-Landau operator, and is defined by:

$$ Q(f,f) = \nabla_v \cdot \left\{ \int_{\mathbb{R}^{d_v}} A(v-v_* ) [f(v_* )\nabla_v f(v) - f(v) \nabla_{v_* } f(v_* ) ] \mathrm{d}v_* \right\} , $$

where the collision kernel
$$A(z)= |z|^{2+\gamma} \left(I_{d_v} - \frac{z \otimes z}{ |z|^2 }\right) $$. The parameter $\gamma$ determines the type of interaction between particles. In the case of inverse power law, i.e., when two particles at distance $r$ interact with a force propotional to $$\frac{1}{r^s}$$, $\gamma=\frac{s-5}{s-1}$. The most physically relevant case is $\gamma=-3$, which corresponds to the Coulomb interaction ($s=2$). 

Solving the Vlasov-Landau equation presents significant challenges, primarily due to its high dimensionality, mutilple scales, strong nonlinearity and non-locality. On the other hand, deep learning has progressively transformed the numerical computation of partial differential equations by leveraging neural networks' ability to approximate high-dimensional functions and the powerful optimization toolbox. However, straightforward application of deep learning to compute PDEs often encounters training difficulties and leads to a loss of physical fidelity. Therefore, I aim to develop methods that elegantly combines learning with both asymptotic-preserving and structure-preserving numerical schemes.

In my first paper [1](https://arxiv.org/abs/2409.12296), we propose a score-based particle method for the spatially homogeneous Landau equation. Our main concept is to rewrite the Landau operator into log form

$$ Q(f,f) = \nabla \cdot \left\{ \int_{\mathbb{R}^{d_v}} A(v-v_* ) [\nabla \log f - \nabla_{* } \log f_* ]f f_* \mathrm{d}v_* \right\} , $$

and recognize $\nabla \log f$ as score function. Then it can be efficiently learned from particle data by the score-matching technique widely used in the deep generative models. This method is not only structure-preserving but also significantly faster than the deterministic particle method, making it promising for solving the Vlasov-Landau equation where a large number of particles are commonly needed. 

In my second paper [2](https://arxiv.org/abs/2405.05187), we introduce a variational particle method by leveraging the gradient flow structure of the homogeneous Landau equation w.r.t entropy $$ \mathcal{H}(f) = \int_{\mathbb{R}^{d_v}} f \log f \mathrm{d}v $$. The gradient flow structure enables us to develop a solution using the seminal Jordan-Kinderlehrer-Otto (JKO) scheme,

$$\inf_{f, u} \frac{1}{2} \int_0^1 \iint_{\mathbb{R}^{2d}} |u-u_*  |^2_A f f_* \mathrm{d}v \mathrm{d}v_* \mathrm{d}t + 2\Delta t \mathcal{H}(f(1, \cdot)) , $$

$$ s.t. \quad \partial_t f = \nabla \cdot \left[ f \left( \int_{\mathbb{R}^d} A(v-v_* ) ( u-u_* ) f_* \mathrm{d}v_* \right) \right] , f(0, \cdot) = f^n , $$

        
which guarantees desirable exact entropy dissipation and unconditional stability that are lacking in both deterministic and score-based particle methods. Therefore, this approach is suitable for plasma simulations over large-scale time periods.


