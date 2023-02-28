
Im klassischen OpenGL sieht die Grafik-Pipeline wie folgt aus:

![](classical_opengl_pipeline.png)

Allerdings ist diese Pipeline **nicht programmierbar**, sondern nur **konfigurierbar**. 

Beim klassischen OpenGL wird [[Buffering]] verwendet.

Außerdem gibt es die Möglichkeit einen **Matrix-Stack** zu verwenden.

### Geometrische Primitive

![](opengl_classical_primitives.png)

### Geometrieverarbeitung

Der Schritt der **Geometrieverarbeitung** beinhaltet die Angabe, wie Primitive aus einem Strom von Vertices zusammengesetzt werden.
Diese Angabe wird in klassischem OpenGL mit dem glBegin-Befehl eingeleitet und mit dem glEnd-Befehl abgeschlossen.
Das anschließende Clipping und die Rasterisierung geschehen ohne eigenes Zutun.

### Shading

Das Shading findet in **[[Wichtige Koordinatensysteme und Transformationen dazwischen|Kamerakoordinaten]]** statt.

Es gibt folgende Shading-Arten in klassischem OpenGL:
- [[Shadingarten|Flat-Shading]]: Das ist Shading pro Vertex/Fragment mit **Dreiecks-Normale**
- Gouraud-Shading: Das ist Shading pro Vertex mit **gemittelter Normale der anliegenden Dreiecke**
- [[Phong-Shading]]: Das ist Shading pro Fragment mit **interpolierter Normale**

Alle Shading-Arten verwenden eine Variante [[Phong-Beleuchtungsmodell|Phong-Beleuchtungsmodells]], genannt **Blinn-Phong-Beleuchtungsmodell**. 
[[Phong-Shading]] kann auch andere Beleuchtungsmodelle verwenden. 
Allerdings wird [[Phong-Shading]] in klassischem OpenGL nicht nativ unterstützt, Gouraud-Shading aber schon.