---
layout: default
title: Publications
permalink: /publications/
enable_maths: false
cv: false
---

<!-- ## Papers
<ul class="list">
    {% for paper in site.data.pubs.papers %}
    <li>{{ paper.author }}, <i>{{ paper.title }}</i>, {{ paper.journal }}, ({{ paper.year }}), {{ paper.doi }}</li>
    {% endfor %}
</ul> -->

## Posters
<ol class="publications-list" reversed>
    {% for poster in site.data.pubs.posters %}
        <li>
        {% assign authors = poster.authors | split: "," %}

        {% for auth in authors %}
            {% if forloop.last and authors.size > 1 %}
                and 
            {% endif %}
            {% if auth contains "Varnish" %}
                <b>{{ auth }}</b>,
            {% else %}
                {{ auth }},
            {% endif %}
        {% endfor %}

        <i>"{{ poster.title }}"</i>, {{ poster.conference }} ({{ poster.where }}, {{ poster.when }}).
        </li>
    {% endfor %}
</ol>
