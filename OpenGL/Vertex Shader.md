
![](vertex_shader.png)

Vertex-Shader sind komplett frei **programmierbar**.

Ein Vertex Shader wird immer mit einem Vertex als Parameter aufgerufen. Er wendet eine **Transformation** auf diesen Vertex an und übergibt ihn der nächsten Stufe der Pipeline.

Dabei ist ein Vertex-Shader weder in der Lage neue Vertices zu erzeuge, oder bestehende zu löschen.

### Attributeberechnung
Im Vertex Shader können zusätzlich zur Transformation noch Attribute berechnet werden, die für spätere Pipeline-Stufen interessant sind.
Ein wichtiges Beispiel hierfür ist die Interpolation von Normalen.

### Shading
Möchte man Gouraud-Shading implementieren, dann tut man das normalerweise im Vertex-Shader. Ansonsten nutzt man die hier interpolierten Normalen später in der Pipeline, z.B im [[Fragment Shader]] zum Phong-Shading.