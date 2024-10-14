---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My current research focus on computing the Vlasov-Landau equation in kinetic plasma physics:

$$
\partial_t f + v \cdot \nabla_x f + (E + v \times B) \cdot \nabla_v f = \frac{1}{\varepsilon} Q(f, f) ,
$$

where $f=f(t,x,v)$ is the mass distribution function of charged particles in the phase space, such as electrons or ions. $E$ and $B$ represent the electric and magnetic fields, which can be prescribed or obtained self-consistently through the Maxwell's equation. The parameter $\varepsilon$ is the Knudsen number. When $\varepsilon \to 0$, one obtains the hydrodynamic limit Euler-Maxwell equation. The collision operator $Q(f,f)$ is known as the Landau / Fokker-Planck-Landau collision operator, and is defined by:

$$
Q(f,f) = \nabla_v \cdot \left\{ \int_{\mathbb{R}^{d_v}} |v-v_* |^{2+\gamma} \Pi(v-v_* ) [f(v_* )\nabla_v f(v) - f(v) \nabla_{v_* } f(v_* ) ] \mathrm{d}v_* \right\} ,
$$

where $\Pi(z)= I_{d_v} - \frac{z \otimes z}{\|z\|^2}$ denotes the projection into $$\\{ z \\}$$

The parameter $\gamma$ determines the type of interaction between particles. The most physical relevant case is $d_v =3, \gamma=-3$, which corrsponds to the Coulomb interaction is plasma.
