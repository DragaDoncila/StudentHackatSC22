---
title: Getting started with Designsafe-CI
tags: 
 - DesignSafe
description: >
  Instructions on how to log into Designsafe-CI, Copy the example code to your "My Data" folder, and Start a JupyterLab Session. 
---

# Getting Started

<table>
<tr>
  {% for step in site.data.jupyter.designsafe %}
    {% if step.anchor %}
    <td style="text-align: center;">
      <strong><a href="{{ site.baseurl}}/docs/getting-started/#{{ step.anchor }}" >{{ step.anchor }}</a></strong>
    </td>
    {% endif %}
  {% endfor %}
</tr>
</table>

<table>
{% for step in site.data.jupyter.designsafe %}

    {% if step.anchor %}
    <tr>
    <td>
      <h3 id="{{ step.anchor }}">{{ step.anchor }}</h3><br>
      {{ step.description }}
    </td>
   
      {% if step.image %}
       <td>
      <img src="{{ step.image | prepend: site.baseurl }}"> <br>
      </td>
      {% endif %}
      
    </tr>
    {% else %}
    <tr>
    <td>
    {% if step.description %}
    <br>  {{ step.description }}
    {% endif %}
    </td>
    
      {% if step.image %}
      <td>
      <img src="{{ step.image | prepend: site.baseurl }}"> 
      </td>
    {% endif %}
    
    
    </tr>
    {% endif %}
    
{% endfor %}
</table>
