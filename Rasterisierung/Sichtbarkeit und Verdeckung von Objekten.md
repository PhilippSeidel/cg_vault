In einer Szene können sich Objekte überdecken. Um sie darstellen zu können muss man bestimmen welches Objekt wo sichtbar ist.

### Maler-Algorithmus

Angenommen wir können bereits Polygone rasterisieren.
Der Maler-Algorithmus ist ein Ansatz, bei dem man Polygone nach ihrem Abstand zur Kamera absteigend sortiert. (Also "von hinten nach vorne")
In dieser Reihenfolge zeichnet man die Polygone dann auch.

**Probleme:**
- Es ist unklar nach welchem Abstand sortiert werden soll. Der Abstand eines Punktes auf einem Polygon zur Kamera liefert nicht immer das korrekte Ergebnis
- Falls es Zyklen bei den Polygonen gibt können diese nicht aufgelöst werden

### Z-Puffer/Tiefenpuffer

Der Tiefenpuffer ist ein bildbasierter Ansatz, bei dem in jedem "Pixel" anstatt einer Farbe der Abstand zur nahsten Fläche gespeichert wird.

![](deep_buffer.png)

Bei der Verwendung eines Tiefenpuffers gibt es also zusätzlich zum Farbpuffer einen zweiten Puffer. Bevor ein Farbwert in den Farbpuffer geschrieben wird, wird zuerst im Tiefenpuffer getestet ob nicht bereits ein "näherer" Farbwert im Farbpuffer steht. Diesen Test nennt man **Tiefentest**.

**Vorteile:**
- Dreiecke/Polygone können in beliebiger Reihenfolge verarbeitet werden.
- Ein Tiefenpuffer ist Standard beim Rasterisieren, auch auf Grafikhardware

**Nachteile:**
- Begrenzte Genauigkeit
- Z-Aliasing
- transparente Flächen sind schwierig zu behandeln