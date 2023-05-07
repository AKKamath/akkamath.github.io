---
layout: archive
title: "Notable publications"
permalink: /publications/
author_profile: true
---
{% if site.author.googlescholar %}
  You can find a full list of articles on my <a href="{{site.author.googlescholar}}">Google Scholar profile</a>.
  <p class="divider__line"></p>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
