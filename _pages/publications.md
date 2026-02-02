---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

Hello

{% include base_path %}


{% assign sorted_pubs = site.publications | sort: "date" %}
{% assign reversed_pubs = sorted_pubs | reversed %}

{% for post in reversed_pubs %}
  <div class="publication-entry" style="margin-bottom: 15px;">
    {{ post.content | markdownify }}
  </div>
{% endfor %}