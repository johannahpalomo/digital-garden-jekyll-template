---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 1em 1em; background: #f5f7ff; border-radius: 4px;">
  I'm a doctoral candidate in Sociology at the University of North Carolina at Chapel Hill.
</p>

I study religion, gender, family, and well-being. [[about|More about me.]]

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 3 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
