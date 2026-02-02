---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% if page.author and site.data.authors[page.author] %}
  {% assign author = site.data.authors[page.author] %}{% else %}{% assign author = site.author %}
{% endif %}

<div id="main" role="main">
  {% include sidebar.html %}

  <div class="archive">
    <h1 class="page__title">{{ page.title }}</h1>
    
    <p>A full list of my research output is available via <a href="https://scholar.google.com/citations?user=5ccB6BcAAAAJ&hl=en">Google Scholar</a>.</p>

    {% comment %} Sort the publications collection by date, newest first {% endcomment %}
    {% assign entries = site.publications | sort: 'date' | reversed %}

    {% for post in entries %}
      {% include archive-single.html %}
    {% endfor %}
  </div>
</div>