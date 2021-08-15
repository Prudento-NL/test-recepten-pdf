---
layout: post
title:  "Verbeteren recepten met pdf file"
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
    {% endif %}
  {% endfor %}

          <li>
    <a href="{{ pdf.path }}">{{ pdf.basename }}</a>

      </li>
</ul>
<!-- <ul
  class="image-gallery">
  {% for file in site.static_files %}
    {% if file.path contains include.folder %}
      {% if file.extname == '.jpg' or file.extname == '.jpeg' or file.extname == '.JPG' or file.extname == '.JPEG' %}
        {% assign filenameparts = file.path | split: "/" %}
          {% assign filename = filenameparts | last | replace: file.extname,"" %}
            <li>
              <a href="{{ file.path | relative_url }}" title="{{ filename }}">
                <img src="//images.weserv.nl/?url={{ site.url | replace: 'http://','' | replace: 'https://','' }}{{ file.path | relative_url }}&w=300&h=300&output=jpg&q=50&t=square" alt="{{ filename }}" title="{{ filename }}" /><span>{{ filename }}</span></a>
              </li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul> -->
