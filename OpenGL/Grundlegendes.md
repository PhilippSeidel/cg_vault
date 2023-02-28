
**OpenGL** ist eine plattformunabhängige und hardwareunabhängige 3D Rendering API.

Es gibt zwei Api-Ebenen:
- High-level API $\rightarrow$ Grafik-Pipeline
- Low-level $\rightarrow$ keine höheren Modellierungskonzepte, kein [[Szenengraph]]
Im Immediate-Mode bewirk ein Befehl sofortiges rendern.

Außerdem ist OpenGL eine **Zustandmaschine**. Das bedeutet man kann den Zustand der "Grafikmaschine" für einen Rendering-Durchlauf anpassen.

Man kann OpenGl auch als **Client-Server-Konzept** begreifen. Dabei ist die Anwendung der Client und der Grafiktreiber und die Grafikkarte sind der Server.

Es gibt auch die Unterscheidung zwischen [[Klassisches OpenGL|klassischem OpenGL]] und [[Modernes OpenGL|modernem OpenGL]].
In klassischem OpenGL ist die Grafik-Pipeline nur **konfigurierbar**.
In modernem OpenGL ist die Grafik-Pipeline in (einigen) Stufen **frei programmierbar** mit sog. Shadern.