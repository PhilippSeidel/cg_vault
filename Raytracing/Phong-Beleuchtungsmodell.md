- Modelliert Reflektion in drei Komponenten
	- ambient: indirekte Beleuchtung, Licht von anderen Oberflächen
	- diffus: nach dem Lambertschen Gesetz ([[Lambertsche Reflektion]])
	- spekular: imperfekte Spiegelung ([[Spekulare Reflektion]])

### $I = k_a \cdot I_L + k_d \cdot I_L \cdot (n \cdot l) + k_s \cdot I_L \cdot (r_l \cdot v)^n = I_L \cdot (k_a + k_d \cdot (n \cdot l) + k_s \cdot (r_l \cdot v)^n)$ 
$k_a$ : Ambienter Koeffizient
$k_d$ : Diffuser Koerffizient
$k_s$ : Spekularer Koeffizient
$I_L$ : Lichtintensität
![](specular_refelction.png)
- $k_a, k_d, k_s, I_l$ sind wellenlängenabhängig
- $k_a, k_d$ repräsentieren die Eigenfarbe der Oberfläche
- $k_s$ hat bei Metallen Oberflächenfarbe sonst meist Farbe der Lichtquelle
- man verwendet oft $(n \cdot l)^+ := max(0, (n \cdot l))$ weil nur Richtungen interessant sind deren Skalarprodukt positiv ist

![](computeDirectLight.png)
Intensität sollte realistisch im Abstandsquadrat abfallen -> teile Ergebnis durch $(dist \cdot dist)$ 
