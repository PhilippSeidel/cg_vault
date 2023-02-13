## RGB - Farbraum
- Biologisch und technisch motiviert
**R** : Rot
**G** : Grün
**B** : Blau
![](rgb.png)



## CMY(K) - Farbraum
- dualer Raum zum RGB-Farbraum
**C** : Cyan
**M** : Magenty
**Y** : Yellow
![](cmy1.png)
![](cmy2.png)

#### CMYK
- Wird für Drucken verwendet, damit Schwarz (K) nicht gemischt werden muss nimmt man stattdessen schwarze Tinte und braucht dann nen extra Wert K
- K = min(C, M, Y) 
- C' = C - K
- M' = M - K
- Y' = Y - K


## HSV-Farbraum
H : Hue : Farbton
S : Saturation : Sättigung
V : Value : Helligkeit

- Weder additiv noch subtraktiv
- Intuitiv, deshalb oft in Benutzerschnittstellen verwendet

![](hsv.png)

#### Konversion RGB --> HSV
V = max(r, g, b) 
S = (max - min) / max
0° <= H <= 360° (mit Fallunterscheidung)
