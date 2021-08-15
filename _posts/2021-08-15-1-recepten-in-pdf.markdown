---
layout: post
title:  "1-Recepten met pdf file"
date:   2021-08-15 12:00:32 +0200
---


  <ul>
  {% for pdf in site.static_files %}
        <li>
    <a href="{{ pdf.path }}">{{ pdf.basename }}</a>
      </li>
  {% endfor %}
  </ul>
