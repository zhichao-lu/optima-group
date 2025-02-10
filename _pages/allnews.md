---
title: "News"
layout: gridlay
excerpt: "Optima Group -- News"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<strong>{{ article.date }}</strong> <br /> 
{{ article.headline | markdownify}}
{% if article.image != '' %}
<p><img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image }}" class="img-responsive" width="33%"/></p>
{% endif %}
<br />
{% endfor %}
