Erzeuge Zufallswerte für Punkte eines Gitters, interpoliere zwischen den Werten.
### Art der Interpolation
Lineare Interpolation ist shit weil man dort Bandeffekte und so bekommt. trikubisch ist besser.
![](interpolation_LVN.png)

### Art der Zufallszahlen
- **naiver Ansatz:** erzeuge großes 2D/3D-Gitter gefüllt mit Zufallszahlen
	- Z(x) gibt Werte aus dem Gitter zurück
	- ist unpraktisch wg. großer Datenmenge und Periodizität
- **eleganter:** erzeuge ein 1D-Array mit Zufallszahlen zwischen 0 und 1
	- verwende Hashfunktion um darauf zuzugreifen
	![](hash_index.png)
	- P(.) ist eine Permutation
	- Zufallszahl ergibt sich dann als
	![](hash_zufallszahl.png)
	