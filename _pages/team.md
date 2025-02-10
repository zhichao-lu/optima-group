---
title: "Allan Lab - Team"
layout: gridlay
excerpt: "Allan Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

 **We are always looking for self-motivated students with strong mathematical and programming background** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

## Principal Investigators
{% assign number_printed = 0 %}
{% for member in site.data.team_member_PIs %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <a href="{{ member.url }}" target="_blank" rel="noopener noreferrer"><img 
    src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" 
        width="25%" style="float: left" /></a>
  <h4><a href="{{ member.url }}" target="_blank" rel="noopener noreferrer">{{ member.name }}</a></h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

  {% if member.number_topic == 1 %}
  <li> {{ member.topic1 }} </li>
  {% endif %}

  {% if member.number_topic == 2 %}
  <li> {{ member.topic1 | markdownify}} </li>
  <li> {{ member.topic2 | markdownify}} </li>
  {% endif %}

  {% if member.number_topic == 3 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  {% endif %}

  {% if member.number_topic == 4 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  <li> {{ member.topic4 }} </li>
  {% endif %}

  {% if member.number_topic == 5 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  <li> {{ member.topic4 }} </li>
  <li> {{ member.topic5 }} </li>
  {% endif %}

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


## Postdoc Research Fellows
{% assign number_printed = 0 %}
{% for member in site.data.team_member_postdocs %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <a href="{{ member.url }}" target="_blank" rel="noopener noreferrer"><img 
    src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" 
        width="25%" style="float: left" /></a>
  <h4><a href="{{ member.url }}" target="_blank" rel="noopener noreferrer">{{ member.name }}</a></h4>

[//]: # (  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->)
  <ul style="overflow: hidden">

{% if member.number_topic == 1 %}
  <li> {{ member.topic1 }} </li>
  {% endif %}

{% if member.number_topic == 2 %}
  <li> {{ member.topic1 | markdownify}} </li>
  <li> {{ member.topic2 | markdownify}} </li>
  {% endif %}

{% if member.number_topic == 3 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  {% endif %}

{% if member.number_topic == 4 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  <li> {{ member.topic4 }} </li>
  {% endif %}

{% if member.number_topic == 5 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  <li> {{ member.topic4 }} </li>
  <li> {{ member.topic5 }} </li>
  {% endif %}

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


## PhD Students
{% assign number_printed = 0 %}
{% for member in site.data.team_member_PhDs %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <a href="{{ member.url }}" target="_blank" rel="noopener noreferrer"><img 
    src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" 
        width="25%" style="float: left" /></a>
  <h4><a href="{{ member.url }}" target="_blank" rel="noopener noreferrer">{{ member.name }}</a></h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

{% if member.number_topic == 1 %}
  <li> {{ member.topic1 }} </li>
  {% endif %}

{% if member.number_topic == 2 %}
  <li> {{ member.topic1 | markdownify}} </li>
  <li> {{ member.topic2 | markdownify}} </li>
  {% endif %}

{% if member.number_topic == 3 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  {% endif %}

{% if member.number_topic == 4 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  <li> {{ member.topic4 }} </li>
  {% endif %}

{% if member.number_topic == 5 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  <li> {{ member.topic4 }} </li>
  <li> {{ member.topic5 }} </li>
  {% endif %}

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


## MPhil Students
{% assign number_printed = 0 %}
{% for member in site.data.team_member_MPhils %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <a href="{{ member.url }}" target="_blank" rel="noopener noreferrer"><img 
    src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" 
        width="25%" style="float: left" /></a>
  <h4><a href="{{ member.url }}" target="_blank" rel="noopener noreferrer">{{ member.name }}</a></h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

{% if member.number_topic == 1 %}
  <li> {{ member.topic1 }} </li>
  {% endif %}

{% if member.number_topic == 2 %}
  <li> {{ member.topic1 | markdownify}} </li>
  <li> {{ member.topic2 | markdownify}} </li>
  {% endif %}

{% if member.number_topic == 3 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  {% endif %}

{% if member.number_topic == 4 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  <li> {{ member.topic4 }} </li>
  {% endif %}

{% if member.number_topic == 5 %}
  <li> {{ member.topic1 }} </li>
  <li> {{ member.topic2 }} </li>
  <li> {{ member.topic3 }} </li>
  <li> {{ member.topic4 }} </li>
  <li> {{ member.topic5 }} </li>
  {% endif %}

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


## Alumni

<div class="row">
<div class="col-sm-12 clearfix">
{% for member in site.data.alumni_members %}
<a href="{{ member.url }}" target="_blank" rel="noopener noreferrer">{{ member.name }}</a>, {{ member.affiliation }}
{% endfor %}
</div>
</div>


## Former visitors, BSc/ MSc students
<div class="row">

<div class="col-sm-4 clearfix">
<h4>Visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Postgraduate students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Bachelor students</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>
