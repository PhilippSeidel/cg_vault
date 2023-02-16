Verwandt mit [[Distributed Raytracing]], ist praxisrelevant™. [[Raytracing (Whitted-Style)|Verfolge]] jeweils nur einen weiteren [[Sekundärstrahlen|Strahl]], dafür aber mehrere "Pfade" pro Pixel. Führt zu höherer Abtastung nahe der Kamera, geringere Abtastung bei weiter entfernten Regionen.
![](path_tracing.png)
Verdeckung kann zu Problemen führen, weil Pfade vielleicht nicht bis zur Lichtquelle finden.
![](obstruction.png)