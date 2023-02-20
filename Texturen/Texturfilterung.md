
## Magnification

**Magnification** (oder Vergrößerung) ist die Abbildung weniger Texel auf viele Pixel.

### Nearest Neighbor

Bei der Nearest-Neighbor-Technik verwendet man einfach immer die Farbe des am nähsten liegenden Texels für einen Pixel.

### Bilineare Interpolation

Bei bilinearer Interpolation interpoliert man den Wert einen Pixels aus den vier Texeln die ihn umgeben. 

![](bilinear_interpolation.png)

Dabei interpoliert man drei mal:
- Zwischen $t_1$ und $t_2$: $t_{12} \space = \space (1-a) \space * \space t_1 \space + \space a \space * \space t_2$ 
- Zwischen $t_3$ und $t_4$: $t_{12} \space = \space (1-a) \space * \space t_3 \space + \space a \space * \space t_4$ 
- Zwischen $t_{12}$ und $t_{34}$: $t \space = \space (1-b) \space * \space t_{12} \space + \space b \space * \space t_{34}$ 

Das Resultat wäre dann folgendes:

![](lineare_interpolation_result.png)

Alternativ kann man sich das Interpolieren auch mit [[Baryzentrische Koordinaten|baryzentrischen Koordinaten]] vorstellen.

### Texturfilterungen höherer Ordnung
Es gibt auch Texturfilterungen höherer Ordnung als bilineare Interpolation.
Z.B. **bikubsiche Interpolation**.
Folgendes Bild zeigt einen Vergleich zwischen Nearest-Neighbor-Filterung, bilinearer Interpolation und bikubischer Interpolation:

![](texture_filtering_comparison.png)


## Minification

**Minification** ist die Abbildung mehrerer Texel auf einen Pixel,
also wenn ein Pixel auf dem Bildschirm mehrere Texel abdeckt, aber nur ein Texel ausgelesen, verwendet und angezeigt wird.
Man sagt es entstehen [[Aliasing]]artefakte durch Unterabtastung.

![](minification.png)
 Es gibt zwei Lösungsansätze:
 - Vorfilterung des Signals (der Textur)
 - Überabtasten (Supersampling), was in der Regel zu teuer ist


### Mip-Mapping

**Mip-Mapping** ist eine einfache Vorfilterung für Texturen.
Beim Mip-Mapping generiert man aus einer Textur rekursiv kleinere Texturen mit einem Viertel der Größe der Ausgangstextur (man halbiert die Größe entlang jeder Achse).
Dies bewirkt gleichzeitiges Filtern und Reduzieren der Auflösung.

Die daraus entstehende sog. Auflösungspyramide braucht nur 33% mehr Speicher als die Originaltextur selbst. (Ist also speicher-effizient)

Den Farbwert der am Ende für ein Pixel verwendet wird berechnet man durch **trilineare Interpolation**:

Man wählt die Bilder zweier Mipmap-Stufen aus. Diese Auswahl geschieht mit folgender Regel:
Texelgröße(𝑛) < Größe Pixelfootprint auf Textur < Texelgröße(𝑛 + 1).
In jedem der Mipmap-Bildern interpoliert man bilinear. Anschließend interpoliert man bilinear zwischen den interpolierten Farbwerten der beiden Mipmap-Bilder.


### Anisotrope Texturfilterung

Mip-Mapping erzeugt oft verwaschene Flächen, da die Vorfilterung bei Mip-Mapping gleichförming in $s$ und $t$ ist (isotrop). Der Pixelfootprint auf dem Texturraum ist allerdings oft nicht isotrop. 
Anisotrope Texturfilterung bezieht den Pixelfootprint auf dem Texturraum mit in die Filterung ein.