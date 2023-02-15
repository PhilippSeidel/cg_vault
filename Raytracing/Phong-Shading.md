Illusion einer glatten, gekrümmten Fläche. Nutzt Interpolation von Normalen und das [[Phong-Beleuchtungsmodell]] (deshalb heißt das auch so).


- Vertexnormalen bestimmen über gewichtete Summen der angrenzenden Flächen
	- Berechne Normale für jedes Dreieck
	- für jeden Vertex: summiere Normalen aller angrenzenden Dreiecke
	![](normal_interpolation.png)
- Scharfe Kanten brauchen mehrere Normalen (wenn man immer nur interpoliert gehen Kanten Verloren)
- Definiere Threshold ab wann eine Kante scharf sein soll, also ab der der Winkel zwischen zwei angrenzenden Flächen zu groß ist
![](sharp_edges.png)
- Nutze [[Baryzentrische Koordinaten]] um zwischen Vertexnormalen zu interpolieren und normalen für beliebige Punkte auf der Oberfläche zu berechnen
	- Es muss darauf geachtet werden das Ergebnis der Interpolation erneut zu normieren. **Interpolation ist nicht längenerhaltend!**
![](normal_interpolation2.png)
- Beleuchtungsberechnung mit interpolierten Normalen nennt man [[Phong-Shading]] (**!= [[Phong-Beleuchtungsmodell]]**)
![](flat_shading_vs_phong_shading.png)
