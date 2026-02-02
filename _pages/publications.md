---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include sidebar.html %}

<p>A full list of my research output is available via <a href="https://scholar.google.com/citations?user=5ccB6BcAAAAJ&hl=en">Google Scholar</a>.</p>

{% comment %} 
  1. Group by year
  2. Sort the groups (names)
  3. Reverse to get the newest year first
{% endcomment %}
{% assign postsByYear = site.publications | group_by_exp: "post", "post.date | date: '%Y'" | sort: "name" | reversed %}

{% for year in postsByYear %}
  {% comment %} Sort items within the year by date descending {% endcomment %}
  {% assign yearItems = year.items | sort: "date" | reversed %}
  {% for post in yearItems %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
  
