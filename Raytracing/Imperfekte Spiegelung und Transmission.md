[[Spekulare Reflektion|Perfekte Spiegelung]] ist unrealistisch und damit uncool.

Um alle Lichtwege zu berücksichtigen, sind mehrere Strahlen nötig.
- Richtungen basically zufällig
- Anteil an Gesamtfarbe werden durch [[Bidirektionale Reflektanzverteilungsfunktion (BRDF)|BSDF]] bestimmt
![](imperfekte_spiegelung.png)

#### Physik sagt:
### $L(x,\omega) = L_e(x,\omega)+\int_{\Omega oder \Omega^+}f_r(\omega_i,x,\omega)L_i(x,\omega_i)cos\Phi_i, d\omega_i$ 

- $L$ : Strahldichte
- $L_e$ : Emissionsterm
- $L_i$ : Einfallendes Licht
- Integrationsbereich (Im Bild die Halbkugel):
	- $\Omega^+$ : posiive Hemisphäre (nur Reflexion)
	- $\Omega$ : alle Richtungen (inkl. Transmission)
- $f_r$ : Reflektanzverteilungsfunktion (Wie viel Licht aus Richtung $\omega_i$ wird in Richtung $\omega$ reflektiert?)
- $cos\Phi$ : Einfallsrichtung

![](rendering_gleichung.png)
![[Monte Carlo-Rendering]]