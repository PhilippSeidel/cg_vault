[[Raumunterteilung durch reguläre Gitter|Reguläre Gitter]] sind langweilig, deshalb hat man sich adaptive Gitter ausgedacht. Unterteilt einen Raum in unterschiedlich große Zellen, kleinere Zellen in Bereichen in denen mehr Primitive sind, Große Zellen für große leere Bereiche.
![](adaptive_gitter.png)
### Oktalbaum
- Beginne mit [[Hüllkörper, Bounding Volumes|Bounding Box]] der ganzen Szene
- rekursive 1-zu-8 Unterteilung jeweils in der Mitte in jeder Richtung, falls noch zu viele Primitive in der Zelle sind
--> adaptive Unterteilung erlaubt große Schritte im leeren Raum, feine Unterteilung nur dort wo geometrie ist
#### Traversierung
- Verweise nur in Blättern auf Primitive
- Prüfe Schnitt mit Wurzel, falls Schnitt weiter mit Kindknoten
- Überprüfe alle Kindknoten von vorne nach hinten