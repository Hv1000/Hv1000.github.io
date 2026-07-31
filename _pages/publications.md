---
layout: archive
title: "Publications"
permalink: /publication/
author_profile: true
---


### Preprints:
[1] Asymptotic-preserving deterministic particle methods for collisional plasma models (with Li Wang), [arXiv](https://arxiv.org/abs/2604.09484)

### Journals:
[2] [JKO for Landau: a variational particle method for homogeneous Landau equation](https://academic.oup.com/imajna/advance-article-abstract/doi/10.1093/imanum/drag041/8746121) (with Li Wang), IMA Journal of Numerical Analysis, 2026.

[1] [A score-based particle method for homogeneous Landau equation](https://doi.org/10.1016/j.jcp.2025.114053) (with Li Wang), Journal of Computational Physics, 2025. 



{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
