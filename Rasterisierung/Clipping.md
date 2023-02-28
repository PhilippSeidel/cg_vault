**Clipping** schneidet Linien/Polygone, die außerhalb des gewünschten sichtbaren Bereiches liegen ab. Das kann sehr wichtig für die Effizienz der Darstellung sein, da nichts rasterisiert werden muss, was nicht im sichtbaren Bereich liegt.

Clipping hängt stark zusammen mit den [[Projektionen]] zur Sichtebene.

### Clipping mit einer [[Projektionen#Perspektivische Projektion|perspektivischen Projektion]] 

Beim Clipping mit einer perspektivischen Projektion darf das Clipping **nicht** nach der Normalisierungstransformation gemacht werden.

Es gibt mehrere Optionen wann man Clipping anwenden kann:

1. Vor der Projektionstransformation.
   In diesem Fall findet das Clipping gegen das View Frustum in Welt - oder **[[Wichtige Koordinatensysteme und Transformationen dazwischen|Kamerakoordinaten]]** statt. Man würde die Sichtpyramide mit seches Ebenengleichungen beschreiben und diese zum Clipping verwenden. 
   Allerdings gibt es effizientere Ansätze.
2. Nach der Projektionstransformation, aber vor dem Dehomogenisieren.
   Auf diese Weise findet das Clipping gegen das View Frustum in sog. Clipping-Coordinaten statt.
   Das ist effizient, weil sich die Transformationen für Modell, Kamera und Projektion in einer Matrix zusammenfassen lassen.

### Wechsel zwischen den verschiedenen Koordinatensystemen beim Clipping

Die Ausgangsbasis sind Kamerakoordinaten.
Von hier aus nutzt man die Projektionstransformation um in Clipping-Koordinaten zu kommen.
Dort findet (noch in homogenen Koordinaten) das Clipping statt. Dann wird dehomogenisiert. 
Dann findet die Normalisierungstranformation in normalisierte Gerätekoordinaten statt:

![](clipping_coordinate_systems.png)


## Clipping-Verfahren

### Clipping-Algorithmus von Cohen-Sutherland

Der Cohen-Sutherland-Algorithmus ist eine Algorithmus zum Clippen von Linien.

Es gibt zwei triviale Fälle:
1. Das Objekte ist vollständig enthalten => tirvial accept
2. Das Objekte ist gar nicht enthalten => trivial reject

Der Cohen-Sutherland-Algorithmus unterteilt eine Ebene in neun Bereiche
![](cohen_sutherland_separation.png)
Jede Bit-Stelle im Code der die Bereiche codiert, ist einer der vier Achsen zugeordnet.
Das entsprechende Bit ist gesetzt, wenn sich ein Punkt außerhalb bezüglich einer Kante befindet.

Der Algorithmus funktioniert dann wie folgt:
- Prüfe durch Verodern und Verunden auf trivial accept und trivial reject
- Falls keines von beiden der Fall, schneide Kante die überschritten wird mit der Linie. Wähle dann den Schnittpunkt als neuen Endpunkt der Linie.
- Falls der zweite Schnittpunkt ebenfalls außerhalb liegt verfahre hier ebenso.

## $\alpha$-Clipping

$\alpha$-Clipping ist eine Optimierung des Cohen-Sutherland-Algorithmus mit Hilfe von **Window-Edge-Coordinates**. Diese werden für jede Kante berechnet und sind kleiner null, falls sich ein Punkt außerhalb bezöglich der entsprechenden Kante befindet. 

Dieses $\alpha$-Clipping geht für Polygone. Dort sind es eben mehr Kanten.


### Clipping-Algorithmus von Sutherland-Hodgman

Dieser Algorithmus ist zum Clippen von Polygonen gedacht.

Als Eingabe nimmt der Algorithmus die Liste der Vertices des zu clippenden Polygons.
Als Ausgabe liefert er die Vertices des geclippten Polygons.

Der Algorithmus clippt ein Polygon gegen jede Kante einzeln und nacheinander. Deshalb kann das Clippen mehrerer Polygone in eine "Pipeline" gepackt und somit parallelisiert werden.
