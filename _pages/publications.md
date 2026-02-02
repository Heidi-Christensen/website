---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
{% include base_path %}

<div class="archive">
  <p>A full list of research outputs. Also available via <a href="https://scholar.google.com/citations?user=5ccB6BcAAAAJ">Google Scholar</a>.</p>

  {% comment %} 
    This loop goes through every paper and prints the 'content' 
    (the full text from your works.md) instead of just a link.
  {% endcomment %}
  
  {% for post in site.publications %}
    <div class="publication-item" style="margin-bottom: 20px; border-bottom: 1px solid #eee; padding-bottom: 10px;">
      {{ post.content | markdownify }}
    </div>
  {% endfor %}

</div>
