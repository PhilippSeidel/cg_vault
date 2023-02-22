Es gibt zwei Arten von Projektionen:
- Senkrechte Projektion auf die Bildebene:
  Hierbei wird von einer orthographischen Kamera bzw. von parallelen Sichtstrahlen ausgegangen.
  ![](orthographic_projection.png)
- Zentrierte Projektion:
  Hierbei wird von einer perspektivischen Kamera ausgegangen.
  ![](perspective_projection.png)

### Orthographische Projektion

Bei der orthographischen Projektion wird davon ausgegangen, dass die Koordinaten aller Objekte in Kamerakoordinaten vorliegen. Dabei zeigt die x-Achse nach rechts, die y-Achse nach oben und die z-Achse in die negative Blickrichtung.

Die Bildebene ist parallel zur xy-Ebene => orthogonal zu z-Ebene.

Das sog. **Sichtvolumen** (oder View Frustum) ist eine rechteckiger Ausschnitt aus der Szene, in dem sich alles Sichtbare (alles was angezeigt werden soll) befindet.

![](orthographic_projection_transformation.png)

Der Quader ist definiert durch $[l,r] \times [b,t] \times [n,f]$. 
Durch eine affine Abbildung wird der dieser Quader auf den Einheitswürfel $[-1,1]^3$ abgebildet.
Diese Operation ist eine **Projektionstransformation**. Die eigentliche Projektion ist das weglassen der z-Koordinate.

### Perspektivische Projektion

Bei der perspektivischen Projektion ist das View Frustum eine sog. Sichtpyramide. Diese wird ebenfalls auf den Einheitswürfel $[-1,1]^3$ abgebildet.

![](perspective_projection_transformation.png)
Diese Abbildung umfasst eine Projektions und eine Normalisierungstransformation.
Nach der Normalisierung geht man von parallelen auf den Einheitswürfel gerichteten Sichtstrahlen aus.
![](perspective_projection_transformation_2.png)
Außerdem zeigt die Z-Achse nun nicht mehr in die negative, sondern in die positive Blickrichtung.

Die Transformation der der z-Werte ist nicht linear. Die Genauigkeit bei Oberflächen die näher bei der Kamera sind ist größer.
Deshalb muss man [[Clipping]] anwenden um die problematischen/ungenauen Randbereiche wegzuschneiden:

![](perspective_projection_clipping.png)
Die hier angegebene Tiefe ist die nach Projektions- und Normalisierungstransformation.