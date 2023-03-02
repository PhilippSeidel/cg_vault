Definiere komplexe Objekte durch sukzessives Ersetzen von Teilen eines einfacheren Objekts durch Ersetzungsregeln. Ähnlich zu Chomskys formalen Grammatiken.
![](L-System.png)
Zusätzlich braucht man noch eine Interpretationsvorschrift
![](D0L-System.png)
![](ableitung_D0L.png)


### Turtle-Grafik
"Schildkröte" ist ein Cursor mit (x,y)-Position und Richtung $\alpha$. Wird eine Schrittweite d und ein Winkelinkrement $\sigma$ vorgegeben, dann kann die Schildkröte mit wenigen Kommandos gesteuert werden.
![](turtle.png)
![](turtle2.png)


### Verzweigungen
Das Alphabet wird um die zwei Symbole "[" und "]" erweitert. Eckige klammer auf sichert den aktuellen Zustand (x,y,$\alpha$) auf einem Stack. Eckige Klammer zu holt den letzten gesicherten Zustand vom Stack.
![](verzweigungen.png)



### In der Praxis
Rein Algorithmische erzeugung ist schwer und erfordert viel Erfahrung. Deshalb nutzt man oft parametrisierte, stochastische Ersetzungsregeln.


### Stochastische/Parametrisierte L-Systeme
![](stochastische_L-Systeme.png)
