In der Computergrafik berechnet man die Farben von Bildern in einem linearen Raum.
Ein Monitor stellt Farben allerdings nicht in einem linearen Verlauf dar.
Stattdessen hat jeder Monitor einen charakteristischen Gamma-Wert.
Die Intensität die ein Monitor darstellt, hänget dann wie folgt von der Helligkeit im linearen Raum ab:
![](monitor_intensity_correlation.png)
Dabei ist n aus \[0, ..., N\]  und I(n) die vom Monitor dargestellte Intensität.
	=> Die dargestellte Intensität ist proportional zur prozentualen Intensität im linearen Raum (n/N) hoch den Gamma-Wert des Bildschirms.

Aus diesem Grund werden die Werte im Framebuffer **direkt vor der Darstellung** angepasst, um die Verzerrung des Monitors auszugleichen.

Um I(n) ∝ a die Intensität I(n) richtig  darzustellen wähle n wie folgt: 𝑛 ∝ 𝑎^(1/𝛾):

![](gamma_correction.png)

Diese Korrektur wird für jede Primärfarbe unabhängig von den anderen Primärfarben durchgeführt.

Beispiel: Wie bestimmt man den Gamma-Wert bei bekanntem Pixel-Wert und bekannter Intensität?

![](determine_gamma_example.png)

Die Werte aus dem Framebuffer werden dann mit einer sogenannten Transferfunktion auf die entsprechenden Intensitäten abgebildet:
[[Transferfunktion]] 
Diese macht dann auch die Quantisierung.
Das ergibt Sinn schaut man sich die Bildmenge der Transferfunktion an.
Sie ist das Intervall $[I_{max}$, $I_{min}]$ und keine prozentuale Angabe wie $I(n) \in [0,1]$.

## Quantisierung

Die Intensität I(n) ist eine prozentuale Angabe. Die Quantisierung bildet I(n) auf einen absoluten Pixelwert in der Skala der Bildschirms ab, indem I(n) mit der (absoluten) maximalen Intensität des Bildschirms I_max multipliziert wird.