---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---


{% include base_path %}

{% comment %} Group by year and sort descending {% endcomment %}
{% assign postsByYear = site.publications | group_by_exp: "post", "post.date | date: '%Y'" | sort: "name" | reversed %}

{% for year in postsByYear %}
  <! -- <h2 id="{{ year.name }}" class="archive__subtitle">{{ year.name }}</h2> -->
  {% for post in year.items %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}