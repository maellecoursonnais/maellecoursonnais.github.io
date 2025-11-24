---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}


* **Lecoursonnais, M.**, Brandén, M., & Rosenqvist, E. (2025). The Spatial Determinants of Academic Aspirations: Evidence From Sweden. Population, Space and Place, 31(6), e70082, <https://doi.org/10.1002/psp.70082>.
* **Lecoursonnais, M.** (2025). Places of influence: The lasting imprint of where we grow up (Doctoral dissertation, Linköping University Electronic Press), <https://doi.org/10.3384/9789181180510>.


<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}



