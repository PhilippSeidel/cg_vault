Whitted-Style Raytracing ist zu schön. Um das zu ändern hat man sich distributed raytracing ausgedacht.

#### Ziele:
- **Weiche Schatten**
	- Reale Lichtquellen haben räumliche Ausdehnung --> mehrere Schattenstrahlen zur Lichtquelle schicken
- **Bewegungsunschärfe** (Dinge machen wooosh)
	- Pixel mehrfach zu verschiedenen Zeitpunkten berechnen und das Ergebnis mitteln
![](motion_blur.png)
- **Tiefenunschärfe**
	- Echte Kameras enthalten Linsen und haben eine Brennweite
	- Simuliere Linse indem zuerst der Eintrittspunkt in Linse und dann der neue Strahl von dort durch den Brennpunkt berechnet wird
![](depth_blur.png)
![](depth_blur_code.png)
- **[[Imperfekte Spiegelung und Transmission]]**


Wie bei [[Raytracing (Whitted-Style)|Whitted-Style Raytracing]] findet auch hier Rekursion statt, es wird allerdings mithilfe von [[Distributed Raytracing]] und [[Monte Carlo-Rendering]] ein (hemi-)sphärisches Integral berechnet, statt immer nur ausgewählte [[Sekundärstrahlen]] zu verschießen.
![](distributed_raytracing_hemispaeren.png)



##### Related
[[Raytracing (Whitted-Style)]]