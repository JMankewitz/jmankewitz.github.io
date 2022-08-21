---
layout: page
permalink: /publications/
title: publications
years: [2022, 2021]
paper_years: [2022]
proceedings_years: [2021]
pres_years: [2022, 2021]
categories: [conference proceedings]
nav: true
---

<div class="publications">
<p><em>* indicates equal contribution</em></p>

<h4 class="category"> Preprints</h4>
<h2 class="year">{{"Under Review"}}</h2>
  {% bibliography -f preprints%}

<div class="publications">
<h4 class="category"> Journal Papers and Articles</h4>
{% for y in page.paper_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
</div>

<h4 class="category"> Peer-reviewed Conference Proceedings</h4>
{% for y in page.proceedings_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f conf-proceedings -q @*[year={{y}}]* %}
{% endfor %}

</div>

<div class="publications">
<h4 class="category"> Peer-reviewed Conference Presentations</h4>
{% for y in page.pres_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f conference-presentations -q @*[year={{y}}]* %}
{% endfor %}
</div>
