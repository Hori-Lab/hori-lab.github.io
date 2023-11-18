---
title: "Hori Lab - Publications"
layout: gridlay
excerpt: "Hori Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Recent highlights

(For a full list of publications see [below](#full-list-of-publications) or go to [Google Scholar](https://scholar.google.com/citations?user=Je_SISQAAAAJ))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>

  {% if publi.youtube != nil %}
  <iframe width="400" height="200" src="{{ publi.youtube }}" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  {% else %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  {% endif %}

  <p>{{ publi.description }}</p>

  <p><em>{{ publi.authors }}</em> <br/>
  <strong><a href="{{ publi.link.url }}" target="_blank">{{ publi.link.display }}</a></strong> <br/>
  {{ publi.news2 }}</p>
  <!-- <p class="text-danger"><strong> {{ publi.news1 }}</strong></p> -->
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

<!--
## Patents
-->

## Full list of publications

<ol reversed>
{% for publi in site.data.publist %}

  <li>
  {{ publi.title }} <br />
  <em> {{ publi.authors }} </em><br />
  <a href="{{ publi.link.url }}" target="_blank">{{ publi.link.display }}</a>
  {% if publi.link2.flag == 1 %}
  &nbsp;&nbsp;&nbsp;<a href="{{ publi.link2.url }}" target="_blank">{{ publi.link2.display }}</a>
  {% endif %}
  </li>

{% endfor %}
</ol>
