---
layout: post
title:  "9-link naar pdf file werkt niet"
date:   2022-01-29
---
# Dit is de oplossing:
[comment]: # % raw % in het code block is om de Liquid te tonen en niet eerst te laten verwerken.

De hyperlink in de oplossing zoals beschreven in post 5 is niet correct.  
In de hyperlink moet verwezen worden naar de baseurl. 
```
{% raw %}
<ul>
  {% for file in site.static_files %}
    {% if file.path contains 'assets' %}
      {% if file.extname == '.pdf' or file.extname == '.PDF' %}
        <li>
          <a href="{{ site.baseurl }}{{ file.path }}">{{ file.basename }}</a>
        </li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul>
{% endraw %}
```  

# Uitleg
- De naam `file` kan gewijzigd worden indien noodzakelijk voor een beter overzicht. Dat moet dan ook in de prefixes van de code gedaan worden.
- De `site.static.files` zijn statische files zonder front matter, zoals images en pdf.
- Het `file.path` geeft de directory weer waaruit de data gepresenteerd wordt; in dit geval `assets`. Als de files opgeslagen worden in een andere directory dan moet de directory wijzigen in deze regel.
- De `file.extname` is de extensie van de files die opgenomen worden in de lijst. De regel aanpassen als je andere extensies wil tonen of verwijderen (inclusief de % endif %) als je alles wilt zien wat er in de directory staat.
- De link `<a href="....</a>` is de link naar de file en de naam die weergegeven wordt

# Het resultaat van de code:
<ul>
  {% for file in site.static_files %}
    {% if file.path contains 'assets' %}
      {% if file.extname == '.pdf' or file.extname == '.PDF' %}
        <li>
          <a href="{{ site.baseurl }}{{ file.path }}">{{ file.basename }}</a>
        </li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul>
