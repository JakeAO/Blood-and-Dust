---
layout: page
title: Sessions
description: Session summaries and campaign chronicle
permalink: /sessions/
---

Below are session summaries documenting the gladiators' battles in the Grand Arena of Obusia, ordered chronologically.

{% assign items = site.sessions | sort: 'index' %}

{% if items.size > 0 %}
<ul>
{% for doc in items %}
  <li><strong>Session {{ doc.index }}:</strong> <a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% else %}
<p><em>No sessions have been recorded yet. The arena awaits its champions!</em></p>
{% endif %}

---

*Summaries are added after each session to track the gladiators' victories, defeats, and survival.*
