---
layout: page
permalink: /publications/
title: publications
years: [2026, 2025, 2024, 2023, 2022, 2021]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  {%- capture n %}{% bibliography_count -f papers -q @*[year={{y}}]* %}{% endcapture %}
  {%- if n != "0" %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
  {%- endif %}
{% endfor %}

</div>
