---
layout: page
title: Recent Projects
description: >
  Recent experimental tooling for making engineering knowledge usable by AI agents.
---

1. this list will be replaced by the toc
{:toc .large-only}

{% for project in site.data.projects %}
## {{ project.title }}

{{ project.description }}

{% if project.finding %}> {{ project.finding }}
{% endif %}
{% unless project.link == "#" %}[Read more →]({{ project.link }}){% endunless %}

{% unless forloop.last %}---{% endunless %}

{% endfor %}
