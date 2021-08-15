---
layout: post
title:  "1-Recepten met pdf file"
date:   2021-08-15 12:00:32 +0200
---

Werkt, maar er komt een extra file mee minima-social-icons omdat alle assets weergegeven worden.

  <ul>
  {% for pdf in site.static_files %}
        <li>
    <a href="{{ pdf.path }}">{{ pdf.basename }}</a>
      </li>
  {% endfor %}
  </ul>
