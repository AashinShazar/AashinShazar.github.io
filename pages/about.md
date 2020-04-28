---
layout: page
title: About Me
permalink: /about/
weight: 5
---

# **About Me**

Hi I am **{{ site.author.name }}** :robot: and welcome to my website!<br>

Here's everything you need to know about me at a glance. Head over to the resume section for a deeper dive of what I can bring to your company.

<div class="row">
{% include about/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Technical Skills" source=site.data.other-skills %}
</div>

<div class="row">
{% include about/timeline.html %}
</div>