Beim Anwenden von Texturen nimmt man vorberechnete Bilder und passt diese "oder Ausschnitte/einzelne Pixel" an die Geometrie einer Oberfläche in der Szene an.
Damit ist man in der Lage mit vergleichsweise wenig aufwand hohe Detailgrade der Szene zu erreichen, auch wenn das unterliegende Dreiecksnetz eher grob ist.

Im Allgemeinen bezeichnet man die Pixel einer Textur als **Texel**. Für Texel verwendet man die Koordinaten $(s,t)$ anstatt $(x,y)$.

Es gibt verschieden Techniken auf die man beim Texturieren zurückgreifen kann:
- [[Texture Mapping]]
- [[Normal-Mapping|Bump-Mapping/Normal-Mapping]]
- Shadow-Mapping/Light-Maps
- [[Displacement-Mapping]]
- Diffuse Textur: Dabei wird der diffuse Anteil im Phong-Beleuchtungsmodell $k_d$ durch die Textur verändert.
- Gloss-Map: Dabei werden der spekulare Anteil $k_s$, sowie der Phong-Exponent $n$ durch die Textur verändert.
- [[Ambient Occlusion]]
