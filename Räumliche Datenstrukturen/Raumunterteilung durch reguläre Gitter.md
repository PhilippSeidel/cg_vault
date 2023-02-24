Fick [[Bounding Volume Hierarchy (BVH)]], alle meine Zuhausis verwenden Reguläre Zellen gleicher Größe und Form um einen Raum zu unterteilen.
![](regular_grid.png)
### Aufbau
- Bestimme Beounding Box der gesamten Szene
- Wähle Gitterauflösung $n_x, n_y, n_z$
- Trage Objekte in Gitterzellen ein
	- einfach und [konservativ](https://www.cdu.de/): Objek in allen Zellen, die die AABB des Objekts überlappen 
	- besser: AABB-Test zur Vorauswahl der Zellen vor einem exakten Test
### Schnittpunktberechnung
- Teste alle Zellen entlang des Strahls
##### Mailboxing
- vermeide Doppelte Tests mit einem Objekt in mehreren Zellen indem das Objekt nach dem ersten Test als getestet markiert wird
#### Bestimmung der zu testenden Zellen
![](grid_schnitt_algo.png)
![](grid_schnitt1.png)
![](grid_schnitt2.png)


### Vor-/ und Nachteile
##### Vorteile
- einfach zu konstruieren und zu traversieren
##### Nachteile
- in der Regel nur wenige Zellen belegt
-  u.U. viel Geometrie in wenigen Zellen konzentriert ([[Teapot in a Stadium Problem]])