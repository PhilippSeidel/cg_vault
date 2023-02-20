Um Texturkoordination unabhängig von der absoluten Breite/Höhe einer Textur angeben zu können verwendet man oft den Raum $[0,1]^2$. Texture Wrapping sind Techniken, wie man mit berechneten Texelwerten umgeht, die außerhalb dieses Raumes liegen. 

Hier gibt es die folgenden Techniken:
- Clamping: Bilde Texturkoordinaten auf den nähsten Randpunkt der Textur ab
- Repeating: Nutze Module-Arithmetik um Texturkoordinaten wieder auf $[0,1]^2$ abzubilden