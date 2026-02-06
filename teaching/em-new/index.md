<ul>
{% for file in site.static_files %}
  {% if file.path contains 'teaching/cm/' %}
    <li><a href="{{ file.path | relative_url }}">{{ file.name }}</a></li>
  {% endif %}
{% endfor %}
</ul>