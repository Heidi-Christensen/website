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
  {% for post in year.items %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}