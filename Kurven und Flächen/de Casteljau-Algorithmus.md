Ein Algorithmus zur effizienten Auswertung und Unterteilung von [[(Kubische) Bezier-Kurven|Bezier-Kurven]].

### Effiziente Auswertung von Bezier-Kurven
Möglich durch rekursive Darstellung der [[Bernstein-Polynome]]:

## $B^n_i(u)=u\cdot B^{n-1}_{i-1}(u)+(1-u)\cdot B^{n-1}_i(u)$ 

![](deCasteljau-algo.png)
![](deCasteljau-beispiel.png)
![](deCasteljau-grafischeInterpretation.png)

### Unterteilung von Bezier-Kurven
![](deCasteljau_Unterteilung.png)


### de Casteljau Algorithmus für [[Tensorprodukt-Bezier-Flächen]] 
Wiederhole analog bilinieare Interpolation zur auswertug von Flächen.