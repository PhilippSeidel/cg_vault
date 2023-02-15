Ein Szenegraph ist eine gerichteter azyklischer Graph, der die hierarchische Struktur einer Szene beschreibt. Darin plaziert man Elemente relativ zu ihren Eltern, sodass sie sich implizit mitbewegen, wenn die Eltern sich bewegen.

### Matrix-Stacks

Matrix-Stacks sind eine Technik um die Wiederverwendbarkeit von Transformationsmatrizen beim Traversieren eines Szenengraphs zu gewährleisten. Dabei ist die oberste Matrix im Stack immer die aktuelle Transformation (z.B. von lokalen Koordinaten in Weltkoordinaten). 
Geht man beim Traversieren im Szenengraph eine Stufe nach unten, multipliziert man die aktuell oberste Matrix im Matrix-Stack mit der lokalen Eltern-zu-Kind-Transformationmatrix im Szenengraph. Damit erhält man als oberstes Element im Matrix-Stack die Kind-zu-Welt-Matrix. 
Geht man beim Traversieren im Szenengraph eine Stufe nach oben, löscht man das oberste Element auf dem Matrix-Stack.