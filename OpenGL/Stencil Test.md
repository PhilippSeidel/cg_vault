Schaltet man den Stencil-Test in OpenGL ein, wird zusätzlich zum Framebuffer und zum Tiefenpuffer ein sog. **Stencil Buffer** angelegt.
Dieser speichert zusätzliche Informationen pro Pixel.

Damit kann entschieden werden, ob ein Fragment gezeichnet werden soll. Dies geschieht mit einem Vergleich der Stencil-Werte (die den Pixeln des Fragments entsprechen) mit einem Referenz-Wert:

![](stencil_buffer.png)

### Schattenvolumen

Um Schattenvolumen zu zeichnen, zeichnet man zuerst alle Objekte. Dabei erhöhen die Vorderseiten den Wert im **Stencil Buffer**, und die Hinterseiten erniedrigen ihn.
Diese Unterscheidung macht man mittels [[Backface Culling]].

Dann zeichnet man dort Schatten, wo der Wert im Stencil-Buffer größer null ist.

![](shadow_volumes.png)