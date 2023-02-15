Wenn man ein 2D-Bild aus Pixeln von einer 3D-Szene baut dann bestimmt man die Farbe eines Pixels durch einen Strahl der durch dessen Mittelpunkt geht. Dadurch das so diskret Abgetastet wird und Pixel Quadraisch sind kann es zu Treppenstufeneffekten kommen. Außerdem können hässliche Aliasingeffekte entstehen.

- Aliaseffekte entstehen durch ungenügende Abtastung von Signalen
![](aliasing.png)
#### Nyquist-Shannon-Abtasttheorem
Ein kontinuierliches, bandbegrenztes Signal mit einer max. Frequenz $f_{max}$ muss mit einer Frequenz größer als $2f_{max}$ abgetastet werden, damit aus dem diskreten Signal das Ursprungssignal exakt rekonstruiert werden kann

##### Typische Quellen von Aliasing
- Detaillierte Geometrie
- Texturen
- Shading

![](Supersampling.md)