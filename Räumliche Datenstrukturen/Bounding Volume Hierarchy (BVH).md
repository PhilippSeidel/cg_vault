[[Hüllkörper, Bounding Volumes|Bounding Volumes]] sind cool aber damit es richtig effizient wird verschachtelt man die dinger noch. Dabei entsteht eine Baumstruktur.
![](BVH.png)
In der Theorie lässt sich so eine Beschleunigung von $O(n) \rightarrow O(log(n))$  erreichen.

### Aufbau der Datenstruktur
#### Top-Down
- Bestimme den Hüllquader der Primitive jeder Gruppe (anfangs alle Dreiecke)
- Teile Primitive in zwei Gruppen auf
- Verfahre so Rekursiv weiter
Jeder Knoten speichert die Hüllkörper seiner Kindknoten und einen Verweis auf diesen
##### Unterschiedliche Unterteilungskriterien
- Unterteile in der Mitte senkrecht zur Achse der größten Ausdehnung
- Unterteile abwechselnd rotierend zwischen x-,y-,z-achse
- Unterteile so das in den Teilmengen etwa gleich viele Objekte sind
- Verwende Szenengraph
- Minimiere Kostenfunktion ([[Surface Area Heuristik (SAH)]])
Hüllkörper können überlappen --> kann zusätzliche Tests nötig machen
Aufbau hat Laufzeit in $O(n log(n))$, kann aber auf $O(nlog^2(n))$ beschleunigt werden wenn die AABBs in zwei etwa gleich große Gruppen geteilt werden und eine $O(nlog(n))$ Sortierung verwendet wird


