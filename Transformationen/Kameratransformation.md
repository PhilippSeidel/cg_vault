Die Kameratransformation ist ein Wechsel des Koordinatensystems, wobei der Ursprung die Kamera ist (Kamerakoordinaten).

Gespeichert wird in diesem Modell die Position der Kamera $e$, sowie die (negative) Blickrichtung $w$ und eine Up-Vektor $up$. Diese Up-Vektor gibt an, wo im Modell oben ist.
Die Basis des Kamerakoordinatensystems kann dann wie folgt berechnet werden.

![](camera_coordinates_basis.png)
![](camera_coordinates_view.png)

Dies erleichert beim [[Rasterisieren]] die Projektion auf die Bildebene.