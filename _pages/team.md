---
title: "Hori Lab - Team"
layout: gridlay
excerpt: "Hori Lab: Team members"
sitemap: false
permalink: /team/
---

<!-- **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!** -->


# Members

{% assign number_printed = 0 %}
{% for member in site.data.members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />

  <h4>{{ member.name }} </h4>

  {{ member.info }}
  {% if member.email %} <br> email: {{ member.email }}{% endif %}
  {% if member.googlescholar %} <br>
    <a href="{{ member.googlescholar }}" target="_blank">
    <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Google_Scholar_logo.png" 
    alt="Google Scholar" height="16" 
    style="box-shadow: none; border-radius: 0; margin: 0; vertical-align: middle;">
    </a>
    {% if member.orcid %} &ensp;
      <a href="https://orcid.org/{{ member.orcid }}" target="_blank">
      <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/orcid-logo.webp" 
      alt="ORCID" height="16" 
      style="box-shadow: none; border-radius: 0; margin: 0; vertical-align: middle;">
      </a>
    {% endif %}
  {% elsif member.orcid %} <br>
    <a href="https://orcid.org/{{ member.orcid }}" target="_blank">
    <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/orcid-logo.webp" 
    alt="ORCID" height="16" 
    style="box-shadow: none; border-radius: 0; margin: 0; vertical-align: middle;">
    </a>
  {% endif %}

  <ul style="overflow: hidden">

  {% if member.bullet1 %}<li> {{ member.bullet1 }} </li>{% endif %}
  {% if member.bullet2 %}<li> {{ member.bullet2 }} </li>{% endif %}
  {% if member.bullet3 %}<li> {{ member.bullet3 }} </li>{% endif %}
  {% if member.bullet4 %}<li> {{ member.bullet4 }} </li>{% endif %}
  {% if member.bullet5 %}<li> {{ member.bullet5 }} </li>{% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


### Former members

{% assign number_printed = 0 %}
{% for member in site.data.alumni %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />

  <h4>{{ member.name }} </h4>

  {{ member.info }}
  {% if member.email %} <br> email: {{ member.email }}{% endif %}
  {% if member.googlescholar %} <br>
    <a href="{{ member.googlescholar }}" target="_blank">
    <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Google_Scholar_logo.png" 
    alt="Google Scholar" height="16" 
    style="box-shadow: none; border-radius: 0; margin: 0; vertical-align: middle;">
    </a>
    {% if member.orcid %} &ensp;
      <a href="https://orcid.org/{{ member.orcid }}" target="_blank">
      <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/orcid-logo.webp" 
      alt="ORCID" height="16" 
      style="box-shadow: none; border-radius: 0; margin: 0; vertical-align: middle;">
      </a>
    {% endif %}
  {% elsif member.orcid %} <br>
    <a href="https://orcid.org/{{ member.orcid }}" target="_blank">
    <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/orcid-logo.webp" 
    alt="ORCID" height="16" 
    style="box-shadow: none; border-radius: 0; margin: 0; vertical-align: middle;">
    </a>
  {% endif %}

  <ul style="overflow: hidden">

  {% if member.bullet1 %}<li> {{ member.bullet1 }} </li>{% endif %}
  {% if member.bullet2 %}<li> {{ member.bullet2 }} </li>{% endif %}
  {% if member.bullet3 %}<li> {{ member.bullet3 }} </li>{% endif %}
  {% if member.bullet4 %}<li> {{ member.bullet4 }} </li>{% endif %}
  {% if member.bullet5 %}<li> {{ member.bullet5 }} </li>{% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

