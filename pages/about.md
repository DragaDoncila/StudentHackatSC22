---
title: About
permalink: /about/
---
# About

Computational research begins with an observation of a natural occurrence, then transitions to developing a model which mathematically describes that occurrence, to using advanced computing techniques to solve that model, then generating, verifying, and validating the data against observational data, and repeating the cycle: building and expanding, solving, generating, verifying and validating. The end goal is to build a system, accurately representing a scientific process, which you can run “what if” scenarios against when a real world experiment is not attainable.

It starts with a simple scientific process, using simple probability to get a “person” sick. Then expand that simple process into a computational model to simulate a disease propagating through a set population. Students will be broken into teams and given a set of challenges, requiring the teams to update and expand their computational models to meet.

# Presenters

<table>
<tr>
{% for person in site.presenters %}
    <td style="text-align: center;">
        <img src="{{ person.img | prepend: site.baseurl }}"><br>
        <strong>{{ person.name }}</strong> 
        {% for link in person.social %}
          {% if link.title == "envelope" %}
          <a href="{{ link.url }}">[<i class="fa fa-{{ link.title }}" style="font-size: 14px; padding: 2px; margin: 0px;"></i>]</a>
          {% else %}
          <a href="{{ link.url }}">[<i class="fab fa-{{ link.title }}" style="font-size: 14px; padding: 2px; margin: 0px;"></i>]</a>
          {% endif %}
        {% endfor %}
        <br>
        <a href="{{ person.url }}">{{ person.position }}</a>
    </td>
{% endfor %}
</tr>
</table>

