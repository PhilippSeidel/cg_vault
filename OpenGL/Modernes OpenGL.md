Die API die durch modernes OpenGL bereitgestellt wird ist wesentlich flexibler als die API die durch [[Klassisches OpenGL|klassisches OpenGL]] bereitgestellt wird.
Einige Konzepte wie der Immediate-Mode oder Hilfsfunktionen (z.B. Matrix-Stacks) gibt es nicht mehr.

Auch gibt es keine sog. **Fixed-Function-Pipeline** mehr. Das heißt es gibt keine Standardverarbeitung mehr, sondern die einzelnen Pipeline-Stufen sind **frei programmierbar**.

Damit ist z.B. die Beleuchtungsberechnung selbst implementierbar und nicht mehr auf einen Standard festgelegt.

Die OpenGL-Pipeline in modernem OpenGL sieht wie folgt aus:
![](modern_opengl_pipeline.png)

Einige dieser Stufen sind (voll oder teilweise) programmierbar. Andere können nicht frei programmiert werden:

- [[Vertex Shader]] (Geometrieverarbeitung)
- [[Tesselation Shader]] (Geometrieverarbeitung)
- [[Geometry Shader]] (Geometrieverarbeitung)