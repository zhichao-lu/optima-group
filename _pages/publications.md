---
title: "Optima Group - Publications"
layout: gridlay
excerpt: "Optima Group -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

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
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
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


## Selected List of publications
**Full list of papers are available on [CityU Scholars](https://scholars.cityu.edu.hk/en/persons/qingfu-zhang(a25373cf-62a1-4697-ad08-43678bcbf3f2)/publications.html).**

#### **Journal**
{% for publi in site.data.journallist %}

<a href="{{ publi.link.url }}"><strong>{{ publi.title }}</strong></a> <br />
  <em>{{ publi.authors }} </em><br />{{ publi.link.display }}

{% endfor %}

#### **Conference**
{% for publi in site.data.conferencelist %}

<a href="{{ publi.link.url }}"><strong>{{ publi.title }}</strong></a> <br />
<em>{{ publi.authors }} </em><br />{{ publi.link.display }}

{% endfor %}