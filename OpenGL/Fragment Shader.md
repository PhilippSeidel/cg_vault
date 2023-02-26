
![](fragment_shader.png)

Für jedes Fragment wird ein Fragment-Shader ausgeführt.
Eingabe-Attribute der Fragmente werden automatisch aus den Ausgaben früherer Shader interpoliert. (z.B. die Normale eines Fragments wird aus den Vertex-Normalen des [[Vertex Shader| Vertex Shaders]] interpoliert)

Berechnet wird im Fragment-Shader die **Farbe eines Pixels** und ein optionaler **Tiefenwert pro Fragment**. Das kann z.B. mit Phong-Shading erfolgen.

Die Ausgaben des Fragment-Shaders durchlaufen noch die [[Per-Fragment Operations]], bevor sie in den Framebuffer gespeichert werden.