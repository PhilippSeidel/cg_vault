Bei **Bump-Mapping/Normal-Mapping** wird die Normale einer Oberfläche verändert.
Im [[Phong-Beleuchtungsmodell]] entspricht das dem verändern des Parameters $N$ (und damit auch des Parameters $R$).

Die Normale einer Oberfläche wird durch die Angabe einer Bump/Normal-Map wie folgt verändert:
![](bump_normal_map_effects.png)
Die Oberfläche bleibt dabei allerdings flach(gestrichelte Linie im Bild rechts).

Dabei kann es allerdings zu Inkonsistenzen der Schattenberechnung, da teilweise die Normalen nicht mehr zu den glatten Oberflächen passen, die aber weiterhin für Schnitttests mit Strahlen genutzt werden.


