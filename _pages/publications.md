---
layout: page
title: publications
permalink: /_publications/
description: 
years: [Forthcoming, 2019, 2018, 2017, 2016]
---

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

