---
layout: page
title: About Me
permalink: /about/
weight: 5
---

# **About Me**

Hi I am **{{ site.author.name }}** :robot: and here’s everything you need to know about me at a glance.<br>

<div class="row">
{% include about/skills.html title="Coding Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Technical Skills" source=site.data.other-skills %}
{% include about/skills.html title="Engineering Tools" source=site.data.tool-skills %}
</div>

<div class="row">
{% include about/timeline.html %}
</div>