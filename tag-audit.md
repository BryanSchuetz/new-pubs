---
title: Tag Audit
permalink: "/tag-audit/"
published: false
layout: tags
---

Here's all the tags currently being used on the site:  
<ul>
{% for tag in site.tags %}
  <li><a href="/tags/?tag={{ tag[0] | slugify}}">{{ tag[0] }}</a> <em>{% if tag[1].size == 1 %}<strong>(being used on {{ tag.[1]size }} posts)</strong>{% else %}(being used on {{ tag.[1]size }} posts){% endif %}</em></li>
{% endfor %}
</ul>

Here are the tags being used to connect content across the Pubs/Digital/dai.com sites:
<ul>
  <li><strong>Sustainable Business</strong></li>
  <li><strong>Digital Acceleration</strong></li>
  <li><strong>Economic Growth</strong></li>
  <li><strong>Environment & Energy</strong></li>
  <li><strong>Governance</strong></li>
  <li><strong>Health</strong></li>
  <li><strong>Stability</strong></li>
</ul>
