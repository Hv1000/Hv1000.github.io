---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My current research focuses on computing the fundamental equation in kinetic plasma physics---the Vlasov-Landau equation:

$$ \partial_t f + v \cdot \nabla_x f + (E + v \times B) \cdot \nabla_v f = \frac{1}{\varepsilon} Q(f, f) , $$

where $f=f(t,x,v)$ is the mass distribution function of charged particles in the phase space, such as electrons or ions. $E$ and $B$ represent the electric and magnetic fields, which can be prescribed or obtained self-consistently through the Maxwell's equation. The parameter $\varepsilon$ is the Knudsen number describing the collision strength. When $\varepsilon \to 0$, one obtains the hydrodynamic limit Euler-Maxwell equation. The collision operator $Q(f,f)$ is known as the Landau / Fokker-Planck-Landau collision operator, and is defined by:

$$ Q(f,f) = \nabla_v \cdot \left\{ \int_{\mathbb{R}^{d_v}} |v-v_* |^{2+\gamma} \Pi(v-v_* ) [f(v_* )\nabla_v f(v) - f(v) \nabla_{v_* } f(v_* ) ] \mathrm{d}v_* \right\} , $$

where 
$$\Pi(z)= I_{d_v} - \frac{z \otimes z}{ |z|^2 } $$
denotes the projection into the orthogonal complement of $$\left\{ z \right\}$$. The parameter $\gamma$ determines the type of interaction between particles. In the case of inverse power law, i.e., when two particles at distance $r$ interact with a force propotional to $$\frac{1}{r^s}$$, $\gamma=\frac{s-5}{s-1}$. The most physically relevant case is $\gamma=-3$, which corresponds to the Coulomb interaction ($s=2$).


