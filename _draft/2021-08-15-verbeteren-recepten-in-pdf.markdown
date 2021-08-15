---
layout: post
title:  "Test recepten met pdf file"
date:   2021-08-15 12:45:32 +0200
---

Werkt, maar er komt een extra file mee minima-social-icons
  <ul>
  {% for pdf in site.static_files %}
          <li>
    <a href="{{ pdf.path }}">{{ pdf.basename }}</a>
      </li>
  {% endfor %}
  </ul>

  <ul>
  {% for pdf in site.static_files %}
  {% if pdf.path contains 'assets/recepten/' %}
  {% endfor %}

          <li>
    <a href="{{ pdf.path }}">{{ pdf.basename }}</a>

      </li>


  </ul>
