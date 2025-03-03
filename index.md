markdown
layout: default
title: Home
Welcome to my site! Here are all my pages:
<ul>
{% for page in site.pages %}
  {% if page.path contains '.md' and page.layout == 'default' and page.path != 'index.md' %}
    <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

