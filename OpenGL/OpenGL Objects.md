
OpenGL-Objekte sind **keine** Objekte im OOP-Sinn. OpenGL-Objekte sind Texturen, Geometrie oder Shader.

![](opengl_objects_management.png)


## Buffer Objects

Man unterscheidet zwei unterschiedliche Typen von Buffern: 
- **Vertex Buffer**: Speichert Vertices und und deren Attribute
- **Index Buffer**: Speichert an einer Position eine Menge von Indizes. Diese Indizes zeigen auf Elemente in einem zugehörigen Vertex-Buffer.

Einen **Vertex Buffer** und den zugehörigen **Index Buffer** (falls vorhanden) nennt man zusammengefasst ein **Vertex Array Object**.

### Buffer Object Mapping

Beim Buffer-Object-Mapping wird ein Buffer zunächst angelegt, ohne ihn mit Daten zu füllen.
Dabei kann ein Buffer in den Hauptspeicher "eingeblendet" werden.

### Index Face Set / Shared Vertex -Darstellung eines Dreiecksnetzes

Bei der Darstellung eines Dreiecksnetzes verwendet man ein **Vertex Array Object**. Dies erlaubt es jeden Vertex nur einmal zu speichern, anstatt ihn für jedes Dreieck einmal zu speichern. Die Dreiecke werden dann im **Index Buffer** zusammengesetzt. 
Damit muss man weniger Daten speichern.

## Vertex Cache

GPUs haben einen Cache für Speicherzugriffe auf Vertices. Allerdings funktioniert dieser nur für **Vertex Array Objects** mit **Index Buffern**. 
Der Cache speichert die Indizes bezüglich eines **Vertex Buffers**, also die Indizes, die aus dem **Index Buffer** ausgelesen werden.
