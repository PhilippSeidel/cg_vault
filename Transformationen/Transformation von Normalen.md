
Normalen sind **Bi-Vektoren**. Das bedeutet sie sind durch die Orthogonalität zu einer Tangentialfläche (2D-Ebene) definiert, und nicht durch die Differenz zweier anderer Vektoren.
Da lineare und affine Transformationen im Allgemeinen nicht winkeltreu sind, muss man Normalen gesondert betrachten.

Normale werden mit der invers-transponierten Matrix der (eigentlichen) Transformationsmatrix transformiert:
![](normal_transformation.png)

In der Theorie ist die Idee also, die gerade Orthogonalität der Normalen $n$ zur Ebene $t$ auszunutzen, und aus den transformierten Punkten $P1$ und $P2$ die normale neu zu berechnen.
In der Praxis verwendet man, wie oben angebildet, die Matrix $(M^{-1})^\top$.

