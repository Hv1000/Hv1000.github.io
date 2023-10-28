---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---
## Research Interests
Numercial Methods for Kinetic Equations

Gradient Flows, Optimal Transport

Scientific Machine Learning, Deep Learning Theory

## Research Projects
1.Acceleration of Variable Frequency Fourier Transform, SUSTech, Summer 2022 
- Developed an acceleration algorithm for computing variable frequency Fourier transform with Prof. Zhen Zhang. 



{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
