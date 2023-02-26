Um unnötige [[Ray intersecion|Schnitttests]] bei [[Raytracing (Whitted-Style)|Ray tracing]] zu vermeiden hüllt man Dreiecksnetze in Hüllkörper ein. Diese haben eine einfachere Geometrie und geben Aufschluss ob die Dreiecke überhaupt noch getestet werden müssen.

### Verschiedene Arten

#### Kugel
- Schneller Schnittalgorithmus
- Oft zu groß

#### [[AABB]] (Axis Aligned Bounding Box) <--WICHTIGSTE ART
- Einfache Berechnung (min/max)

#### OBB (Oriented Bounding Box)
- Aufwendige Berechnung

#### Begrenzende Halbräume
- Gute Effizienz, schnelle Berechnung