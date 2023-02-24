Wie unterteilt man einen Raum am besten in zwei Regionen?

### Ziel
- Identifiziere kompakte, dichtbesetzte Regionen
	- Großer Aufwand nur wenn Strahl diese auch wirklich trifft
- Trenne dünnbesetzte Regionen ab




## Kosten für das Traversieren eines Knotens eines  [[kD-Bäume|kD-Baum]]s oder einer [[Bounding Volume Hierarchy (BVH)|BVH]]
## $C_T = C_D + P(treffe(L))C(L) + P(treffe(R))C(R)$
$C_D$ : Kosten für Entscheidung mit welchem kindknoten fortgefahren wird (in der Vorlesung $C_T$ aber das ist geistig behindert weil die gleiche Variable später (siehe unten) was anderes bedeutet)
$P$ : Wahrscheinlichkeit
$L$ : Linker Teilraum
$R$ : Rechter Teilraum



## Kosten für das Unterteilen eines Knotens $p$ in einem [[kD-Bäume|kD-Baum]] oder eines [[Bounding Volume Hierarchy (BVH)|BVH]]-Knotens
## $C = C_T + \frac{SA(B_l)}{SA(B_p)}|P_l|C_i + \frac{SA(B_r)}{SA(B_p)}|P_r|C_i$
$B_l, B_r, B_p$ : Bounding Boxes der Primitive in den Kindknoten und im betrachteten Knoten $p$
$|P_l|$ und $|P_r|$ : Anzahl der Primitive im linken und rechten Kindknoten
$C_i$ : Kosten eines Strahl-Primitiv-[[Ray intersecion|Schnitttests]]
$C_T$ : Kosten der Traversierung eines Knotens (siehe oben)


**Ziel**: finde unterteilung die die Kostenfunktion minimiert
![](gut_schlecht.png)


## Optimierung / Bestimmung der Unterteilung

### Approximative Konstruktion (nicht coolio)
- Bau zufällige Unterteilungskandidaten
- Bestimme für jeden wie gut die sind, nimm besten

### Konstruktion mit inkrementeller Berechnung
- Sortiere die n Primitive nah x-,y-,z-Achse
- Teste jede der möglichen 3(n - 1) Aufteilungen
- inkrementelle Berechnung der [[AABB]]s und damit vergleichsweise effiziente Berechnung der SAH möglich
- 