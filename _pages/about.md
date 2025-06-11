---
permalink: /
title: "Julius Erbach"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Ph.D. candidate in the Center for Learning Systems under the supervision of Prof. Konrad Schindler and Prof. Bernt Schiele.
I am interested in the use of Probabilistic Generative Models like Diffusion Models for computational photography and 3D modeling. Particularly, I want to investigate how to efficiently re-use priors which are incorporated in Foundation models for new applications like inverse problems.

## Publications

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
