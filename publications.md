---
layout: default
title: Publications
permalink: /publications/
enable_maths: false
cv: false
---

## Papers
<ol class="publications-list" reversed>
    {% for paper in site.data.pubs.papers %}
        <li>
        {% assign authors = paper.authors | split: "," %}

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

        <b><i>"{{ paper.title }}"</i></b>, {{ paper.journal }} ({{ paper.year }}){% if paper.doi %}, <a href="{{ paper.link }}">doi:{{ paper.doi }}</a>{% endif %}.
        </li>
    {% endfor %}
</ol>
