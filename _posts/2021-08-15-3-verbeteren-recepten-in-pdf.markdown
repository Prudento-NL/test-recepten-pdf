---
layout: post
title:  "3-Verbeteren recepten met pdf file"
date:   2021-08-15 14:45:32 +0200
---

Files uit recepten_subset
<ul>
  {% for pdf in site.static_files %}
    {% if pdf.path contains 'recepten_subset' %}
      <li>
        <a href="{{ pdf.path }}">{{ pdf.basename }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>

Files uit assets
<ul>
  {% for pdf in site.static_files %}
    {% if pdf.path contains 'assets' %}
      {% if pdf.extname == '.pdf' or file.extname == '.PDF' %}
        <li>
          <a href="{{ pdf.path }}">{{ pdf.basename }}</a>
        </li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul>
