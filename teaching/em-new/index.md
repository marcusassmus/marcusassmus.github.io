---
layout: null
---

<html>
<head>
    <meta charset="UTF-8">
    <style>
        body {
            font-family: monospace;
            font-size: 1.05em;
            color: #000;
            margin: 2rem auto;
            max-width: 800px;
            padding: 0 1rem;
        }
		ul {
            list-style-type: circle; 
            padding-left: 1.1em;     
        }
        a {
            color: #000;
            text-decoration: none;
        }
    </style>
</head>
<body>

<ul>
{% for file in site.static_files %}
  {% if file.path contains 'teaching/em-new/' and file.path != page.path %}
    <li><a href="{{ file.path | relative_url }}">{{ file.name }}</a></li>
  {% endif %}
{% endfor %}
</ul>

</body>
</html>