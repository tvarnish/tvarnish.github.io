---
layout: default
title: Curriculum Vitae
page_title: CV
permalink: /cv/
enable_maths: false
cv: true
---

For more detailed descriptions, please see my [LinkedIn](https://linkedin.com/in/{{ site.author.linkedin }}) profile.

## Research Experience
<ul class="list">
    {% for position in site.data.cv.research %}
    <div class="cv-item">
        <div class="cv-item-header">
            <div> <b> {{ position.title }} </b> </div>
            <div> {{ position.when }} </div>
        </div>
        <div class="cv-item-content">
            <div> {{ position.where }} </div>
            {% if position.supervisors %}
            <div id="supervisors"> Supervisors: {{ position.supervisors }} </div>
            {% endif %}
            {% if position.project %}
            <div id="supervisors"> Project: <em>{{ position.project }}</em> </div>
            {% endif %}
        </div>
    </div>
    {% endfor %}
</ul>

## Education
<ul class="list">
    {% for school in site.data.cv.education %}
    <div class="cv-item">
        <div class="cv-item-header">
            <div> <b> {{ school.name }} </b> </div>
            <div> {{ school.when }} </div>
        </div>
        <div class="cv-item-content">
            <div> {{ school.what }} </div>
        </div>
    </div>
    {% endfor %}
</ul>

## Volunteering
<ul class="list">
    {% for position in site.data.cv.volunteering %}
    <div class="cv-item">
        <div class="cv-item-header">
            <div> <b> {{ position.name }} </b> </div>
            <div> {{ position.when }} </div>
        </div>
        <div class="cv-item-content">
            <div> {{ position.what }} </div>
        </div>
    </div>
    {% endfor %}
</ul>
