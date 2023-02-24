Insbesondere bei dynamischen Szenen müssen räumliche Datenstrukturen oft neu berechnet werden. Paralleles Berechnen hilft.
### Optimierung durch Vorsortierung
- Quantisiere Primitivschwerpunkte
- Weise Zellen [Morton Codes](https://en.wikipedia.org/wiki/Z-order_curve) zu
- Sortiere Primitive nach Zellcodes
--> ergibt implizite Baumstruktur
![](morton.png)
![](morton_tree.png)
- Große Primitive sind shite und machen alles kaputt