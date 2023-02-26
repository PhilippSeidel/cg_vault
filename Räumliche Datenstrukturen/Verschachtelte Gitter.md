Sowohl [[Raumunterteilung durch reguläre Gitter|Reguläre Gitter]] als auch [[Raumunterteilung durch adaptive Gitter|Adaptive Gitter]] haben vor und Nachteile, wenn man verschiedene Gitterarten verschachtelt kann man sich die Vorteile von beiden zu Nutze machen. Nutzt due effiziente Traversierung von [[Raumunterteilung durch reguläre Gitter|regulären Gittern]] und die Adaptivität einer [[Raumunterteilung durch adaptive Gitter|hierarchischen Repräsentation]].

### Aufbau
- Grobes Giter für Bounding Box der Szene
- Zellen mit dicht gepackten Objekten werden durch neues Gitter ersetzt
--> Benötigt Heuristik: Wann Gitter welcher Auflösung?

### Vergleich Gitter vs. Octree
![](vergleich_gitter.png)
