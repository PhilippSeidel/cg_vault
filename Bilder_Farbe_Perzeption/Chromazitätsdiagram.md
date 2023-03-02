Das Chromazitätsdigramm enthält alle Farben der menschlichen Wahrnehmung.
Die Spektralfarben befinden sich entlang der Randkurve und entsprechen monochromatischem Licht. Der untere Rand ("purple line") enthält keine Spektralfarben.
![[chromacity_diagram.png]]

### Komplementäre Farben und Farbanteile ablesen.

- Man kann die Komplementärfarbe einer Farbe ablesen, indem man den die Gerade durch den Weißpunkt bis zum Rand verlängert.
- Um die reinen Spektralfarben zu einer Farbe C zu finden, legt man die Gerade durch C und W und nimmt die Randfarben

![](chromacity_diagram_read.png)

### Ablesen des Gamuts eines Ausgabegerätes

Der Gamut eines Ausgabegerätes ist die Menge aller Farben, die das Ausgabegerät darstellen kann.
Dieser wird wie folgt durch drei Farben (bzw. drei Wellenlängen im Spektrum) festgelegt:

![](chromacity_diagram_gamut.png)

Vergrößern lässt sich ein Gamut durch besser gewählte oder mehr Primärfarben.

Zusammen mit dem [[Transferfunktion|Dynamikumfang]]  ist der Gamut die größte Einschränkung für Monitore.

## Gamut Mapping
**Gamut-Mapping** ist die Abbildung zwischen den (verschiedenen Gamuts) zweier Monitore, mit dem Ziel Farbverschiebungen zu vermeiden.

Um ein Mappinng zwischen Gamuts durchzuführen benötigt es einen neutralen Zwischenfarbraum. z.B. [XYZ und (CIE)LAB](./Farbräume.md). Dies ist nötig da es abhängige Farbräume gibt die auf Anwendungen oder Geräte zugeschnitten sind, wie z.B. sRGB oder CMYK.

**Achtung:** Es kann auch nur zwischen Farbräumen konvertiert werden. Ein Farbraum ist kein Gamut!

Zu den verwendeten Algorithmen gehören sowohl das 
- Gamut Clipping, als auch die
- Gamut Compression 
- und die Kombination aus beiden.

### Gamut Clipping
Alle Farben innerhalb des Zielgamuts bleiben gleich, alle außerhalb werden mit kürzester euklidischer Distanz auf eine Farbe im Gamut gemappt.
> Der Clipping Algorithmus, welcher mit der geringsten Euklidischen Distanz arbeitet, berechnet das Zielgamut so, dass alle innerhalb des Zielgamuts liegenden Farbwerte gleich bleiben und die Werte außerhalb auf den Punkt transformiert werden, der am nächsten zur Gamutgrenze des Abbildungsgerätes liegt.
> [Gamut Mapping Proseminar](https://userpages.uni-koblenz.de/~cg/ss09/Proseminar_Farbmanagement/Gamut-Mapping.pdf)

### Gamut Compression
![[gammut_compression.png]]