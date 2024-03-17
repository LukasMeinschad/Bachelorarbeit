### Die B-Matrix

> Ein Set an 3N kartesischen Koordinaten $X$ kann über Wilson B-Matrix in Interne Koordinaten Transformiert werden


>$R = B * X$

Wichtig für gute Koordinaten bei Geometrieoptimisierung ist wenig Kupplung zwischen Koordinaten.

Kupplung spiegelt sich in hohen nichtdiagonalelementen der Hessian Matrix $H$ wieder.

> Interne Koordinaten geben haben Achsen für einzelne Platzierungen wie Bond Streching. Interne Koordinaten verhindern also sowohl harmonisch als auch anharmonisch die Kupplng

Betrachtet man interne Koordinaten $q = (q_1,q_2...q_n)^t$ so entsprechen Displacments $\Delta q$ genau Displacments $\Delta x$ durch die $B$ Matrix

$\Delta q = B \Delta x$

Wilson B-Matrix ist ebenfalls ein Indikator ob Koordinaten in q überflüssig sind, sonst wäre B linear unabhängig

### Kraftkonstanten Matrix

Potentielle Energie von Molekülen wird durch zweite Ableitung genähert

$f_{ij} = \frac{\delta^2 E}{\delta x_i \delta x_j}$

$F_{ij} = \frac{\delta E}{\delta r_i \delta r_j}$

Auch die Kraftkonstantenmatrix kann durch die Wilson B-Matrix umgewandelt werden

$F = (B^{-1})f B^{-1}$

$f = B^T F B$

#### Kinetic Energy Matrix and Treatment of Redundant internal Coordinates

Inverses von B wird über die kinetische Energie Matrix berechnet

$G = B m^{-1} B^T$

Wenn keine retudanten IC Sets vorliegen ist die G Matrix reel und symetrisch

$GK = KE$ kann diagonalisierung durchführen

$G^{-1} = Ke^{-1}K^T$

### Normal Moden

Die gewichtete kartesiche Kraftkonstante ist

$f' = (M^{-1/2})^T f M^{-1/2}$

Diese kann diagonalisiert werden

$\Lambda = L^T f' L$

Wobei $\Lambda$ diagonal ist und die Eigenwerte beinhaltet L ist die Matrix mit en Normalmoden als Eigenvektoren

Man kann auch eine $1$ Matrix mit Massengewichteten Normalmoden in Kartesischen Koordinaten erzeugen durch

$\Lambda = 1^T f 1$

wobei $1 = M^{-1/2}L$ 

Nun nutzen wir die B Matrix um die kartesische Kraftkonstante $f$ umzurechnen

$\Lambda = 1^T f 1 = 1^T (B^T F B)1$

Durch die Multiplikation von $B$ mit $1$ Matrix bekommt man die Normalmoden in der D Matrix

$D = B1$ diese Matrix hat Eigenvektoren in in internen Koordinaten

### Potential, Kinetic and Total Energy Distribution Matrices

Die harmonische Potentielle Energie V von internen Koordinaten ist

> $V = \frac{1}{2} \sum_m \sum_n F_{mn}R_mR_n$

die kinetische Energie wird beschrieben durch

> $T = \frac{1}{2} \sum_m \sum_n (G^{-1})_{mn}\dot{R_m}\dot{R_n}$

Die Umwandlung zwischen interne Koordinaten und normalen Koordinaten geht über

$R = DQ$

> Fazit man kann die Anteile an potentieller Energie und kinetischer Energie in einzelne Anteile einer Mode aufsplitten

$V^i = \frac{1}{2}Q_i^ \sum_i \sum_n D_{ni}D_{mi}F_{mn}$

$T^i =  \frac{1}{2}Q_i^2 \sum_m \sum_n D_{ni}D_{mi}(G^{-1})_{mn}$

Das sind dann die Einträge der PED und KED Matrix

### Vibrational Energy Distribution Matrix

Man kann also die Energyverteilung vereinfachen um nicht drei Matrizen für eine Mode zu bekommen.

Ein Weg ist alle Elemente aufzusummieren. Die Matrizen 35-37 sind numerisch ident und können berechnet werden durch

$P_m^i = T_m^i = E_m^i = D_{ik}(D^{-1})k_i$

In der VED Matrix sind die Spalten die Normalmoden und die Zeilen die Internen Koordinaten, jedoch kann man einzelne Anteile nicht mehr Nachmessen.

### Intristiscche Vibrational Frequencies

Diese wird durch die Kontribution aller Normalmoden zu einer internen Koordinate beschrieben

$v_n = \sum_n \sum_i P^i_{mn} \lambda_i$


$v_n = \sum_n \sum_i = \frac{D_{mi}F_{mn}D_{ni}}{\lambda_i}\lambda_i = \sum_m \sum_i D_{mi}F_{mn}D_{ni}$


