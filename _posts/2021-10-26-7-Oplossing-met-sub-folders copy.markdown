---
layout: post
title:  "7-Oplossing met sub-folders"
date:   2021-10-26
---
In de ordners met resepten gebruikte ik een indeling op hoofdpunten.
Bijvoorbeeld: Gevogelte, rijst, past, desserts, etcetera.

Je zou zo'n soortgelijke indeling kunnen maken met folders en sub-folders.

Voor een complete opsomming verwijs je naar de hoofdfolder.  
Eventueel een navigatiedeel maken naar de sub-folders is dan ook mogelijk.

# Het resultaat van de code:
<ul>
  {% for file in site.static_files %}
    {% if file.path contains 'indeling' %}
      {% if file.extname == '.pdf' or file.extname == '.PDF' %}
        <li>
          <a href="{{ file.path }}">{{ file.basename }}</a>
        </li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul>
