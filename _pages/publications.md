---
layout: archive
title: "Publications"
permalink: /publication/
author_profile: true
---


### Preprints:
[2] JKO for Landau: a variational particle method for homogeneous Landau equation (with Li Wang). [arXiv](https://arxiv.org/abs/2409.12296)

[1] A score-based particle method for homogeneous Landau equation (with Li Wang). [arXiv](https://arxiv.org/abs/2405.05187)



{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
