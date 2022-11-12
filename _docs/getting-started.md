---
title: Getting Started
tags: 
 - DesignSafe
description: Getting started with Designsafe-CI
---

# Getting Started
<table>
{% for step in site.data.jupyter.designsafe %}
  <tr>
  {% if step.image %}
    <td><img src="{{ step.image | prepend: site.baseurl }}"> </td>
  {% endif %}
  {% if step.description %}
   <td> {{ step.description }} </td>
  {% endif %}
  </tr>
{% endfor %}
</table>
