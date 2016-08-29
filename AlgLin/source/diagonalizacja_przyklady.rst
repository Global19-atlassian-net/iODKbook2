Przykłady diagonalizacji macierzy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Przykład 0.**

Pokazać, że macierzy :math:`\ \boldsymbol{A}\ =\ 
\left[\begin{array}{cc} 1 & a \\ 0 & 1 \end{array}\right]
\in M_2(R),\quad a\neq 0,\ ` nie można zdiagonalizować
poprzez przekształcenie podobieństwa, :math:`\ ` czyli że 
nie istnieje nieosobliwa macierz :math:`\ \boldsymbol{P}\ ` taka, że

.. math::
   :label: simil
   
   \boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P}\ =\ \boldsymbol{D}

gdzie :math:`\ \boldsymbol{D}\ ` jest macierzą diagonalną.

**Dowód.**

**I.** :math:`\,` Macierz :math:`\,\boldsymbol{A}\in M_n(K)\,` 
może być doprowadzona do postaci diagonalnej poprzez przekształcenie podobieństwa :eq:`simil` wtedy i tylko wtedy, gdy jej wektory własne 
rozpinają przestrzeń :math:`\,K^n,\ ` czyli gdy w przestrzeni :math:`\,K^n\,` 
istnieje baza, złożona z wektorów własnych macierzy :math:`\,\boldsymbol{A}.`

Równanie charakterystyczne macierzy :math:`\,\boldsymbol{A}:`

.. math::
   
   \det{(\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)}\ =\ 
   \left|\begin{array}{cc} 1-\lambda &a \\ 0 & 1-\lambda \end{array}\right|\ =\ 
   (1-\lambda)^2 =\,0

dostarcza jedną, algebraicznie podwójną, wartość własną :math:`\,\lambda=1.`

Wektory własne :math:`\,\boldsymbol{x}\,` dla tej wartości wyznaczamy z równania
:math:`\ (\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)\,\boldsymbol{x}\,=\,
\boldsymbol{0},\ ` czyli

.. math::
   
   \left[\begin{array}{cc} 0 & a \\ 0 & 0 \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right]\ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right]
   \quad : \quad
   \begin{cases} 
   \ \ x_1 \text{  -  dowolne,} \\ \ \ a\,x_2=0\,;  
   \end{cases}
   \ : \quad
   \begin{cases} 
   \ \ x_1 \text{  -  dowolne,} \\ \ \ x_2=0\,.  
   \end{cases}
   \,,

Wektory własne są więc postaci

.. math::
   
   \boldsymbol{x}\,=\,
   \left[\begin{array}{c} \beta \\ 0 \end{array}\right]\ =\ 
   \beta\ \left[\begin{array}{c} 1 \\ 0 \end{array}\right],\quad
   \beta\in R\setminus\{0\}

i tworzą (razem z wektorem zerowym) 1-wymiarową podprzestrzeń: 
krotność geometryczna wartości własnej :math:`\,\lambda=1\,` 
wynosi 1 :math:`\,` i :math:`\,` jest różna od krotności algebraicznej.

Nie istnieje więc baza przestrzeni :math:`\,R^2,\ ` złożona z wektorów własnych 
macierzy :math:`\,\boldsymbol{A},\ ` gdyż dowolne dwa wektory własne tej 
macierzy są liniowo zależne. Stąd nie istnieje również nieosobliwa macierz 
:math:`\,\boldsymbol{P},\ ` diagonalizująca macierz :math:`\,\boldsymbol{A}.`

**II.** :math:`\,` Macierze podobne mają taki sam wielomian charakterystyczny,
a więc również taki sam zbiór wartości własnych o takich samych odpowiednich krotnościach algebraicznych.

Łatwo widać, że macierz :math:`\,\boldsymbol{A}\,` ma jedną wartość własną
:math:`\,\lambda=1\,` o krotności algebraicznej 2.

Gdyby istniała nieosobliwa macierz :math:`\,\boldsymbol{P}\,` 
spełniająca warunek :eq:`simil`, :math:`\,` to macierz 
:math:`\,\boldsymbol{D}\,` w tym równaniu byłaby diagonalną macierzą 2. stopnia 
o podwójnej algebraicznie wartości własnej :math:`\,\lambda=1.\ ` 
Warunki te określają jednoznacznie macierz jednostkową: 
:math:`\ \boldsymbol{D}\,=\,\boldsymbol{I}_2.` 

W konsekwencji byłoby
:math:`\ \boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P}\ =\ 
\boldsymbol{I}_2,\ ` skąd :math:`\ \boldsymbol{A}\,=\,
\boldsymbol{P}\,\boldsymbol{I}_2\boldsymbol{P}^{-1}\ =\ 
\boldsymbol{P}\boldsymbol{P}^{-1}\ =\ \boldsymbol{I}_2.`

Doszliśmy do sprzeczności, 
bo :math:`\ \boldsymbol{A}\neq\boldsymbol{I}_2.\ `
Nie istnieje więc macierz :math:`\,\boldsymbol{P}\,` spełniająca :eq:`simil`.

**Przykład 1.**

Macierz :math:`\ \boldsymbol{\sigma}_x\,=\,
\left[\begin{array}{cc} 0 & 1 \\ 1 & 0 \end{array}\right]\in M_2(C)\ `
jest rzeczywista i symetryczna, a więc hermitowska.
Sprawdzimy, że:

* jej wartości własne są rzeczywiste,
* wektory własne, należące do różnych wartości, są ortogonalne,
* dla każdej wartości własnej krotność algebraiczna równa się
  krotności geometrycznej,
* w przestrzeni :math:`\,C^2\,` istnieje ortonormalna baza, 
  złożona z jej wektorów własnych,
* można ją zdiagonalizować poprzez rzeczywistą transformację ortogonalną.

Równanie charakterystyczne macierzy :math:`\,\boldsymbol{\sigma}_x\,:`

.. math::
   
   w(\lambda)\,=\,
   \left|\begin{array}{cc}
   -\lambda & 1 \\ 1 & -\lambda
   \end{array}\ \right|\ =\ 
   (-\lambda)^2-1\ =\ \lambda^2-1\ =\ (\lambda-1)(\lambda+1)\ =\ 0

daje dwie wartości własne i ich krotności algebraiczne:

.. math::
   
   \lambda_1\,=\ 1\quad(1)\,,\qquad\lambda_2\,=\ -1\quad(1)\,.

Podstawiając kolejno wyliczone wartości własne do równania

.. math::
   
   (\boldsymbol{\sigma}_x -\lambda\,\boldsymbol{I}_2)\,\boldsymbol{x}\ =
   \ \boldsymbol{0}

wyznaczamy odpowiednie wektory własne :math:`\ \boldsymbol{x}.`

Wektory własne dla wartości :math:`\,\lambda_1=\,1:`

.. math::
   
   \begin{array}{l}
   \left[\begin{array}{rr} -1 & 1 \\ 1 & -1 \end{array}\ \right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right]
   \quad : \quad
   \begin{cases}\ 
   \begin{array}{r} -x_1+x_2=0 \\ x_1-x_2=0 \end{array}
   \end{cases}
   : \quad
   x_1=x_2=\alpha,\ \ \alpha\in C.
   \\ \\
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} \alpha \\ \alpha \end{array}\right]\ =\ 
   \alpha\ \left[\begin{array}{c} 1 \\ 1 \end{array}\right]\,,
   \quad\alpha\in C\setminus\{0\}.
   \end{array}

Wektory własne dla wartości :math:`\,\lambda_2=\,-1:`

.. math::
   
   \begin{array}{l}
   \left[\begin{array}{rr} 1 & 1 \\ 1 & 1 \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right]
   \quad : \quad
   \begin{cases}\ 
   \begin{array}{r} x_1+x_2=0 \\ x_1+x_2=0 \end{array}
   \end{cases}
   : \quad
   x_1=-x_2=\beta,\ \ \beta\in C.
   \\ \\
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} \beta \\ -\beta \end{array}\right]\ =\ 
   \beta\ \left[\begin{array}{r} 1 \\ -1 \end{array}\right]\,,
   \quad\beta\in C\setminus\{0\}.
   \end{array}

Krotność geometryczna obydwu wartości własnych wynosi 1 i zgadza się 
z ich krotnością algebraiczną. Każde dwa wektory własne należące do 
różnych wartości są ortogonalne:

.. math::
   
   \left\langle\ 
   \left[\begin{array}{c} \alpha \\ \alpha \end{array}\right],\ 
   \left[\begin{array}{c}  \beta \\ -\beta \end{array}\right]\ 
   \right\rangle\ =\ 
   \alpha^*\beta\,+\,\alpha^*(-\beta)\ =\ 
   \alpha^*\beta\,-\,\alpha^*\beta\ =\ 0.

Ortonormalna baza :math:`\ \mathcal{F}\ ` przestrzeni :math:`\,C^2\ ` 
jest złożona z unormowanych wektorów własnych macierzy 
:math:`\ \boldsymbol{\sigma}_x\,:`

.. math::
   
   \mathcal{F}\ =\ \,(\,\boldsymbol{f}_1,\,\boldsymbol{f}_2\,)\,,
   \quad\text{gdzie}\quad
   \boldsymbol{f}_1\ =\ \textstyle{\frac{1}{\sqrt{2}}}\,
   \left[\begin{array}{c} 1 \\ 1 \end{array}\right]\,,\quad
   \boldsymbol{f}_2\ =\ \textstyle{\frac{1}{\sqrt{2}}}\,
   \left[\begin{array}{c} 1 \\ -1 \end{array}\right]\,.

Wektory bazy :math:`\,\mathcal{F}\ ` tworzą 
macierz :math:`\,\boldsymbol{P}\ `
diagonalizującą macierz :math:`\,\boldsymbol{\sigma}_x:`

.. math::
   
   \boldsymbol{P}\,=\ 
   [\ \boldsymbol{f}_1\ |\ \boldsymbol{f}_2\ ]\ =\ 
   \textstyle{\frac{1}{\sqrt{2}}}\,
   \left[\begin{array}{rr} 1 & 1 \\ 1 & -1 \end{array}\right]\,.

Zauważmy, że :math:`\,\boldsymbol{P}\,` jest macierzą rzeczywistą, 
jednocześnie hermitowską (symetryczną) :math:`\\` i :math:`\ ` unitarną 
(ortogonalną):

.. math::
   
   \boldsymbol{P}^+\ =\ \,\boldsymbol{P}^T\ =\ \,\boldsymbol{P}
   \,,\qquad
   \boldsymbol{P}^+\boldsymbol{P}\ =\ 
   \boldsymbol{P}^T\boldsymbol{P}\ =\ 
   \boldsymbol{I}_2\,;

   \text{ponadto:}\qquad
   \boldsymbol{P}^2\ =\ \boldsymbol{I}_2,\quad
   \boldsymbol{P}^{-1}\ =\ \boldsymbol{P}^+\ =\ \boldsymbol{P}\,.

Numeryczna diagonalizacja macierzy :math:`\,\boldsymbol{\sigma}_x:`

.. code-block:: python
   
   sage: P = (1/sqrt(2))*matrix(RR,[[1, 1],
                              [1,-1]])
   sage: P*P

   [ 1.00000000000000  0.000000000000000]
   [ 0.000000000000000 1.00000000000000 ]

.. code-block:: python
   
   sage: S_x = matrix(RR,[[0, 1],
                          [1, 0]])
   
   sage: P = (1/sqrt(2))*matrix(RR,[[1, 1],
                              [1,-1]])
   sage: P*S_x*P

   [ 1.00000000000000   0.000000000000000]
   [ 0.000000000000000 -1.00000000000000 ]

.. :math:`\\[14pt]`

**Przykład 2.**

Macierz :math:`\ \boldsymbol{R}_\phi\ =\ 
\left[\begin{array}{cc}
\cos{\phi} & -\sin{\phi} \\ \sin{\phi} & \cos{\phi}
\end{array}\right] \in M_2(C)\ `
jest rzeczywista i ortogonalna, a więc unitarna:

.. math::
   
   \boldsymbol{R}_\phi^+\,\boldsymbol{R}_\phi\ =\
   \boldsymbol{R}_\phi^T\,\boldsymbol{R}_\phi\ =\ 
   \boldsymbol{I}_2.
   
Sprawdzimy, że:

* jej wartości własne są liczbami zespolonymi o module 1,

* wektory własne, należące do różnych wartości własnych, są ortogonalne,

* dla każdej wartości własnej krotność algebraiczna równa się
  krotności geometrycznej,

* w przestrzeni :math:`\,C^2\,` istnieje ortonormalna baza, 
  złożona z jej wektorów własnych,

* można ją zdiagonalizować poprzez unitarną transformację podobieństwa.

Dla :math:`\,\phi=0\ ` oraz :math:`\,\phi=\pi\ ` 
macierz :math:`\ \boldsymbol{R}_\phi\ ` już jest diagonalna i
równa się odpowiednio :math:`\,\boldsymbol{I}_2\ ` albo
:math:`\ -\,\boldsymbol{I}_2.\ ` W dalszym ciągu zakładamy więc,
że :math:`\ \phi\neq 0,\,\pi.`

Macierz unitarna, diagonalizująca macierz :math:`\ \boldsymbol{R}_\phi,\ `
jest macierzą przejścia od bazy kanonicznej :math:`\,\mathcal{E}\,=\,
(\boldsymbol{e}_1,\, \boldsymbol{e}_2)\ ` przestrzeni :math:`\,C^2\ ` 
do ortonormalnej bazy :math:`\,\mathcal{F}\,=\,
(\boldsymbol{f}_1,\boldsymbol{f}_2),\ ` złożonej z unormowanych wektorów 
własnych macierzy :math:`\ \boldsymbol{R}_\phi.`

Rozwiążemy problem własny macierzy :math:`\ \boldsymbol{R}_\phi\ `
i :math:`\,` zbudujemy bazę :math:`\,\mathcal{F}.`

Wielomian charakterystyczny :math:`\,w(\lambda)\,=\,
\det(\boldsymbol{R}_\phi -\,\lambda\,\boldsymbol{I}_2)\ `
jest dany przez

.. math::
   
   \begin{array}{rl}
   w(\lambda) \!\! & =\ \ \left|\begin{array}{cc}
   \cos{\phi}-\lambda & -\sin{\phi} \\ \sin{\phi} & \cos{\phi}-\lambda
   \end{array}\right| \ =\ (\cos{\phi}-\lambda)^2\,+\ {\sin}^2\phi\ = 
   \\[12pt]
   & =\ \, {\cos}^2\phi - 2\,\lambda\,\cos{\phi}\ + \lambda^2 +\ {\sin}^2\phi\  
   =\ 1\, -\, 2\,\lambda\,\cos{\phi}\ +\,\lambda^2.
   \end{array}

Wartości własne macierzy :math:`\ \boldsymbol{R}_\phi\ `
są pierwiastkami równania charakterystycznego :math:`\,w(\lambda)=0:`

.. math::
   
   \begin{array}{rl}
   \vartriangleright 
   & \lambda^2\,-\ 2\,\cos{\phi}\cdot\lambda\ +\ 1\ =\ 0 \\[8pt]
   & \Delta\ =\ 4\,{\cos}^2\phi\ -\ 4\ 
            =\ -\ 4\,(1-{\cos}^2\phi)\ 
            =\ -\ 4\,{\sin}^2\phi\,<\,0\,; \\[8pt]
   & \sqrt{\Delta}\ =\ \pm\,2\,i\,\sin{\phi}; \\[8pt]
   & \lambda_{1,2}\ =\ \frac{1}{2}\ (2\,\cos{\phi}\,\pm\,2i\sin{\phi})\ 
                    =\ \cos{\phi}\,\pm\,i\,\sin{\phi}\ 
                    =\ e^{\ \pm\,i\,\phi}\,.                       
   \end{array}

Otrzymaliśmy dwie wartości własne, obie algebraicznie pojedyncze:

.. math::
   
   \blacktriangleright\quad
   \lambda_1\,=\ e^{\ +\,i\,\phi}\,,\qquad
   \lambda_2\,=\ e^{\ -\,i\,\phi}\,.

Podstawiając kolejno wyliczone wartości własne do równania

.. math::
   
   (\boldsymbol{R}_\phi-\lambda\,\boldsymbol{I}_2)\ \boldsymbol{x}\ =
   \ \boldsymbol{0}

wyznaczamy odpowiednie wektory własne :math:`\ \boldsymbol{x}.`

Dla wektorów własnych należących do wartości :math:`\ \lambda_1 =\,
e^{\ +\,i\,\phi}\,=\,\cos{\phi}\,+\,i\,\sin{\phi}\ ` otrzymujemy:

.. math::
   
   \left[\begin{array}{cc}
   -i\,\sin{\phi} & -\sin{\phi} \\ \sin{\phi} & -i\,\sin{\phi}
   \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right]\,;

   \sin{\phi}\,\cdot\,
   \left[\begin{array}{cc} -i & -1 \\ 1 & -i \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right],\quad
   \text{przy czym  }\sin{\phi}\neq 0\,;

   \left[\begin{array}{cc} -i & -1 \\ 1 & -i \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right]
   \quad : \quad
   \begin{cases}\ 
   \begin{array}{r} -i\,x_1 - x_2 = 0 \\ x_1 - i\,x_2 = 0 \end{array}
   \end{cases}
   : \quad
   x_1=i\,x_2 
   
   \blacktriangleright\quad
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right]\ =\  
   \left[\begin{array}{r} i\,\alpha \\ \alpha \end{array}\right]\ =\ 
   \alpha\,\left[\begin{array}{r} i \\ 1 \end{array}\right],
   \quad\alpha\in C\setminus\{0\}.

Wektory własne dla wartości :math:`\ \lambda_2 =\,
e^{\ -\,i\,\phi}\,=\,\cos{\phi}\,-\,i\,\sin{\phi}\ `
wyznaczone są przez warunki:

.. math::
   
   \left[\begin{array}{cc}
   i\,\sin{\phi} & -\sin{\phi} \\ \sin{\phi} & i\,\sin{\phi}
   \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right]\,;

   \sin{\phi}\,\cdot\,
   \left[\begin{array}{cc} i & -1 \\ 1 & i \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right],\quad
   \text{przy czym  }\sin{\phi}\neq 0\,;

   \left[\begin{array}{cc} i & -1 \\ 1 & i \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right] \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \end{array}\right]
   \quad : \quad
   \begin{cases}\ 
   \begin{array}{r} i\,x_1 - x_2 = 0 \\ x_1 + i\,x_2 = 0 \end{array}
   \end{cases}
   : \quad
   x_2=i\,x_1 
   
   \blacktriangleright\quad
   \left[\begin{array}{c} x_1 \\ x_2 \end{array}\right]\ =\  
   \left[\begin{array}{r} \beta \\ i\,\beta \end{array}\right]\ =\ 
   \beta\,\left[\begin{array}{r} 1 \\ i \end{array}\right],
   \quad\beta\in C\setminus\{0\}.

Zauważmy, że wektory własne nie zależą od kąta :math:`\,\phi.\ `
Krotności geometryczne obydwu wartości własnych 
:math:`\ \lambda_1,\,\lambda_2\ ` są równe 1 
i zgadzają się z krotnościami algebraicznymi. 

Każde dwa wektory własne, należące do różnych wartości własnych, są ortogonalne:

.. math::
   
   \left\langle\ 
   \left[\begin{array}{c} i\,\alpha \\ \alpha \end{array}\right],\ 
   \left[\begin{array}{c} \beta \\ i\,\beta \end{array}\right]\ 
   \right\rangle\ =\ 
   -i\,\alpha^*\beta\,+\,\alpha^*\,i\,\beta\ =\ 0.

Można teraz zbudować ortonormalną bazę :math:`\ \mathcal{F}\ ` 
przestrzeni :math:`\,C^2,\ ` składającą się z unormowanych 
wektorów własnych macierzy :math:`\ \boldsymbol{R}_\phi,\ ` 
należących do różnych wartości własnych:

.. math::
   
   \mathcal{F}\ =\ (\,\boldsymbol{f}_1,\,\boldsymbol{f}_2\,),
   \quad\text{gdzie}\quad
   \boldsymbol{f}_1\ =\ 
   \textstyle{\frac{1}{\sqrt{2}}}\,
   \left[\begin{array}{c} i \\ 1 \end{array}\right],\quad
   \boldsymbol{f}_2\ =\ 
   \textstyle{\frac{1}{\sqrt{2}}}\,
   \left[\begin{array}{c} 1 \\ i \end{array}\right]\,.

Macierz przejścia :math:`\ \boldsymbol{P}\ ` 
od bazy kanonicznej :math:`\ \mathcal{E}\ ` do bazy :math:`\ \mathcal{F}\ `,
zestawiona z kolumn :math:`\ \boldsymbol{f}_1,\,\boldsymbol{f}_2:`

.. math::

   \boldsymbol{P}\ =\ [\ \boldsymbol{f}_1\ |\ \boldsymbol{f}_2\ ]\ =
   \textstyle{\frac{1}{\sqrt{2}}}\,\left[\begin{array}{cc}
   i & 1 \\ 1 & i \end{array}\right]   
   
jest unitarna i diagonalizuje macierz :math:`\ \boldsymbol{R}_\phi:`

.. math::
   
   \boldsymbol{P}^+\boldsymbol{P}\ =\ \boldsymbol{I}_2,\qquad
   \boldsymbol{P}^{-1}\boldsymbol{R}_\phi\,\boldsymbol{P}\ =\ 
   \text{diag}(e^{\ +\,i\,\phi},\,e^{\ -\,i\,\phi})\,.

.. Sprawdzenie numeryczne:

.. .. code-block:: python
   
   sage: P = (1/sqrt(2))*matrix(CC,[[I, 1],
                                    [1, I]])
   sage: P.H*P

   [1.00000000000000  0.000000000000000]
   [0.000000000000000 1.00000000000000 ]

.. .. code-block:: python
   
   sage: var 'phi'

   sage: R = matrix(CC,[[cos(phi), -sin(phi)],
                        [sin(phi), cos(phi)]]

   sage: P = (1/sqrt(2))*matrix(CC,[[I, 1],
                                    [1, I]])
   sage: P.I*R*P

Macierz :math:`\ \boldsymbol{R}_\phi\ ` reprezentuje operację obrotu wektora 
na płaszczyźnie o kąt :math:`\,\phi.\ ` Przy tej interpretacji zrozumiały jest 
fakt, że z wyjątkiem przypadków :math:`\,\phi=0,\,\pi\ ` wartości własne 
macierzy są zespolone nierzeczywiste: wektor obrócony o kąt :math:`\,\phi\ `
nie jest równoległy do wektora wyjściowego. W tej sytuacji diagonalizacja 
rzeczywistej macierzy :math:`\ \boldsymbol{R}_\phi\ ` wymaga użycia zespolonej 
nierzeczywistej unitarnej macierzy :math:`\ \boldsymbol{P}.`

.. , chyba że właśnie 
   :math:`\,\phi=0,\,\pi\ ` (w tych dwóch przypadkach wartość własna wynosi 
   odpowiednio +1, -1.)

.. Rzeczywista ortogonalna macierz :math:`\ \boldsymbol{R}_\phi\ `
   ma (dla :math:`\,\phi\neq 0, \pi`) zespolone nierzeczywiste wartości własne.

.. W konsekwencji diagonalizacja tej macierzy wymaga zastosowania zespolonej
   nierzeczywistej unitarnej macierzy diagonalizującej :math:`\ \boldsymbol{P}.`

.. :math:`\ `

**Przykład 3.**

Macierz :math:`\ \boldsymbol{A}\ =\ 
\left[\begin{array}{ccc} 0 & 1 & 1 \\ 1 & 0 & 1 \\ 1 & 1 & 0 \end{array}\right]
\in M_3(R)\ ` jest rzeczywista i symetryczna, a więc hermitowska.

Sprawdzimy, że:

* jej wartości własne są rzeczywiste,
* wektory własne, należące do różnych wartości, są ortogonalne,
* dla każdej wartości własnej krotność algebraiczna równa się
  krotności geometrycznej,
* w przestrzeni :math:`\,R^3\,` istnieje ortonormalna baza, 
  złożona z jej wektorów własnych,
* można ją zdiagonalizować poprzez rzeczywistą transformację ortogonalną.

Macierzą ortogonalną diagonalizującą macierz :math:`\ \boldsymbol{A}\ `
jest macierz przejścia od bazy kanonicznej :math:`\,\mathcal{E}\,`
przestrzeni :math:`\,R^3\,` do ortonormalnej bazy :math:`\,\mathcal{F}^0\,`
złożonej z unormowanych wektorów własnych tej macierzy.
Należy więc rozwiązać problem własny macierzy :math:`\ \boldsymbol{A}\ `
i następnie skonstruować ortonormalną bazę, złożoną z jej wektorów własnych.

Równanie charakterystyczne:

.. math::
   
   \det{(\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)}\ =
   \ \left|\begin{array}{ccc}
   -\lambda & 1 & 1 \\ 1 & -\lambda & 1 \\ 1 & 1 & -\lambda
   \end{array}\ \,\right|\ =
   \ -\lambda^3+3\,\lambda + 2\ =
   -(\lambda-2)(\lambda+1)^2\ =\ 0

daje wartości własne i ich krotności algebraiczne:

.. math::
   
   \lambda_1=\,2 \quad (1)\,,\qquad \lambda_2=\,-1 \quad (2)\,.

Ogólnie, wektory własne :math:`\,\boldsymbol{x}\,` 
dla wartości :math:`\,\lambda\,` wyznacza się z równania

.. math::
   :label: eigen_vector
   
   (\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)\ \boldsymbol{x}\ =
   \ \boldsymbol{0}.

Dla :math:`\ \lambda\,=\,\lambda_1=\,2\ ` równanie :eq:`eigen_vector` 
przyjmuje postać

.. math::
   
   \left[\begin{array}{ccc}
   -2 & 1 & 1 \\ 1 & -2 & 1 \\ 1 & 1 & -2
   \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array}\right]
   \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \\ 0 \end{array}\right]\,.

Metoda ``rref()`` systemu Sage przekształca macierz tego jednorodnego problemu
liniowego do zredukowanej wierszowej postaci schodkowej:

.. code-block:: python
   
   sage: A = matrix(QQ,[[-2, 1, 1],
                        [ 1,-2, 1],
                        [ 1, 1,-2]])
   sage: A.rref()

   [ 1  0 -1]
   [ 0  1 -1]
   [ 0  0  0]
   
Otrzymany równoważny problem liniowy

.. math::
   
   \left[\begin{array}{ccc}
   1 & 0 & -1 \\ 0 & 1 & -1 \\ 0 & 0 & 0
   \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array}\right]
   \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \\ 0 \end{array}\right]

odpowiada układowi równań

.. math::
   :nowrap:
   
   \begin{alignat*}{7}
   x_1 & \  \ &     & \  - \ \ & x_3 & \  = \ \ & 0 \\
       & \  \ & x_2 & \  - \ \ & x_3 & \  = \ \ & 0
   \end{alignat*}

którego ogólnym rozwiązaniem jest 
:math:`\ x_1=x_2=x_3=\alpha, \ \ \alpha\in R.\ ` :math:`\\`
Wektory własne dla wartości :math:`\,\lambda_1=2\,` mają więc postać

.. math::
   
   \boldsymbol{x}\ =\ 
   \left[\begin{array}{c}
   \alpha \\ \alpha \\ \alpha
   \end{array}\right]
   \ =\ 
   \alpha\ \left[\begin{array}{c} 1 \\ 1 \\ 1 \end{array}\right],
   \quad\alpha\in R\setminus\{0\}.

Krotność geometryczna tej wartości wynosi 1 
i zgadza się z jej krotnością algebraiczną.

Podstawienie :math:`\ \lambda\,=\,\lambda_2=\,-1\ ` 
do wzoru :eq:`eigen_vector` daje równanie 

.. math::
   
   \left[\begin{array}{ccc}
   1 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 1 
   \end{array}\right]
   \left[\begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array}\right]
   \ =\ 
   \left[\begin{array}{c} 0 \\ 0 \\ 0 \end{array}\right]\,.

Funkcja ``right_kernel_matrix()`` systemu Sage zwraca macierz, 
której wiersze tworzą bazę przestrzeni rozwiązań jednorodnego 
problemu liniowego. Tutaj otrzymujemy

.. code-block:: python
   
   sage: A = matrix(QQ,[[1, 1, 1],
                        [1, 1, 1],
                        [1, 1, 1]])

   sage: A.right_kernel_matrix()

   [ 1  0 -1]
   [ 0  1 -1]
   
Wektory własne dla wartości :math:`\ \lambda_2\,=-1\ ` są więc postaci

.. math::
   
   \boldsymbol{x}\ =\ 
   \alpha\ \,\left[\begin{array}{r} 1 \\ 0 \\ -1 \end{array}\right]\ +\ 
   \beta \ \,\left[\begin{array}{r} 0 \\ 1 \\ -1 \end{array}\right]\ =\ 
   \left[\begin{array}{c} 
   \alpha \\ \beta \\ -\alpha-\beta 
   \end{array}\right]\,,
   \quad\alpha,\beta\in R,\ \ \alpha^2+\,\beta^2>0.

Krotność geometryczna, zgodna z krotnością algebraiczną, wynosi 2.

Zauważmy, że wektory własne należące do różnych wartości własnych 
są ortogonalne:

.. math::
   
   \left\langle\ \ 
   \left[\begin{array}{c} \alpha \\ \alpha \\ \alpha \end{array}\right],\ 
   \left[\begin{array}{c} 
   \beta \\ \gamma \\ -\,\beta-\gamma 
   \end{array}\right]\ \ 
   \right\rangle\ \ =\ \ 
   \alpha\beta\,+\,\alpha\gamma\,+\,\alpha\,(-\,\beta-\gamma)\ =\ 0\,.

Wprowadzamy oznaczenia dla trzech liniowo niezależnych wektorów własnych 
macierzy :math:`\ \boldsymbol{A}:`

.. math::
   
   \boldsymbol{g}_1\,=\ 
   \left[\begin{array}{c} 1 \\ 1 \\ 1 \end{array}\right],\quad
   \boldsymbol{g}_2\,=\ 
   \left[\begin{array}{r} 1 \\ 0 \\ -1 \end{array}\right],\quad
   \boldsymbol{g}_3\,=\ 
   \left[\begin{array}{r} 0 \\ 1 \\ -1 \end{array}\right],

które tworzą bazę :math:`\,\mathcal{G}=
(\boldsymbol{g}_1,\boldsymbol{g}_2,\boldsymbol{g}_3)\ ` przestrzeni
:math:`\,R^3.\ ` 

W tej sytuacji macierz :math:`\ \boldsymbol{P}\,=\,
[\ \boldsymbol{g}_1\,|\,\boldsymbol{g}_2\,|\,\boldsymbol{g}_3\ ]\ =\ 
\left[\begin{array}{rrr} 
1 & 1 & 0 \\ 1 & 0 & 1 \\ 1 & -1 & -1 
\end{array}\right]\ ` diagonalizuje :math:`\ \boldsymbol{A}:`

.. code-block:: python
   
   sage: A = matrix(QQ,[[0, 1, 1],
                        [1, 0, 1],
                        [1, 1, 0]])

   sage: P = matrix(QQ,[[1, 1, 0],
                        [1, 0, 1],
                        [1,-1,-1]])
   sage: P.I*A*P  

   [ 2  0  0]
   [ 0 -1  0]
   [ 0  0 -1]
   
:math:`\ \boldsymbol{P}\ ` nie jest macierzą ortogonalną, bo iloczyn skalarny
:math:`\ \langle\boldsymbol{g}_2,\boldsymbol{g}_3\rangle = 1 \neq 0.`  
Dla otrzymania bazy ortogonalnej 
:math:`\ \mathcal{F}=(\boldsymbol{f}_1,\boldsymbol{f}_2,\boldsymbol{f}_3)`, 
a następnie ortonormalnej :math:`\ \mathcal{F}^0=
(\boldsymbol{f}_1^0,\boldsymbol{f}_2^0,\boldsymbol{f}_3^0)`, trzeba przeprowadzić ortogonalizację Grama-Schmidta. Kładziemy 

.. math::
   
   \boldsymbol{f}_1=\,\boldsymbol{g}_1=\,
   \left[\begin{array}{c} 1 \\ 1 \\ 1 \end{array}\right],\quad  
   \boldsymbol{f}_2=\,\boldsymbol{g}_2=\,
   \left[\begin{array}{r} 1 \\ 0 \\ -1 \end{array}\right],\quad
   \boldsymbol{f}_3=\,\boldsymbol{g}_3+\eta\,\boldsymbol{f}_2=\,
   \left[\begin{array}{c} \eta \\ 1 \\ -1-\eta \end{array}\right],

gdzie :math:`\,\eta\,` wyznaczamy z warunku ortogonalności
:math:`\ \langle\boldsymbol{f}_2,\boldsymbol{f}_3\rangle\,=\,2\eta+1\,=\,0.\ ` 
Stąd

.. math::
   
   \eta = - \textstyle\frac{1}{2}\,,\qquad
   \boldsymbol{f}_3\ =\ 
   \left[\begin{array}{r} -\frac{1}{2} \\ 1 \\ -\frac{1}{2} \end{array}\right]
   \ =\ -\frac{1}{2}\ \left[\begin{array}{r} 1 \\ -2 \\ 1 \end{array}\right]
   \ \ \sim\ \ \left[\begin{array}{r} 1 \\ -2 \\ 1 \end{array}\right]\,.

Ortogonalna baza :math:`\ \mathcal{F}\ ` składa się więc z wektorów własnych

.. math::
   
   \boldsymbol{f}_1\,=\ 
   \left[\begin{array}{c} 1 \\ 1 \\ 1 \end{array}\right],\quad
   \boldsymbol{f}_2\,=\ 
   \left[\begin{array}{r} 1 \\ 0 \\ -1 \end{array}\right],\quad
   \boldsymbol{f}_3\,=\ 
   \left[\begin{array}{r} 1 \\ -2 \\ 1 \end{array}\right]\,,

a bazę ortonormalną :math:`\ \mathcal{F}^0\ ` otrzymamy 
dzieląc każdy wektor przez jego normę:

.. math::
   
   \boldsymbol{f}_1^0\,=\ \textstyle{\frac{1}{\sqrt{3}}}
   \left[\begin{array}{c} 1 \\ 1 \\ 1 \end{array}\right],\quad
   \boldsymbol{f}_2\,=\ \textstyle{\frac{1}{\sqrt{2}}}
   \left[\begin{array}{r} 1 \\ 0 \\ -1 \end{array}\right],\quad
   \boldsymbol{f}_3\,=\ \textstyle{\frac{1}{\sqrt{6}}}
   \left[\begin{array}{r} 1 \\ -2 \\ 1 \end{array}\right]\,.

Wektory kolumnowe 
:math:`\ \boldsymbol{f}_1^0,\,\boldsymbol{f}_2^0,\boldsymbol{f}_3^0\ `
składają się na ortogonalną macierz przejścia :math:`\ \boldsymbol{P}^0\ `
od bazy kanonicznej :math:`\,\mathcal{E}\,` do bazy :math:`\ \mathcal{F}^0\ `
przestrzeni :math:`\,R^3.\ ` Jest to macierz diagonalizująca macierz
:math:`\,\boldsymbol{A}\,` poprzez ortogonalną transformację podobieństwa:

.. math::
   
   \boldsymbol{P}^0\ =\ \,\textstyle
   \left[\begin{array}{rrr}
   \frac{1}{\sqrt{3}} &  \frac{1}{\sqrt{2}}   &    \frac{1}{\sqrt{6}} \\ \\
   \frac{1}{\sqrt{3}} &  0                    & -\,\frac{2}{\sqrt{6}} \\ \\
   \frac{1}{\sqrt{3}} & -\,\frac{1}{\sqrt{2}} &    \frac{1}{\sqrt{6}}
   \end{array}\right]\,.

Sprawdzenie numeryczne:

.. code-block:: python
   
   sage: P0 = matrix(RR,[[1/sqrt(3), 1/sqrt(2), 1/sqrt(6)],
                         [1/sqrt(3), 0,        -2/sqrt(6)],
                         [1/sqrt(3),-1/sqrt(2), 1/sqrt(6)]])
    
   sage: P0.T*P0.n(digits=4)

   [1.000  0.0000 0.0000]
   [0.0000 1.000  0.0000]
   [0.0000 0.0000 1.000 ]

.. code-block:: python

   sage: A = matrix(RR,[[0, 1, 1],
                        [1, 0, 1],
                        [1, 1, 0]])
    
   sage: P0 = matrix(RR,[[1/sqrt(3), 1/sqrt(2), 1/sqrt(6)],
                         [1/sqrt(3), 0,        -2/sqrt(6)],
                         [1/sqrt(3),-1/sqrt(2), 1/sqrt(6)]])    

   sage: P0.I*A*P0.n(digits=4)

   [2.000   0.0000  0.0000]
   [0.0000 -1.000   0.0000]
   [0.0000  0.0000 -1.000 ]  




















