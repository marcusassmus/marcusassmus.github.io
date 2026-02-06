---
layout: null
---
<ul>
{% for file in site.static_files %}
  {% if file.path contains 'teaching/em-new/' %}
    {% unless file.name contains '.' or file.name == 'index.md' %}
      <li><a href="{{ file.path | relative_url }}">{{ file.name }}</a></li>
    {% endunless %}
  {% endif %}
{% endfor %}
</ul>