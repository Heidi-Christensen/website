---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

hello2

{% assign sorted_pubs = site.publications | sort: "date" %}
{% assign reversed_pubs = sorted_pubs | reversed %}

{% for post in reversed_pubs %}
  <div class="publication-entry" style="margin-bottom: 15px;">
    {{ post.content | markdownify }}
  </div>
{% endfor %}