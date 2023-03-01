Koordinatensysteme zur beschreibung von Farben.

## RGB - Farbraum
- Biologisch und technisch motiviert
**R** : Rot
**G** : Grün
**B** : Blau
![](rgb.png)
$+$ RGB ist additiv


## CMY(K) - Farbraum
- dualer Raum zum RGB-Farbraum
**C** : Cyan
**M** : Magenty
**Y** : Yellow
![](cmy1.png)
![](cmy2.png)

#### CMYK
- Ist subtraktiv
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

## XYZ-Farbraum

Das Ziel dieses Farbraums ist es standardisiert zwischen anderen Farbräumen konvertieren zu können, sowie alle wahrnehmbaren Farben darzustellen.
In diesem Farbraum sind die [[Color Matching Funktion]]en rein positiv.

Die Abbildung in den RGB-Raum ist linear.

## xyY-Farbraum

Der xyY-Farbraum baut auf dem XYZ-Farbraum auf. 
In diesem Farbraum ist Y die Helligkeit und xy die Chromazität.
Allerdings gilt die Normalisierungsbedingung 𝑋 + 𝑌 + 𝑍 = 1.
![](xyY.png)

Der Farbraum ergibt sich dann aus 𝑘𝑋, 𝑘𝑌, 𝑘𝑍 (𝑘 > 0). Für feste X,Y,Z und reguliert k die Intensität, wobei die Farbe allerdings gleich bleibt.

𝑥 = $\frac{𝑋}{𝑋+𝑌+𝑍}$ , 𝑦 = $\frac{Y}{𝑋+𝑌+𝑍}$, z = 1 - x - y (z wird nicht explizit gespeichert)

Folgendes Diagram ist das Chromazitätsdiagram:


x und y geben den Wert auf dem Chromazitätsdiagram an:
![](chromazitätsdiagram)
