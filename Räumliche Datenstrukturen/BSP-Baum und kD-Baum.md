**B**inary **S**pace **P**artitioning Tree. Unterteile Räume mit Ebenen und baue so einen Binären Baum auf.

### Grundidee
- Erweiterung von Binärbäumen auf k Dimensionen
- Verwende Ebenen um den Raum rekursiv zu unterteilen

![](bsp_tree.png)
![](kd_tree.png)
### Unterschied BSP-Bäume vs. kD-Bäume
BSP-Bäume verwenden beliebig orientierte Ebenen, kD-Bäume nur Ebenen die senkrecht zu einer der Koordinatenachsen sind um den Raum zu Unterteilen

![[kD-Bäume]]


### Konstruktion
- Rekursiv (ähnlich wie [[Bounding Volume Hierarchy (BVH)|BVH]])
	- initialisiere Wurzelknoten: enthält alle Primitive der Szene
	- [[Surface Area Heuristik (SAH)|unterteile]] Wurkelknoten rekursiv
		- bis ein Knoten nur noch eine vorgegebene maximale Anzahl Primitive enthält
		- oder eine maximale Rekursionstiefe erreicht ist
	- unterteile den Raum in "linke und recht Hälften"

### Eigenschaften
- Echte Raumunterteilung (keine Überlappung wie bei [[Bounding Volume Hierarchy (BVH)|BVH]])
- gute Anpassung an Geometrie möglich
- kD-Bäume sind einfacher zu Konstruieren und werden daher öfter eingesetzt


### Traversierung
![](bsp_traversierung.png)


### Kombination mit [[AABB]]s
- Für Primitive eines Knotens zusätzlich eine [[AABB]] speichern
- Hilfreich wenn Primitive nur einen kleinen Teil des Raums einnehmen

### Suche im kD-/BSP-Baum
Suche das naheste Objekt/Primitiv zum Punkt e
- Problem: Das naheste Objekt ist nicht zwingend im selben Unterraum wie e
- Speichere Abstand zu zum jeweils nahesten gefunden Objekt und suche in anderen Unterräumen weiter
	- Das gesuchte Objekt kann in jedem Unterraum liegen der näher an e ist als das bisher gefundene Primitiv
	- Wandere Elternknoten nach oben und überprüfe immer ob Kindknoten diese Eigenschaft erfüllen