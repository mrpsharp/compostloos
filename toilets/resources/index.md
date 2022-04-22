---
layout: page
title: Resources
nav_order: 4
parent: Composting Toilets
---
## Other Resources

These files include those that are linked elsewhere 

{% assign files = "" | split: "," %}
{% for file in site.static_files %}
    {% if file.path contains page.dir  %}
        {% unless file.path contains "assets" %}
            {% assign files = files | push: file %}
        {% endunless %}
    {% endif %}
{% endfor %}
{% if files.size > 0 %}
{% for file in files %}* [{{ file.basename | replace: "_"," " }}]({{ file.path }}) 
{% endfor %}
{% endif %}