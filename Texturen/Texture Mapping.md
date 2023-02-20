
### Planare Projektion

Bei der planaren Projektion geht man von einer Ebene aus die vom Punkt $p$ und den Vektoren $\overrightarrow{s}, \space \overrightarrow{t}$ aufgespannt werden.

Um einen Punkt einer Oberfläche $x$ auf die Texel-Koordianten $(s,t)$ einer Textur abzubilden verwendent man dann folgende Abbildungsvorschrift:
- $s = (x - p) \space * \space \overrightarrow{s}$ 
- $t = (x-p) \space * \space \overrightarrow{t}$ 

![](texture_planar_projection.png)

Auf diese Weise lassen sich auch **eindimensionale** Texturen auf **dreidimensionale**  Oberflächen mappen, indem man nur eine der obigen Berechnungsvorschriften anwendet.

### Kugel-Parametrisierung

Bei der Kugel-Parametrisierung wird die Textur wie eine Kugel um den zu texturierenden Körper angeordnet.
Hier nutzt man aus, dass sich die Punkte auf der Oberfläche einer Kugel durch Polarkoordinaten $(r, \phi, \theta)$ (r ist fest) darstellen lassen. Man berechnet die Texturkoordiante wie folgt:
$\begin{pmatrix} s \\ t \end{pmatrix} \coloneqq \begin{pmatrix} \theta / 2 \pi \\ \phi / \pi \end{pmatrix}$   

![](sphere_parametrization.png)

Dabei kann es zu (starken) Verzerrungen der Textur kommen.

### Zylinder-Parametrisierung

Bei der Zylinder-Parametrisierung wird die Textur wie ein Zylinder um den zu texturierenden Körper angeordnet.
Hier benutzt man Zylinder-Koordination: $(r, \phi, \gamma)$ und berechnet die Texturkoordination wie folgt: $\begin{pmatrix} s \\ t \end{pmatrix} \coloneqq \begin{pmatrix} \theta / 2 \pi \\ \gamma / h \end{pmatrix}$ 

![](zylinder_parametrization.png)

Auch hier kann es zu Verzerrungen kommen.

### Würfel-Parametrisierung

Bei der Würfel-Parametrisierung konstruiert man einen Würfel, in dem jede Seite eine Instanz der selben Textur ist. Dieser Würfel "umgibt" das zu texturierende Objekt. Um einen gesuchten Texel zu finden schießt man einen Strahl aus der Würfelmitte durch den enstprechendne Oberflächenpunkt des zu texturierenden Objekts und schaut wo der Strahl den Würfel schneidet.

![](cube_parametrization.png)


### Weitere Abbildungen 
Die oben vorgestellten Parametrisirungen verwenden alle eine Hilfsfläche (Ebene, Zylinder etc.).
Es gibt auch andere Arten von Abbildungen:

![](texture_functions.png)


### Aliasing

Beim Texture-Mapping kann [[Aliasing]] auftreten. 

![](texture_projection_aliasing.png)

Es entsteht beim Projezieren einer 2D-Textur in den dreidimensionalen Raum. Entscheidend dafür ist das Verhältniss der Abtastfrequenz am Bildschirm zur Auflösung der projezierten Textur.
Um [[Aliasing]] in solchen Fällen zu vermeiden verwendet man [[Texturfilterung]].