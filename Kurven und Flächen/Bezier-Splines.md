Modelliere komplexere Formen mit [[(Kubische) Bezier-Kurven|Bezier-Kurven]]. Verwende eine [[(Kubische) Bezier-Kurven|Bezier-Kurve]] von hohem Grad oder füge mehrere [[(Kubische) Bezier-Kurven|Bezier-Kurven]] niedrigeren Grades stückweise aneinander. 

### $C^n$-/ und geometrische ($G^n$) Stetigkeit
Ein Spline ist 
- $C^n$-Stetig wenn:
	- Richtung und Länge der n-ten Ableitungen übereinstimmen
- $G^n$-Stetig wenn:
	- Richtung der n-ten Ableitungen übereinstimmen
![](stetigkeiten.png)
![](Ck_Uebergang_Bezier_Splines.png)


## Definition durch A-Frames
Statt Bezier-Punkte kann man die Ecken eines A-Frames festlegen um einen $C^2$-Stetigen B-Spline zu konstruieren. Diese neuen Kontrollpunkte $d_i$ nennt man de Boor-Punkte. Je Vier auseinanderfolgende de Boor-Punkte definieren eine Bezier-Teilkurve.
![](a_frame-spline.png)


## Kubische B-Splines
![](kubische_b-splines.png)
