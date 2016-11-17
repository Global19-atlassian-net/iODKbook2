
Tensor Product as a Matrix of a Linear Transformation
-----------------------------------------------------

.. Zbiór :math:`\ M_{m\times n}(K)\ ` macierzy prostokątnych o :math:`\,m\ `
   wierszach i :math:`\,n\ ` kolumnach nad ciałem :math:`\,K\ ` jest 
   przestrzenią wektorową nad tym ciałem ze względu na dodawanie macierzy
   i mnożenie ich przez skalary z :math:`\,K.`

Ze względu na dodawanie macierzy i mnożenie ich przez skalary, 
zbiór :math:`\ M_{m\times n}(K)\ ` macierzy prostokątnych o :math:`\,m\ `
wierszach i :math:`\,n\ ` kolumnach nad ciałem :math:`\,K\ ` jest 
:math:`\ mn`-wymiarową przestrzenią wektorową nad tym ciałem. 
Naturalną (dalej: kanoniczną) bazą jest układ macierzy

.. math::
   
   \mathcal{E}_{m\times n}\ =\ 
   \left(\ \boldsymbol{E}_{11},\ \boldsymbol{E}_{12},\ 
   \ldots,\ \boldsymbol{E}_{1n},\ \ 
   \boldsymbol{E}_{21},\ \boldsymbol{E}_{22},\ 
   \ldots,\ \boldsymbol{E}_{2n},\ \ 
   \ldots,\ \ \boldsymbol{E}_{m1},\ \boldsymbol{E}_{m2},\ 
   \ldots,\ \boldsymbol{E}_{mn}\,\right)

   \left(\boldsymbol{E}_{ij}\right)_{\,|\,kl}\ =\ \ 
   \delta_{ik}\ \delta_{jl}\,,
   \qquad
   \begin{array}{l}
   i,k=1,2,\ldots,m, \\
   j,l=1,2,\ldots,n.
   \end{array}

Każda macierz :math:`\ \boldsymbol{A} \in M_{m\times n}(K)\ ` 
może być teraz przedstawiona w bazie :math:`\ \mathcal{E}_{m\times n}:`

.. math::
   
   \boldsymbol{A}\ =\ [a_{ij}]_{m\times n}\ =\ \,
   \displaystyle\sum_{i=1}^m \displaystyle\sum_{j=1}^n\ 
   a_{ij}\ \boldsymbol{E}_{ij}\,.

Niech :math:`\ \boldsymbol{\Lambda}^{mn}(\boldsymbol{A})\ ` 
oznacza wektor kolumnowy utworzony przez kolejne wiersze macierzy 
:math:`\ \boldsymbol{A}:`

.. math::
   
   \boldsymbol{\Lambda}^{mn}(\boldsymbol{A})\ :\,=\ 
   \left[\ a_{11}\ a_{12}\ \ldots\ a_{1n}\ \ a_{21}\ a_{22}\ \ldots\ a_{2n}\ \ 
   \ldots\ \ a_{m1}\ a_{m2}\ \ldots\ a_{mn}\,\right]^T\ 
   \in\ K^{mn}.

Tak zdefiniowany wektor :math:`\ \boldsymbol{\Lambda}^{mn}(\boldsymbol{A})\ `
jest kolumną współrzędnych macierzy :math:`\ \boldsymbol{A}\ ` w bazie 
:math:`\ \mathcal{E}_{m\times n}\,.`

**Przykład.** :math:`\\` 
W przestrzeni :math:`\ M_{2\times 3}(Q)\ ` bazą kanoniczną jest
:math:`\ \mathcal{E}_{2\times 3}\ =\ 
\left(\,\boldsymbol{E}_{11},\ \boldsymbol{E}_{12},\ \boldsymbol{E}_{13},\ 
\boldsymbol{E}_{21},\ \boldsymbol{E}_{22},\ \boldsymbol{E}_{23}\,\right)`:

.. math::
   
   \begin{array}{lll}
   \boldsymbol{E}_{11}\ =\ 
   \left[\begin{array}{ccc} 
   1 & 0 & 0 \\ 0 & 0 & 0
   \end{array}\right], 
   &
   \boldsymbol{E}_{12}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 1 & 0 \\ 0 & 0 & 0
   \end{array}\right],
   &
   \boldsymbol{E}_{13}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 0 & 1 \\ 0 & 0 & 0
   \end{array}\right]
   \\[12pt]
   \boldsymbol{E}_{21}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 0 & 0 \\ 1 & 0 & 0
   \end{array}\right],
   &
   \boldsymbol{E}_{22}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 0 & 0 \\ 0 & 1 & 0
   \end{array}\right],
   &
   \boldsymbol{E}_{23}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 0 & 0 \\ 0 & 0 & 1
   \end{array}\right]
   \end{array}

Dla macierzy :math:`\ \boldsymbol{A}\ =\ 
\left[\begin{array}{ccc} 1 & 2 & 3 \\ 4 & 5 & 6 \end{array}\right]\ `
wektor 
:math:`\ \boldsymbol{\Lambda}^{23}(\boldsymbol{A})\ =\ 
\left[\begin{array}{c} 1 \\ 2 \\ 3 \\ 4 \\ 5 \\ 6 \end{array}\right].`

Niech będą dane macierze 
:math:`\ \boldsymbol{A} = [a_{ij}]_{m\times n}\in M_{m\times n}(K)\ ` oraz
:math:`\ \boldsymbol{B} = [b_{ij}]_{p\times q}\in M_{p\times q}(K).\ ` 
:math:`\\`
Wtedy, :math:`\,` jeżeli 
:math:`\ \boldsymbol{G} = [g_{ij}]_{n\times q}\in M_{n\times q}(K),\ ` to
:math:`\ \boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T\in M_{m\times p}(K).`

Odwołując się do własności iloczynu macierzowego można łatwo uzasadnić,
że odwzorowanie

.. math::
   :label: homo
   
   F_{AB}\,:\qquad 
   M_{n\times q}(K)\ni\boldsymbol{G}\ \ \mapsto\ \ F_{AB}(\boldsymbol{G}) :\,=
   \boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T\in M_{m\times p}(K)

jest liniowe, czyli jest homomorfizmem przestrzeni wektorowych:

.. math::
   
   F_{AB}\ \in\ \text{Hom}\left(M_{n\times q}(K),\,M_{m\times p}(K)\right).

Przyjmując oznaczenie :math:`\boldsymbol{H}\ =\ [h_{ij}]_{m\times p}\ =\ 
\boldsymbol{A}\,\boldsymbol{G}\,\boldsymbol{B}^T\ ` otrzymujemy

.. math::
   
   h_{ij}
   \ =\ \displaystyle\sum_{v=1}^n\sum_{w=1}^q a_{iv}\ g_{vw}\ b^T_{wj}
   \ =\ \displaystyle\sum_{v=1}^n\sum_{w=1}^q (a_{iv}\,b_{jw})\ g_{vw}
   \ =\ \displaystyle\sum_{v=1}^n\sum_{w=1}^q 
   (\boldsymbol{A}\otimes\boldsymbol{B})_{\,|\,ij,\,vw}\ g_{vw}
   
   \text{gdzie}\quad i=1,2,\ldots,m;\ j=1,2,\ldots,p.

A zatem dla dowolnych macierzy 
:math:`\ \boldsymbol{G}\in M_{n\times q}(K),\,`
:math:`\,\boldsymbol{H}\in M_{m\times p}(K):`

.. math::
   
   \boldsymbol{H}\ =\ F_{AB}(\boldsymbol{G})
   \quad\Leftrightarrow\quad
   \boldsymbol{\Lambda}^{mp}(\boldsymbol{H})\ \,=\ \,
   (\boldsymbol{A}\otimes\boldsymbol{B})\ \cdot\ 
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G}),

co oznacza, że iloczyn prosty :math:`\ \boldsymbol{A}\otimes\boldsymbol{B}\ `
jest macierzą homomorfizmu :math:`\ F_{AB}\ ` danego przez :eq:`homo`
w bazach kanonicznych 
:math:`\ \mathcal{E}_{n\times q}\ ` i :math:`\ \mathcal{E}_{m\times p}\ `
przestrzeni :math:`\ M_{n\times q}(K)\ ` i :math:`\ M_{m\times p}(K).`
   
Wykorzystamy teraz wyprowadzone zależności do ponownego udowodnienia
niektórych własności iloczynu prostego macierzy.

Stwierdziliśmy, że jeżeli dane są macierze 
:math:`\ \boldsymbol{A}\in M_{m\times n}(K)\ ` oraz 
:math:`\ \boldsymbol{B}\in M_{p\times q}(K),\ ` :math:`\\` 
to dla dowolnej macierzy :math:`\ \boldsymbol{G}\in M_{n\times q}(K):`

.. math::
   :label: main
   
   \blacktriangleright\quad
   (\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\ \,=\ \,
   \boldsymbol{\Lambda}^{mp}
   (\boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T).

Podstawiając w :eq:`main` 
:math:`\ \boldsymbol{A}\to\boldsymbol{A}_1 + \boldsymbol{A}_2\,,\ ` gdzie 
:math:`\ \boldsymbol{A}_1,\ \boldsymbol{A}_2 \in M_{m\times n}(K),\ `
otrzymamy

.. math::
   
   \begin{array}{ll}
   \left[\,(\boldsymbol{A}_1 + \boldsymbol{A}_2)\otimes\boldsymbol{B}\,\right]
   \,\cdot\,\boldsymbol{\Lambda}^{nq}(\boldsymbol{G}) & 
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,(\boldsymbol{A}_1 + \boldsymbol{A}_2)\ 
   \boldsymbol{G}\,\boldsymbol{B}^T\,\right]\ =
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}_1\,\boldsymbol{G}\,\boldsymbol{B}^T + \,
   \boldsymbol{A}_2\,\boldsymbol{G}\,\boldsymbol{B}^T\right)\ =
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}_1\,\boldsymbol{G}\,\boldsymbol{B}^T\right)\ +\ 
   \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}_2\,\boldsymbol{G}\,\boldsymbol{B}^T\right)\ =
   \\[6pt] &
   =\ \ (\boldsymbol{A}_1\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\ +\ 
   (\boldsymbol{A}_2\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\ =
   \\[6pt] &
   =\ \ \left[\,(\boldsymbol{A}_1\otimes\boldsymbol{B})\ +\ 
   (\boldsymbol{A}_2\otimes\boldsymbol{B})\,\right]\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})
   \end{array}

dla dowolnej macierzy :math:`\ \boldsymbol{G}\in M_{n\times q}(K).\ `
Podstawiając w miejsce :math:`\ \boldsymbol{G}\ ` kolejne macierze 
bazy kanonicznej: :math:`\ \boldsymbol{G} = \boldsymbol{E}_{11},\ 
\boldsymbol{E}_{12},\ \ldots,\ \boldsymbol{E}_{nq}\,,\ ` stwierdzamy
równość odpowiednich kolumn macierzy 
:math:`\ (\boldsymbol{A}_1 + \boldsymbol{A}_2)\otimes\boldsymbol{B}\ `
oraz :math:`\ (\boldsymbol{A}_1\otimes\boldsymbol{B})\ +\ 
(\boldsymbol{A}_2\otimes\boldsymbol{B})\,,\ ` co oznacza równość
samych macierzy:

.. math::
   
   (\boldsymbol{A}_1 + \boldsymbol{A}_2)\otimes\boldsymbol{B}\ \,=\ \,
   (\boldsymbol{A}_1\otimes\boldsymbol{B})\ +\ 
   (\boldsymbol{A}_2\otimes\boldsymbol{B})\,.

Podobnie przebiega dowód rozdzielności iloczynu prostego względem
dodawania w drugim czynniku macierzowym oraz dowód jednorodności:

.. math::
   
   \boldsymbol{A}\otimes(\boldsymbol{B}_1\ +\ \boldsymbol{B}_2)\ \,=\ \,
   (\boldsymbol{A}\otimes\boldsymbol{B}_1)\ +\ 
   (\boldsymbol{A}\otimes\boldsymbol{B}_2)\,,

   (\gamma\,\boldsymbol{A})\otimes\boldsymbol{B}\ =\
   \boldsymbol{A}\otimes(\gamma\,\boldsymbol{B})\ =\ 
   \gamma\ (\boldsymbol{A}\otimes\boldsymbol{B}),\quad\gamma\in K.
   
Dla udowodnienia wzoru :eq:`mixed-product` podstawiamy w równaniu :eq:`main` :

.. math::
   
   \begin{array}{lr}
   \boldsymbol{A}\to\boldsymbol{A}\,\boldsymbol{C},\ \ &
   \begin{array}{r}
   \boldsymbol{A}\ :\ m \times r \\
   \boldsymbol{C}\ :\ r \times n
   \end{array};
   \end{array}
   \qquad
   \begin{array}{ll}
   \boldsymbol{B}\to\boldsymbol{B}\,\boldsymbol{D},\ \ &
   \begin{array}{l}
   \boldsymbol{B}\ :\ p \times s \\
   \boldsymbol{D}\ :\ s \times q
   \end{array}:
   \end{array}
   \\[8pt]
   \begin{array}{ll}
   \left[\,(\boldsymbol{A}\boldsymbol{C})\otimes
   (\boldsymbol{B}\boldsymbol{D})\,\right]\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G}) & 
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,(\boldsymbol{A}\boldsymbol{C})\ \boldsymbol{G}\ 
   (\boldsymbol{B}\boldsymbol{D})^T\,\right]\ \ =\ 
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,\boldsymbol{A}\ 
   (\boldsymbol{C}\boldsymbol{G}\boldsymbol{D}^T)\ 
   \boldsymbol{B}^T\,\right]\ \ =
   \\[6pt] &
   =\ \ (\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{rs}
   (\boldsymbol{C}\boldsymbol{G}\boldsymbol{D}^T)\ \ =
   \\[6pt] &
   =\ \ (\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
   \left[\,(\boldsymbol{C}\otimes\boldsymbol{D})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\,\right]\ \ =
   \\[6pt] &
   =\ \ \left[\,(\boldsymbol{A}\otimes\boldsymbol{B})\cdot
   (\boldsymbol{C}\otimes\boldsymbol{D})\,\right]\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G}).
   \end{array}

Ponieważ macierz :math:`\ \boldsymbol{G}\in M_{n\times q}(K)\ `
jest dowolna, wynika stąd równość macierzowa

.. math::
   
   (\boldsymbol{A}\boldsymbol{C})\otimes
   (\boldsymbol{B}\boldsymbol{D})\ =\ 
   (\boldsymbol{A}\otimes\boldsymbol{B})\ 
   (\boldsymbol{C}\otimes\boldsymbol{D})\,,

którą należało udowodnić.




