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
            list-style-type: disc;  
            padding-left: 1.5em;  
            margin: 1em 0;
        }
        li {
            margin: 0.5em 0;   
            line-height: 1.4;
        }
        a {
            color: #000;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
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