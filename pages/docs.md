---
layout: page
title: Documentation
permalink: /docs/
---

# Documentation

Welcome to the {{ site.title }} Documentation pages! Here you can quickly jump to a 
particular page.

<div class="section-index">
    <hr class="panel-line">
    <h2>Documents: </h2>
    {% for post in site.docs  %}        
    <div class="entry">
    <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
    <p>{{ post.description }}</p>
    {% if post.title == "Getting started with Designsafe-CI" %}
        <h5>Jump to Topic: </h5>
        <ul>
        {% for step in site.data.jupyter.designsafe %}
        {% if step.anchor %}
        <li>
            <strong ><a href="{{ site.baseurl}}/docs/getting-started/#{{ step.anchor }}" style="color: darkgreen;">{{ step.anchor }}</a></strong>
        </li>
        {% endif %}
        {% endfor %}
    </ul>
    {% endif %}
    </div>
    {% endfor %}

    <h2> Helpful Links: </h2>
    <ul>
        {% for link in site.data.jupyter.helpfullinks %}
        <li>
           <strong>{{ link.name }}</strong> - <a href="{{ link.url }}" target="_blank">{{ link.url }} </a>
        </li>

        {% endfor %}
    <ul>

