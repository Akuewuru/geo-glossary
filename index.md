---
layout: default
title: Glossary Index
---

# GeoLedger Glossary

Click a term to view its definition.

{% assign alpha = "ABCDEFGHIJKLMNOPQRSTUVWXYZ" | split: "" %}
{% for letter in alpha %}
## {{ letter }}

{% assign terms_for_letter = site.terms | where_exp:"t","t.title | slice:0,1 | upcase == letter" | sort:"title" %}
{% if terms_for_letter != empty %}
<ul>
  {% for term in terms_for_letter %}
  <li><a href="{{ term.url | relative_url }}">{{ term.title }}</a></li>
  {% endfor %}
</ul>
{% else %}
_No terms yet._
{% endif %}

{% endfor %}
