---
layout: post
title:  "6-Issue oplossing"
date:   2021-10-23
---
Nog eens terugkijkend naar de oplossing in [5-dit-is-de-oplossing](/2021/08/15/5-dit-is-de-oplossing.html) zie ik toch een probleem.
- Het viel me op dat de recepten in een sub-directoty staan van assets.
- Door het gebruik van 'contains' worden alle directories inclusief de sub-directories getoond van de directory in 'file-path'.
- Als je  `file.path contains 'assets'`  zou wijzigen naar `file.path contains 'recepten'` wordt naast de directtory 'assets/recepten' ook de inhoud van directory 'recepten-subset' getoond.
- Geprobeerd om `file-path contains` aan te passen naar `file-path ==` maar nog zonder succes. Waarschijnlijk moet je verwijzen naar een path. Hier verder geenmoeite in gestoken omdat de oplossing met contains goed genoeg is.


## Conclusie:
- Recepten in een volledig eigen directory zetten (bijvoorbeeld recepten) en het 'file-path' laten verwijzen naar deze directory.