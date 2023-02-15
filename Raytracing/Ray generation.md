Wenn man Strahlen durch die Gegend ballern will braucht man erstmal ein paar Strahlen. Zum Glück kann man die ganz leicht konstruieren.

- Definiere Virtuelle Kamera durch
	- Position e
	- Zielpunkt z
	- Negative Blickrichtung w = $\frac{e - z}{|e - z|}$
	- Up-Vektor up
	![](virtuelle_kamera_koordinaten.png)

	u = up x w und v = w x u

- Erzeuge Sichtstrahl mit Richtungsvektor s
![](richtungsvektor_s.png)
![](Bildebene.png)

- Abstand zur Kamera d
- linker/rechter Rand l und r
- unterer/oberer Rand b und t
- 