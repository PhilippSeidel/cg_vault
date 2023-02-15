Rotationen werden von orthogonalen Matrizen dargestellt.

### Von 2D/3D-Rotationen um Hauptachsen

In 2D rotiert man mit folgender Matrix um den Winkel $\phi$:

$R(\phi) = \begin{pmatrix} cos(\phi) && -sin(\phi) \\ sin(\phi) && cos(\phi) \end{pmatrix}$

In 3D sehen die Rotationsmatrizen mit welchen man um die Hauptachsen rotierten kann so aus:
![](3D_mainaxis_rotation.png)


### Wie rotiert man die Vektoren einer Orthonormalbasis $\{u,v,w\}$ auf die Standardbasis $\{x,y,z\}$?

![](orthonormal_basis_rotation.png)

![](3D_mainaxis_rotation_details.png)

### Rotation um eine beliebige Achse

Wenn man um eine beliebige Achse $d = (d_x, d_y, d_z)\space(|d| = 1)$ rotieren möchte, dann wählt man zuerst d als einen Basisvektor einer Orthonormalbasis und berechnet die beiden anderen Basisvektoren wie folgt:
![](calc_orthonormal_basis_vector.png)

Dann berechnet man die Basiswechselmatrix M die einen Vektor bezüglich der $\{d,e,f\}$-Basis darstellt. Nach dieser Transformation benutzt man nun eine Rotationsmatrix, die um die entsprechende Koordinatenachse rotiert. Der dararus entstehende Vektor wird dann von $M^\top$ wieder in das Ausgangskoordinatensystem gebracht:

![](rotation_with_basis_change.png)


## Euler-Rotation

Die Euler-Rotation sagt aus, dass jede Rotation durch drei Rotationen um die Achsen x, y und z ausgedrückt werden kann. 
Dafür müssen die Achsen, sowie die drei **Euler-Winkel** $\psi, \theta \space und \space \phi$ gegeben sein.

Die Rotationsmatix ist dann $R = R_x(\phi) * R_y(\theta) * R_z(\psi)$.

Die kardanische Blockade ist Problem bei der Eulerrotation: die 1. und 3. Rotationsachse können  
zusammenfallen, d.h. nur Summe aus 1. und 3. Winkel ist relevant und  
es fehlt ein Freiheitsgrad.

![](gimbal_lock.png)
