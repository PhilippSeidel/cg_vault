
![](per_fragment_operations.png)

Die **Per-Fragment Operationen** gibt es sowohl im [[Klassisches OpenGL|klassischen OpenGL]], als auch im [[Modernes OpenGL|modernen OpenGL]].
Den Alpha-Test gibt es allerdings nur im klassichen OpenGl.

Die **Per-Fragment-Operations** werden nach dem Rasterisieren und insbesondere nach dem [[Fragment Shader]] ausgeführt. Die oben dargestellten Tests müssen für jedes Fragment durchgeführt werden, bevor es in den Framebuffer geschrieben werden kann.

### Tiefentest
Der Tiefentest ist der Test, der die Tiefenwerte der Pixel des Fragments, mit den Tiefenwerten im [[Sichtbarkeit und Verdeckung von Objekten#Z-Puffer/Tiefenpuffer|Tiefenpuffer]] vergleicht.

### Alpha-Test (nur klassisches OpenGL)
Beim Alpha-Test werden Fragmente aufgrund ihres Alpha-Wertes verworfen.
Im modernen OpenGL kann das im Fragment Shader unter Verwendung des **discard**-Schlüsselwortes implementiert werden.

### [[Blending]]

### [[Stencil Test]]

### Scissor Test
Beim Scissor Test werden alle Fragmente außerhalb eines spezifizierten Rechtecks entfernt. Damit kann man nur einen kleinen Teil des Fensters akutalisieren.

