---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<div class="archive">
  {% comment %} 
    Sort by date and then reverse to put newest at the top.
    We remove the 'border' style if you want a truly plain listing.
  {% endcomment %}
  
  {% assign sorted_pubs = site.publications | sort: 'date' | reversed %}

  {% for post in sorted_pubs %}
    <div class="publication-entry" style="margin-bottom: 15px;">
      {{ post.content | markdownify }}
    </div>
  {% endfor %}
</div>

