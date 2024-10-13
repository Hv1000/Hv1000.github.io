---
permalink: /
title: ""
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I'm a second year mathematics Ph.D. student at the [University of Minnesota, Twin Cities](https://twin-cities.umn.edu/) advised by [Prof. Li Wang](https://liwang-umn.github.io/math/). I obtained my B.S. in Mathematics and Applied Mathematics at the [Southern University of Science and Technology](https://www.sustech.edu.cn/en/). Here is my [CV](https://hv1000.github.io/files/Yan_HUANG_CV.pdf).

My general research interests lie in Numerical Solutions for Kinetic Equations, Gradient Flows, Optimal Transport, Mean-field Limits and Scientifc Machine Learning. 

My current research focus on the Vlasov-Landau equation in kinetic plasma physics:

$$
\partial_t f + v \cdot \nabla_x f + (E + v \times B) \cdot \nabla_v f = \frac{1}{\varepsilon} Q(f, f) ,
$$

where $f=f(t,x,v)$ is the mass distribution function of charged particles in the phase space, such as electrons or ions. $E$ and $B$ represent the electric and magnetic fields, which can be prescribed or obtained self-consistently through the Maxwell's equation. $\varepsilon$ is the Knudsen number defined as the ratio of mean free path and the typical length scale. The collision operator $Q(f,f)$ is referred to as the Landau / Fokker-Planck-Landau collision operator, and is defined by

$$
Q(f,f)= \nabla_v \cdot \left( \int_{\mathbb{R}^{d_v}} |v-v_* |^{2+\gamma} \Pi(v-v_* ) [f(v_* )\nabla_v f(v) -  f(v) \nabla_{v_* } f(v_* ) ] \mathrm{d}v_* \right)
$$

Here $\gamma$ determines the type of interaction between particles. The most physical relevant case is $d_v =3, \gamma=-3$, which corrsponds to the Coulomb interaction is plasma.

