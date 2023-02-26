![](geometry_shader.png)

### Geometry Shader
Der **Geometry Shader** ist **optional** und **frei programmierbar**. 
Er bearbeitet einzelne Primitive. Diese kann er **vervielfachen, entfernen oder umwandeln**.
Dabei kann er auch auf benachbarte Primitive zugreifen, falls diese zur Verfügung gestellt werden.

### Clipping
Das [[Clipping]] ist nicht programmierbar.
Hierbei werden unsichtbare Punkte verworfen und abgeschnittenen Primitiven werden neue Punkte  hinzugefügt. 

### Rasterisierung
Der Rasterisierungsschritt generiert Fragmente aus den Primitiven, die dann an den [[Fragment Shader]] weitergegeben werden.