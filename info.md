---
layout: page
title: Rules & Info
description: Mythras Imperative rules, mechanics, and resources
permalink: /info/
---

This page contains player-facing rules clarifications, reference sheets, and game mechanics for the Blood & Dust campaign.

## Core Resources

- **[Mythras Imperative PDF](https://www.thedesignmechanism.com/resources/Mythras%20Imperative.pdf)** – Free core rules from The Design Mechanism
- **[Mythras Resources](https://www.thedesignmechanism.com/resources.php)** – Additional free downloads and supplements
- **[Mythras Gateway](https://mythras.skoll.xyz/)** – Online character creator and tools

## Quick Reference

Below are campaign-specific resources and rules clarifications, organized by topic.

{% assign groups = site.info | group_by: "topic" | sort_natural: "name" %}
{% for group in groups %}

  {% assign has_content = false %}
  {% for doc in group.items %}
  {% unless doc.tags contains "nested" %}
  {% assign has_content = true %}
  {% endunless %}
  {% endfor %}

  {% if has_content %}
  <h3>{{ group.name }}</h3>
  <ul>
  {% assign items = group.items | sort: "title" %}
  {% for doc in items %}
  {% unless doc.tags contains "nested" %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endunless %}
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

---

*New to Mythras? Start with the [Mythras Imperative PDF](https://www.thedesignmechanism.com/resources/Mythras%20Imperative.pdf) for the complete rules.*
