Beim **Blending** wird eine Farbwert aus dem Framebuffer mit den Farben eines Fragments anhand von Gewichten kombiniert.
Diese Gewichte werden entweder aus den RGBA-Werten erzeugt, oder sind konstant voreingestellt.

![](blending.png)

In OpenGL kann man Blending ein - und ausschalten. 

### Semitransparente Objekte

Die Darstellung semitransparenter Objekte erfordert eine **Tiefensortierung**. Ansonsten werden sich überlappende semitransparente Flächen nicht korrekt dargestellt.

Auch der Tiefentest ist problematisch bei semitransparenten Objekten.

Bei der Rasterisierung verschwinden **als Notlösung** transparente Polygone hinter opaken Polygonen.

### Kommutative Blending-Modi

Diese Arten des Blendings funktionieren ohne eine **Tiefensortierung**:
- Multiplikation der Source-Farbwerte und Destination-Farbwerte
- Addition der RGBA-Vektoren

### Alpha-Blending

Beim Alpha-Blending wird zwischen der Farbe im Fragment und der Farbe im Framebuffer bilinear interpoliert. Wobei $\alpha$ und $(1-\alpha)$ die Gewichte der Farben sind. 