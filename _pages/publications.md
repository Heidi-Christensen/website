---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---


{% include base_path %}

<div class="archive">
  
  {% capture my_publications %}{% include_relative works.md %}{% endcapture %}
  {{ my_publications | markdownify }}

</div>