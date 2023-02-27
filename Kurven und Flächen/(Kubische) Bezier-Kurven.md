Beschreibe eine Kurve durch ein kubisches Polynom. Definiert durch 4 Kontrollpunkte $b_i$. Kurve geht durch den ersten und den letzten Kontrollpunkt und approximiert die beiden anderen. Liegt innerhalb der konvexen Hülle ihrer Kontrollpunkte. Nutze [[Bernstein-Polynome]] als Gewicht.
![](kubische_bezier-kurve.png)
![](bezier-bernstein.png)
![](bezier-definition.png)
### Eigenschaften
![](bezier-eigenschaften1.png)
![](bezier-eigenschaften2.png)
![](bezier-eigenschaften3.png)


### Zeichnen einer Bezier-Kurve

#### Algorithmus 1
- Werte $F(u)$ an $m$ Stellen $u_j$ mit $u_j < u_{j+1}$ aus (mittels 
[[de Casteljau-Algorithmus]])
- Zeichne den Polygonzug $F(u_0)$,...,$F(u_{m-1})$
![](bezier_zeichnen_bsp_1.png)

#### Algorithmus 2
- Unterteile $F(u)$ in der parametrischen Mitte $u = \frac{1}{2}$ mittels des [[de Casteljau-Algorithmus]] in $F_l(u)$ und $F_r(u)$ 
- Führe rekursiv bis zu einer Rekursionstiefe $r$ fort
- zeichne die Kontrollpolygone der jeweils letzten Rekursion
![](bezier_zeichnen_bsp_2.png)