---
layout: page
title: Recent Projects
description: >
  Recent experimental tooling for making engineering knowledge usable by AI agents.
---

{% for project in site.data.projects %}
## {{ project.title }}

{{ project.description }}

{% unless project.link == "#" %}[Read more →]({{ project.link }}){% endunless %}

{% endfor %}
