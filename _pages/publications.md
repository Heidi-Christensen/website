---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

HELLO2

{% include base_path %}

<div class="archive">
  {% assign sorted_pubs = site.publications | sort: "sort_key" | reversed %}

  {% for post in sorted_pubs %}
    <div class="publication-entry" style="margin-bottom: 15px;">
      {{ post.content | markdownify }}
    </div>
  {% endfor %}
</div>
