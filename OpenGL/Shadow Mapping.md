Eine Shadow Map ist eine Textur, die nur für eine Blickrichtung und Lichtquellen-Position gültig ist. Sie speichert, aus Sicht der Kamera, wie weit die nahsten Oberflächen von der Lichtquelle entfernt sind.

Beim Rendering entspricht jeder Punkt im Raum einer Richtung von der Lichtquelle aus. Diese Richtung lässt sich zu einer, in der Shadow Map gespeicherten, nähsten Oberfläche nachschlagen.

Pro Lichtquelle wird eine Shadow Map erzeugt. Diese wird dann für die Schattenberechnung verwendet.

![](shadow_mapping.png)

