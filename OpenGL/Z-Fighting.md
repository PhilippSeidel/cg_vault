
Polygone, die sich in derselben Fläche überlagern, führen trotz Tiefenpuffer zu einem Flackern. 
Das geschieht wegen Rundungsfehlern. Dieses Flackern nennt man Z-Fighting.

![](z_fighting.png)

Um Z-Fighting zu verhindern werdem Primitive um einen kleinen Konstanten Offset $unit$ und um einen neigungsabhängigen Offset $factor * \varDelta z$ verschoben.

