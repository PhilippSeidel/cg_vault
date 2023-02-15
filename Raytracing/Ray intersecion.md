
- Für implizite Geometriedarstellung (siehe [[Mathe Grundlagen]]) muss in die definition der Geometrie die Strahlengleichung eingesetzt werden, dann auflösen
- Für Dreiecke zwei Möglichkeiten:
	- [[Baryzentrische Koordinaten]] für den Schnittpunkt mit der Dreiecksebene berechnen und dann auswerten ob alle größer gleich 0 sind (anschaulich aber so macht man es wohl nicht)
	-  Punkte in Ebene des Dreiecks lassen sich beschreiben durch $Q(\lambda_2, \lambda_3) = P_1 + \lambda_2(P_2 - P_1) + \lambda_3(P_3 - P_1)$ , setzte Strahlengleichung mit dieser Gleichung gleich
		--> 3 Gleichungen, 3 unbekannte $t, \lambda_2, \lambda_3$ , Löse mittels Cramerscher Regel

#### Möller-Trumbore-Algorithmus
- nutze Cramersche Regel (siehe [[Mathe Grundlagen]]) um nacheinander die [[Baryzentrische Koordinaten]] u und v zu berechnen (mach early out möglich, falls eine der koordinaten nicht zwischen 0 und 1 liegt)
- berechne t für die Strahlengleichung auch mittels Cramerscher Regel
- falls t bisher kleinstes gefundenes t größer 0 ist überschreibe hitpoint mit {Dreieck_ID, t, u, v}