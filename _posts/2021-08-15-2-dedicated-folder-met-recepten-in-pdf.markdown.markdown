---
layout: post
title:  "2-Dedicated folder met recepten met pdf file"
date:   2021-08-15 13:00:32 +0200
---

Hierin wordt alleen de content van de folder assets/recepten weergegeven

<ul>
  {% for pdf in site.static_files %}
    {% if pdf.path contains 'assets/recepten/' %}
      <li>
        <a href="{{ pdf.path }}">{{ pdf.basename }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
