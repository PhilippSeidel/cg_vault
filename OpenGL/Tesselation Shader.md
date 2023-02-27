
![](tesselation_shader.png)

### Primitive Assembly
Zwischen dem [[Vertex Shader]] und dem **Tesselation-Shader** gibt es noch die Pipeline-Stufe der **Primitive Assembly**. Diese Stufe nimmt n Vertices und konstuiert daraus ein geometrisches Primitiv.
Sie ist **nicht programmierbar**.

### Tesselation

Die Tesselation ist **optional**. Sie besteht ebenfalls aus mehreren Schritten:
- Der Tesselation Control Shader (bestimmt die Unterteilung)
- Tesselator (nicht programmierbar, nimmt die Unterteilung vor)
- Tesselation Evaluation Shader (berechnet Vertices der erzeugten Geometrie)

Die Tesselation zerlegt das aus den n Vertices generierte Primitiv in kleinere und feinere Dreiecke. Auf diese Weise entsteht ein feineres Dreicksnetz. Die weitergegebenen m Dreiecke bilden auch nach der Tesselation noch ein Primitiv.

Man nutzt **Tesselation** für **parametrische Flächen** und für [[Displacement-Mapping]]. 
