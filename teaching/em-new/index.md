---
layout: null
---
<ul>
{% for file in site.static_files %}
  {% if file.path contains 'teaching/em-new/' and file.path != page.path %}
    <li><a href="{{ file.path | relative_url }}">{{ file.name }}</a></li>
  {% endif %}
{% endfor %}
</ul>