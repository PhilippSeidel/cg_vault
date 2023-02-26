Texturen sind meistens nur als Schnipsel verfügbar. Um große Flächen zu texturieren braucht man große Texturen, mit Textursynthese kann man große Texturen erzeugen die "genau so aussehen" wie die Schnipsel. (D.h. gleiche statistische Eigenschaften haben).

![](textursynthese.png)


- Ausgabetextur wird Pixel für Pixel erzeugt
- Betrachte Nachbarschaft des nächsten zu erzeugenden Pixels
	- i.d.R. kleine Nachbarschaften ca.30-100Pixel, aber große genug um Strukturen der Textur zu erfassen
- Suche ähnliche Nachbarschaften in Eingabetextur (ähnlich heißt Summe über alle Pixelfarbdifferenzen klein)
- Kopiere Pixel einer der ähnlichsten Nachbarschaften

Algorithmus ist sehr einfach aber langsam

