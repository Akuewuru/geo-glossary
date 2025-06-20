---
layout: default
title: Geo Glossary
---

# Geo Glossary A–Z

{% if site.terms %}
<ul>
  {% assign sorted_terms = site.terms | sort: 'title' %}
  {% for term in sorted_terms %}
    <li><a href="{{ term.url }}">{{ term.title }}</a></li>
  {% endfor %}
</ul>
{% else %}
<p>No glossary terms found yet. Please check back later.</p>
{% endif %}
