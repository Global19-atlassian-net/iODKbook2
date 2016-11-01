
Zadania
-------

**Zadanie 1.** :math:`\,`
Niech :math:`\ \boldsymbol{A}\,=\,[a_{ij}]_{2\times 2}\ `
będzie dowolną macierzą nad ciałem :math:`\ K.\ `
Dla :math:`\ n=2,\ 3\ ` pokaż bezpośrednio, że macierz 
:math:`\ \boldsymbol{A}\otimes\boldsymbol{I}_n\ ` można 
przekształcić do postaci :math:`\ \boldsymbol{I}_n\otimes\boldsymbol{A}\ `
poprzez pewne przestawienia wierszy :math:`R_i\ ` :math:`\,` i :math:`\,` 
takie same przestawienia kolumn :math:`\ C_j\ \ (i,j=1,\ldots,n.`).

Określ macierze permutacji :math:`\ \boldsymbol{P},\,\boldsymbol{Q}\ ` 
w zależności

.. math::
   
   \boldsymbol{I}_n\otimes\boldsymbol{A}\ \, = \ \,
   \boldsymbol{P}\ 
   (\boldsymbol{A}\otimes\boldsymbol{I}_n)\ 
   \boldsymbol{Q}\,.

Sprawdź, że :math:`\,\boldsymbol{Q} = \boldsymbol{P}^T =
\boldsymbol{P}^{-1}\,` co oznacza, że jeśli :math:`\,\boldsymbol{P}\,`
jest macierzą pewnej permutacji :math:`\,\sigma\,` wierszy, to
:math:`\,\boldsymbol{Q}\,` jest macierzą tej samej permutacji 
kolumn. Zapisz :math:`\,\sigma\,` w postaci dwuwierszowej.

**Rozwiązanie** :math:`\,` dla :math:`\,` :math:`n=2\ ` 
(wersja wierszowo-kolumnowa):

.. math::
   
   \begin{array}{rrr}
   \boldsymbol{A}\otimes\boldsymbol{I}_2 & =\ \ 
   \left[\begin{array}{cc}
   a_{11}\ \boldsymbol{I}_2 & a_{12}\ \boldsymbol{I}_2 \\
   a_{21}\ \boldsymbol{I}_2 & a_{22}\ \boldsymbol{I}_2
   \end{array}\right]\ \ =\ \ 
   \left[\begin{array}{cc|cc}
   a_{11} &   0    & a_{12} &   0    \\
     0    & a_{11} &   0    & a_{12} \\ \hline
   a_{21} &   0    & a_{22} &   0    \\
     0    & a_{21} &   0    & a_{22}
   \end{array}\right]\ \ \rightarrow &
   \end{array}
   \\[7pt] 
   \begin{array}{rcl}
   & \ \ R_2\leftrightarrow R_3:
   \qquad\qquad\qquad\qquad 
   C_2\leftrightarrow C_3: &
   \\[3pt]
   & \rightarrow\ \ 
   \left[\begin{array}{cccc}
   a_{11} &   0    & a_{12} &   0    \\
   a_{21} &   0    & a_{22} &   0    \\
     0    & a_{11} &   0    & a_{12} \\
     0    & a_{21} &   0    & a_{22}
   \end{array}\right]\ \ \rightarrow\ \ 
   \left[\begin{array}{cc|cc}
   a_{11} & a_{12} &   0    &   0    \\
   a_{21} & a_{22} &   0    &   0    \\ \hline
     0    &   0    & a_{11} & a_{12} \\
     0    &   0    & a_{21} & a_{22}
   \end{array}\right]\ \ =\  
   & \boldsymbol{I}_2\otimes\boldsymbol{A}\,.
   \end{array}
   \\[4pt]

.. **Wniosek**: :math:`\quad \det{(\boldsymbol{A}\otimes\boldsymbol{I}_2)}\,=\,
   \det{(\boldsymbol{I}_2\otimes\boldsymbol{A})}\,=\,(\det{\boldsymbol{A}})^2.`

Przekształcenie macierzy :math:`\ \boldsymbol{A}\otimes\boldsymbol{I}_2\ `
do postaci :math:`\ \boldsymbol{I}_2\otimes\boldsymbol{A}\ ` przebiega 
w jednym podwójnym kroku:

.. math::
   :label: trans-2
   
   \boldsymbol{I}_2\otimes\boldsymbol{A}\ \, =\ \,
   \boldsymbol{P}_{23}\ 
   (\boldsymbol{A}\otimes\boldsymbol{I}_2)\ 
   \boldsymbol{Q}_{23}\,,

gdzie :math:`\ \boldsymbol{P}_{23}\ ` jest macierzą transpozycji wierszy 
(drugiego i trzeciego), a :math:`\ \, \boldsymbol{Q}_{23}\ ` :math:`\ -\ \ `
macierzą transpozycji kolumn (drugiej i trzeciej).

.. Przy numerycznym sprawdzeniu wzoru :eq:`trans-2` należy pamiętać,
   że w systemie Sage:
   
   * w kodzie programu początkowym numerem wierszy i kolumn jest liczba 0;
   
   * | macierz :math:`\ \boldsymbol{P}_{23}\ ` transpozycji wierszy 
       jest macierzą elementarną 1. rodzaju,
     | otrzymaną z macierzy jednostkowej przez przestawienie wiersza
       drugiego z trzecim; 
     | macierz ta przekształca daną macierz mnożąc ją z lewej strony;
   
   * | macierz :math:`\ \boldsymbol{Q}_{23}\ ` transpozycji kolumn 
       jest macierzą elementarną 1. rodzaju,
     | otrzymaną z macierzy jednostkowej przez przestawienie kolumny
       drugiej z trzecią;
     | macierz ta przekształca daną macierz mnożąc ją z prawej strony.
       :math:`\ `

.. code-block:: python
   
   sage: A = matrix([[var("a%d%d" % (k,l)) for l in [1,2]]
                                           for k in [1,2]])
   sage: I2 = identity_matrix(2)
   
   sage: AxI2 = A.tensor_product(I2)
   
   sage: P23 = elementary_matrix(4, row1=1, row2=2)
   sage: Q23 = elementary_matrix(4, col1=1, col2=2)
   
   sage: I2xA = P23 * AxI2 * Q23
   sage: I2xA.subdivide(2,2)
   
   sage: (AxI2, I2xA)
   
   (
   [a11   0|a12   0]  [a11 a12|  0   0]
   [  0 a11|  0 a12]  [a21 a22|  0   0]
   [-------+-------]  [-------+-------]
   [a21   0|a22   0]  [  0   0|a11 a12]
   [  0 a21|  0 a22], [  0   0|a21 a22]
   )

**Rozwiązanie** :math:`\,` dla :math:`\,` :math:`n=3\ ` 
(wersja wierszowo-kolumnowa):

.. math::

   \begin{array}{llll}   
   \boldsymbol{A}\otimes\boldsymbol{I}_3 & 
   \ =\ \ \ 
   \left[\begin{array}{cc}
   a_{11}\ \boldsymbol{I}_3 & a_{12}\ \boldsymbol{I}_3 \\
   a_{21}\ \boldsymbol{I}_3 & a_{22}\ \boldsymbol{I}_3
   \end{array}\right]\ \ =\ \ &
   \left[\begin{array}{ccc|ccc}
   a_{11} &    0   &    0   & a_{12} &    0   &    0   \\
      0   & a_{11} &    0   &    0   & a_{12} &    0   \\
      0   &    0   & a_{11} &    0   &    0   & a_{12} \\ \hline
   a_{21} &    0   &    0   & a_{22} &    0   &    0   \\
      0   & a_{21} &    0   &    0   & a_{22} &    0   \\
      0   &    0   & a_{21} &    0   &    0   & a_{22} 
   \end{array}\right]\ \ \rightarrow & \qquad\quad
   \end{array}
   \\[10pt]
   \begin{array}{ccc}
   R_2\leftrightarrow R_4: & C_2\leftrightarrow C_4: \\[5pt]
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} &    0   &    0   & a_{12} &    0   &    0   \\
   a_{21} &    0   &    0   & a_{22} &    0   &    0   \\
      0   &    0   & a_{11} &    0   &    0   & a_{12} \\
      0   & a_{11} &    0   &    0   & a_{12} &    0   \\
      0   & a_{21} &    0   &    0   & a_{22} &    0   \\
      0   &    0   & a_{21} &    0   &    0   & a_{22} 
   \end{array}\right] & 
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   & a_{11} &    0   &    0   & a_{12} \\
      0   &    0   &    0   & a_{11} & a_{12} &    0   \\
      0   &    0   &    0   & a_{21} & a_{22} &    0   \\
      0   &    0   & a_{21} &    0   &    0   & a_{22} 
   \end{array}\right]\ \ \rightarrow & 
   \end{array}
   \\[10pt]
   \begin{array}{ccc}
   R_4\leftrightarrow R_6: & C_4\leftrightarrow C_6: \\[5pt]
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   & a_{11} &    0   &    0   & a_{12} \\
      0   &    0   & a_{21} &    0   &    0   & a_{22} \\
      0   &    0   &    0   & a_{21} & a_{22} &    0   \\
      0   &    0   &    0   & a_{11} & a_{12} &    0
   \end{array}\right] & 
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   & a_{11} & a_{12} &    0   &    0   \\
      0   &    0   & a_{21} & a_{22} &    0   &    0   \\
      0   &    0   &    0   &    0   & a_{22} & a_{21} \\
      0   &    0   &    0   &    0   & a_{12} & a_{11}
   \end{array}\right] \ \ \rightarrow &
   \end{array}
   \\[10pt]
   \begin{array}{ccc}
   R_5\leftrightarrow R_6: & C_5\leftrightarrow C_6: \\[5pt]
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   & a_{11} & a_{12} &    0   &    0   \\
      0   &    0   & a_{21} & a_{22} &    0   &    0   \\
      0   &    0   &    0   &    0   & a_{12} & a_{11} \\
      0   &    0   &    0   &    0   & a_{22} & a_{21}
   \end{array}\right] & 
   \rightarrow\ \ 
   \left[\begin{array}{cc|cc|cc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\ \hline
      0   &    0   & a_{11} & a_{12} &    0   &    0   \\ 
      0   &    0   & a_{21} & a_{22} &    0   &    0   \\ \hline
      0   &    0   &    0   &    0   & a_{11} & a_{12} \\
      0   &    0   &    0   &    0   & a_{21} & a_{22}
   \end{array}\right] \ \ = & 
   \boldsymbol{I}_3\otimes\boldsymbol{A}\,.
   \end{array}
   \\[10pt]

.. **Wniosek**: :math:`\quad \det{(\boldsymbol{A}\otimes\boldsymbol{I}_3)}\,=\,
   \det{(\boldsymbol{I}_3\otimes\boldsymbol{A})}\,=\,(\det{\boldsymbol{A}})^3.`

Wykonane operacje na wierszach i kolumnach macierzy 
:math:`\ \boldsymbol{A}\otimes\boldsymbol{I}_3\ `
można przedstawić wzorem

.. math::
   :label: trans-3
   
   \begin{array}{lll}
   \boldsymbol{I}_3\otimes\boldsymbol{A} &
   =\ \boldsymbol{P}_{56}\,\{\,\boldsymbol{P}_{46}\,[\,\boldsymbol{P}_{24}\,
   (\boldsymbol{A}\otimes\boldsymbol{I}_3)\,
   \boldsymbol{Q}_{24}\,]\,\boldsymbol{Q}_{46}\,\}\,\boldsymbol{Q}_{56}
   \ = & \\[7pt]
   & =\ \ (\boldsymbol{P}_{56}\,\boldsymbol{P}_{46}\,\boldsymbol{P}_{24})\ 
   (\boldsymbol{A}\otimes\boldsymbol{I}_3)\ 
   (\boldsymbol{Q}_{24}\,\boldsymbol{Q}_{46}\,\boldsymbol{Q}_{56})\ \ \equiv 
   & \boldsymbol{P}\ 
   (\boldsymbol{A}\otimes\boldsymbol{I}_3)\ 
   \boldsymbol{Q}.
   \end{array}
   
A zatem :math:`\ \boldsymbol{P} = 
\boldsymbol{P}_{56}\ \boldsymbol{P}_{46}\ \boldsymbol{P}_{24}\,,\ `
:math:`\ \boldsymbol{Q} = 
\boldsymbol{Q}_{24}\ \boldsymbol{Q}_{46}\ \boldsymbol{Q}_{56}\,,\ `
gdzie :math:`\ \boldsymbol{P}_{ij}\ ` jest macierzą transpozycji wierszy 
:math:`\ i,j\,,\ \,` a :math:`\ \, \boldsymbol{Q}_{ij}\ ` :math:`\ -\ \ `
macierzą transpozycji kolumn :math:`\ i,j\,,\ ` 
:math:`\ (i<j=1,2,\ldots,6.)`

Ponieważ :math:`\ \boldsymbol{Q}_{ij} = \boldsymbol{P}_{ij}^{\,T} =
\boldsymbol{P}_{ij}^{-1}\,,\ \ i<j=1,2,\ldots,6\,,\ ` to

.. math::

   \begin{array}{ll}   
   \boldsymbol{Q}\ =\ 
   \boldsymbol{Q}_{24}\ \boldsymbol{Q}_{46}\ \boldsymbol{Q}_{56} &
   =\ 
   \boldsymbol{P}_{24}^{\,T}\ 
   \boldsymbol{P}_{46}^{\,T}\ 
   \boldsymbol{P}_{56}^{\,T}\ =\ 
   \left(\boldsymbol{P}_{56}\ \boldsymbol{P}_{46}\ 
   \boldsymbol{P}_{24}\right)^T\ =\ 
   \boldsymbol{P}^{\,T}, \\[7pt]
   &
   =\ 
   \boldsymbol{P}_{24}^{-1}\ 
   \boldsymbol{P}_{46}^{-1}\ 
   \boldsymbol{P}_{56}^{-1}\ =\ 
   \left(\boldsymbol{P}_{56}\ \boldsymbol{P}_{46}\ 
   \boldsymbol{P}_{24}\right)^{-1}\ =\ 
   \boldsymbol{P}^{-1},
   \end{array}

czyli :math:`\ \ \boldsymbol{Q}\ \,=\ \,\boldsymbol{P}^{\,T}\ =\ \,
\boldsymbol{P}^{-1},\ \ ` czego należało oczekiwać.

**Wniosek**: :math:`\quad \det{(\boldsymbol{A}\otimes\boldsymbol{I}_3)}\,=\,
\det{(\boldsymbol{I}_3\otimes\boldsymbol{A})}\,=\,(\det{\boldsymbol{A}})^3.`

Macierze :math:`\ \boldsymbol{P}\ ` i :math:`\ \boldsymbol{Q}\ `
wyznaczymy numerycznie pamiętając o tym, że w systemie Sage:

* w kodzie programu początkowym numerem wierszy i kolumn jest liczba 0;

* | macierz :math:`\ \boldsymbol{P}_{ij}\ ` transpozycji wierszy 
    :math:`\ i,j\ ` jest macierzą elementarną 1. rodzaju,
  | otrzymaną z macierzy jednostkowej przez przestawienie wiersza
    :math:`\ i`-tego z :math:`\ j`-tym 
  | :math:`\ (i<j=1,2,\ldots,6.);\ `
    macierz ta przekształca daną macierz mnożąc ją z lewej strony;

* | macierz :math:`\ \boldsymbol{Q}_{ij}\ ` transpozycji kolumn 
    :math:`\ i,j\ ` jest macierzą elementarną 1. rodzaju,
  | otrzymaną z macierzy jednostkowej przez przestawienie kolumny
    :math:`\ i`-tej z :math:`\ j`-tą 
  | :math:`\ (i<j=1,2,\ldots,6.);\ `
    macierz ta przekształca daną macierz mnożąc ją z prawej strony.

.. :math:`\ `

.. code-block:: python
   
   sage: P24 = elementary_matrix(6, row1=1, row2=3)
   sage: P46 = elementary_matrix(6, row1=3, row2=5)
   sage: P56 = elementary_matrix(6, row1=4, row2=5)
   sage: P = P56*P46*P24
   
   sage: Q24 = elementary_matrix(6, col1=1, col2=3)
   sage: Q46 = elementary_matrix(6, col1=3, col2=5)
   sage: Q56 = elementary_matrix(6, col1=4, col2=5)
   sage: Q = Q24*Q46*Q56
   
   sage: (P,Q)

   (
   [1 0 0 0 0 0]  [1 0 0 0 0 0]
   [0 0 0 1 0 0]  [0 0 0 0 1 0]
   [0 0 1 0 0 0]  [0 0 1 0 0 0]
   [0 0 0 0 0 1]  [0 1 0 0 0 0]
   [0 1 0 0 0 0]  [0 0 0 0 0 1]
   [0 0 0 0 1 0], [0 0 0 1 0 0]
   )

.. :math:`\\`

Sprawdzimy teraz numerycznie zależność macierzową :eq:`trans-3`: 

.. :math:`\\`

.. code-block:: python
   
   sage: A = matrix([[var("a%d%d" % (k,l)) for l in [1,2]]
                                           for k in [1,2]])
   sage: I3 = identity_matrix(3)
   
   sage: AxI3 = A.tensor_product(I3)
   sage: I3xA = P * AxI3 * Q
   sage: I3xA.subdivide([2,4],[2,4])

   sage: (AxI3, I3xA)
   
   (
                              [a11 a12|  0   0|  0   0]
   [a11   0   0|a12   0   0]  [a21 a22|  0   0|  0   0]
   [  0 a11   0|  0 a12   0]  [-------+-------+-------]
   [  0   0 a11|  0   0 a12]  [  0   0|a11 a12|  0   0]
   [-----------+-----------]  [  0   0|a21 a22|  0   0]
   [a21   0   0|a22   0   0]  [-------+-------+-------]
   [  0 a21   0|  0 a22   0]  [  0   0|  0   0|a11 a12]
   [  0   0 a21|  0   0 a22], [  0   0|  0   0|a21 a22]
   )

Oznaczmy przez :math:`\ \sigma\in S_6\ ` permutację wierszy i kolumn,
która przeprowadza macierz :math:`\ \boldsymbol{A}\otimes\boldsymbol{I}_3\ `
w :math:`\ \boldsymbol{I}_3\otimes\boldsymbol{A}.\ ` 
Jeżeli w zapisie dwuwierszowym pierwszy wiersz ma postać 
:math:`\ \boldsymbol{r}_1\,=\,(1,\,2,\,3,\,4,\,5,\,6),\ ` 
to drugi wiersz jest dany przez
:math:`\ \ \boldsymbol{r}_2\ =\ (1,\,2,\,3,\,4,\,5,\,6)\ \boldsymbol{Q}:`

.. code-block:: python
   
   sage: r1 = vector([1,2,3,4,5,6])
   sage: r2 = r1 * Q
   sage: sigma = matrix([r1,r2])
   sage: sigma
   
   [1 2 3 4 5 6]
   [1 4 3 6 2 5]

:math:`\\`
A zatem poszukiwaną permutacją jest 

.. math::

   \sigma\ = \ 
   \left(\begin{array}{cccccc}
   1 & 2 & 3 & 4 & 5 & 6 \\
   1 & 4 & 3 & 6 & 2 & 5
   \end{array}\right)\,.

Permutację :math:`\sigma` można też wyliczyć bezpośrednio,
jako złożenie transpozycji odpowiadających macierzom 
:math:`\ \boldsymbol{P}_{ij}\ ` albo :math:`\ \boldsymbol{Q}_{ij}\,.\ `
Trzeba przy tym wziąć pod uwagę, że dla wierszowych macierzy permutacji
:math:`\ \boldsymbol{P}_{\sigma}\ \ ` i :math:`\ ` kolumnowych 
macierzy permutacji :math:`\ \boldsymbol{Q}_{\sigma}\ ` 
:math:`\ (\sigma\in S_6)\ \ ` zachodzą związki

.. math::
   
   \boldsymbol{P}_{\rho\ \cdot\ \sigma}\, = \ 
   \boldsymbol{P}_{\sigma}\,\cdot\,\boldsymbol{P}_{\rho}\,,\qquad
   \boldsymbol{Q}_{\rho\ \cdot\ \sigma}\, =\ 
   \boldsymbol{Q}_{\rho}\ \cdot\ \boldsymbol{Q}_{\sigma}\,,\qquad
   \rho,\sigma\in S_6\,.

Na tej zasadzie obydwu iloczynom macierzy,
:math:`\ \boldsymbol{P}_{56}\ \boldsymbol{P}_{46}\ \boldsymbol{P}_{24}\ `
oraz
:math:`\ \boldsymbol{Q}_{24}\ \boldsymbol{Q}_{46}\ \boldsymbol{Q}_{56}\,,\ `
odpowiada ten sam iloczyn transpozycji
:math:`\ \tau_{24}\ \tau_{46}\ \tau_{56}\,.\ ` 
Otrzymujemy stąd ponownie permutację :math:`\ \sigma:`

.. math::
   
   \begin{array}{ll}
   \sigma & = \ \ \tau_{24}\ \tau_{46}\ \tau_{56}\ \ = 
   \\[9pt] 
   & =\ \ \left(\begin{array}{cccccc}
   1 & 2 & 3 & 4 & 5 & 6 \\
   1 & 4 & 3 & 2 & 5 & 6
   \end{array}\right)\ 
   \left(\begin{array}{cccccc}
   1 & 2 & 3 & 4 & 5 & 6 \\
   1 & 2 & 3 & 6 & 5 & 4
   \end{array}\right)\ 
   \left(\begin{array}{cccccc}
   1 & 2 & 3 & 4 & 5 & 6 \\
   1 & 2 & 3 & 4 & 6 & 5
   \end{array}\right)\ \ = 
   \\[10pt] 
   & = \ \ \left(\begin{array}{cccccc}
   1 & 2 & 3 & 4 & 5 & 6 \\
   1 & 4 & 3 & 6 & 2 & 5
   \end{array}\right).
   \end{array}


.. **Rozwiązanie** :math:`\,` dla :math:`\,` :math:`n=3\ ` 
   (wersja kolumnowo-wierszowa):

.. math:

   \begin{array}{llll}   
   \boldsymbol{A}\otimes\boldsymbol{I}_3 & 
   \ =\ \ \ 
   \left[\begin{array}{cc}
   a_{11}\ \boldsymbol{I}_3 & a_{12}\ \boldsymbol{I}_3 \\
   a_{21}\ \boldsymbol{I}_3 & a_{22}\ \boldsymbol{I}_3
   \end{array}\right]\ \ =\ \ &
   \left[\begin{array}{ccc|ccc}
   a_{11} &    0   &    0   & a_{12} &    0   &    0   \\
      0   & a_{11} &    0   &    0   & a_{12} &    0   \\
      0   &    0   & a_{11} &    0   &    0   & a_{12} \\ \hline
   a_{21} &    0   &    0   & a_{22} &    0   &    0   \\
      0   & a_{21} &    0   &    0   & a_{22} &    0   \\
      0   &    0   & a_{21} &    0   &    0   & a_{22} 
   \end{array}\right]\ \ \rightarrow & \qquad\quad
   \end{array}
   \\[10pt]
   \begin{array}{ccc}
   \ \ C_2\leftrightarrow C_4: & R_2\leftrightarrow R_4: \\[5pt]
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
      0   &    0   &    0   & a_{11} & a_{12} &    0   \\
      0   &    0   & a_{11} &    0   &    0   & a_{12} \\ 
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   &    0   & a_{21} & a_{22} &    0   \\
      0   &    0   & a_{21} &    0   &    0   & a_{22} 
   \end{array}\right] & 
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   & a_{11} &    0   &    0   & a_{12} \\
      0   &    0   &    0   & a_{11} & a_{12} &    0   \\ 
      0   &    0   &    0   & a_{21} & a_{22} &    0   \\
      0   &    0   & a_{21} &    0   &    0   & a_{22} 
   \end{array}\right]\ \ \rightarrow & 
   \end{array}
   \\[10pt]
   \begin{array}{ccc}
   C_4\leftrightarrow C_6: & R_4\leftrightarrow R_6: \\[5pt]
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   & a_{11} & a_{12} &    0   &    0   \\
      0   &    0   &    0   &    0   & a_{12} & a_{11} \\ 
      0   &    0   &    0   &    0   & a_{22} & a_{21} \\
      0   &    0   & a_{21} & a_{22} &    0   &    0  
   \end{array}\right] & 
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   & a_{11} & a_{12} &    0   &    0   \\
      0   &    0   & a_{21} & a_{22} &    0   &    0   \\
      0   &    0   &    0   &    0   & a_{22} & a_{21} \\
      0   &    0   &    0   &    0   & a_{12} & a_{11}
   \end{array}\right] \ \ \rightarrow &
   \end{array}
   \\[10pt]
   \begin{array}{ccc}
   C_5\leftrightarrow C_6: & R_5\leftrightarrow R_6: \\[5pt]
   \rightarrow\ \ 
   \left[\begin{array}{cccccc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\
      0   &    0   & a_{11} & a_{12} &    0   &    0   \\
      0   &    0   & a_{21} & a_{22} &    0   &    0   \\
      0   &    0   &    0   &    0   & a_{21} & a_{22} \\
      0   &    0   &    0   &    0   & a_{11} & a_{12}
   \end{array}\right] & 
   \rightarrow\ \ 
   \left[\begin{array}{cc|cc|cc}
   a_{11} & a_{12} &    0   &    0   &    0   &    0   \\
   a_{21} & a_{22} &    0   &    0   &    0   &    0   \\ \hline
      0   &    0   & a_{11} & a_{12} &    0   &    0   \\
      0   &    0   & a_{21} & a_{22} &    0   &    0   \\ \hline
      0   &    0   &    0   &    0   & a_{11} & a_{12} \\
      0   &    0   &    0   &    0   & a_{21} & a_{22}
   \end{array}\right] \ \ = & 
   \boldsymbol{I}_3\otimes\boldsymbol{A}\,.
   \end{array}

.. :math:`\,`

.. **Rozwiązanie** :math:`\,` dla :math:`\,` :math:`n=2\ ` 
   (wersja kolumnowo-wierszowa):

.. math:
   
   \begin{array}{rrr}
   \boldsymbol{A}\otimes\boldsymbol{I}_2 & =\ \ 
   \left[\begin{array}{cc}
   a_{11}\ \boldsymbol{I}_2 & a_{12}\ \boldsymbol{I}_2 \\
   a_{21}\ \boldsymbol{I}_2 & a_{22}\ \boldsymbol{I}_2
   \end{array}\right]\ \ =\ \ 
   \left[\begin{array}{cc|cc}
   a_{11} &   0    & a_{12} &   0    \\
     0    & a_{11} &   0    & a_{12} \\ \hline
   a_{21} &   0    & a_{22} &   0    \\
     0    & a_{21} &   0    & a_{22}
   \end{array}\right]\ \ \rightarrow &
   \end{array}
   \\[10pt] 
   \begin{array}{rcl}
   & \ \ C_2\leftrightarrow C_3:
   \qquad\qquad\qquad\qquad 
   R_2\leftrightarrow R_3: &
   \\[5pt]
   & \rightarrow\ \ 
   \left[\begin{array}{cccc}
   a_{11} & a_{12} &   0    &   0    \\
     0    &   0    & a_{11} & a_{12} \\
   a_{21} & a_{22} &   0    &   0    \\
     0    &   0    & a_{21} & a_{22}
   \end{array}\right]\ \ \rightarrow\ \ 
   \left[\begin{array}{cc|cc}
   a_{11} & a_{12} &   0    &   0    \\
   a_{21} & a_{22} &   0    &   0    \\ \hline
     0    &   0    & a_{11} & a_{12} \\
     0    &   0    & a_{21} & a_{22}
   \end{array}\right]\ \ =\  
   & \boldsymbol{I}_2\otimes\boldsymbol{A}\,.
   \end{array}

**Zadanie 2.**

.. Wykorzystując podaną w tym rozdziale interpretację 
   iloczynu prostego dwóch macierzy :

.. admonition: :math:`\,`

   Jeżeli :math:`\ \boldsymbol{A}\in M_{m\times n}(K),\ `
   :math:`\ \boldsymbol{B}\in M_{p\times q}(K),\ ` to
   :math:`\ \boldsymbol{A}\otimes\boldsymbol{B}\ `
   jest macierzą homomorfizmu
   
   .. math::
   
      F_{AB}\,:\qquad 
      M_{n\times q}(K)\ni\boldsymbol{G}
      \ \ \mapsto\ \ 
      F_{AB}(\boldsymbol{G}) :\,=
      \boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T\in M_{m\times p}(K)
   
   w bazach kanonicznych 
   :math:`\ \mathcal{E}_{n\times q}\ ` i :math:`\ \ \mathcal{E}_{m\times p}\ `
   przestrzeni :math:`\ M_{n\times q}(K)\ ` i :math:`\ M_{m\times p}(K).\ `
   Wówczas
   
   .. math::
      :label: main-1
      
      (\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
      \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})
      \ \,=\ \,
      \boldsymbol{\Lambda}^{mp}
      (\boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T)\,,

   
   gdzie :math:`\ \boldsymbol{\Lambda}^{rs}(\boldsymbol{X})\ `
   jest kolumną współrzędnych macierzy 
   :math:`\ \boldsymbol{X}\in M_{r\times s}(K)\ `
   w bazie :math:`\ \mathcal{E}_{r\times s}\,.`

.. gdzie :math:`\ \ \boldsymbol{A}\in M_{m\times n}(K),\ `
   :math:`\ \boldsymbol{B},\,\boldsymbol{B}_1,\boldsymbol{B}_2
   \in M_{p\times q}(K)\,.`

Udowodnij, że dla 
:math:`\ \,\boldsymbol{A}\in M_{m\times n}(K),\ `
:math:`\ \boldsymbol{B},\,\boldsymbol{B}_1,\boldsymbol{B}_2
\in M_{p\times q}(K)\,:` 

.. math::
   
   \boldsymbol{A}\otimes(\boldsymbol{B}_1 +\,\boldsymbol{B}_2)\ \,=\ \,
   (\boldsymbol{A}\otimes\boldsymbol{B}_1)\ +\ 
   (\boldsymbol{A}\otimes\boldsymbol{B}_2)\,,

   (\gamma\,\boldsymbol{A})\otimes\boldsymbol{B}\ =\
   \boldsymbol{A}\otimes(\gamma\,\boldsymbol{B})\ =\ 
   \gamma\ (\boldsymbol{A}\otimes\boldsymbol{B}),\quad\gamma\in K.

**Wskazówka.**

Jeżeli :math:`\ \boldsymbol{A}\in M_{m\times n}(K),\ `
:math:`\ \boldsymbol{B}\in M_{p\times q}(K),\ ` to
:math:`\ \boldsymbol{A}\otimes\boldsymbol{B}\ `
jest macierzą homomorfizmu
   
.. math::

   F_{AB}\,:\qquad 
   M_{n\times q}(K)\ni\boldsymbol{G}
   \ \ \mapsto\ \ 
   F_{AB}(\boldsymbol{G}) :\,=
   \boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T\in M_{m\times p}(K)

w bazach kanonicznych 
:math:`\ \mathcal{E}_{n\times q}\ ` i :math:`\ \ \mathcal{E}_{m\times p}\ `
przestrzeni :math:`\ M_{n\times q}(K)\ ` i :math:`\ M_{m\times p}(K).\ `

Wówczas

.. math::
   :label: main-1
   
   (\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})
   \ \,=\ \,
   \boldsymbol{\Lambda}^{mp}
   (\boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T)\,,
   \qquad\boldsymbol{G}\in M_{n\times q}(K)\,,

gdzie :math:`\ \boldsymbol{\Lambda}^{rs}(\boldsymbol{X})\ `
jest kolumną współrzędnych macierzy 
:math:`\ \boldsymbol{X}\in M_{r\times s}(K)\ `
w bazie :math:`\ \mathcal{E}_{r\times s}\,.`

**Dowód.**   

Podstawiając w :eq:`main-1` 
:math:`\ \boldsymbol{B}\to\boldsymbol{B}_1 + \boldsymbol{B}_2\,,\ ` gdzie 
:math:`\ \boldsymbol{B}_1,\ \boldsymbol{B}_2 \in M_{p\times q}(K),\ `
otrzymamy

.. math::
   
   \begin{array}{ll}
   \left[\,\boldsymbol{A}\otimes\,(\boldsymbol{B}_1 + \boldsymbol{B}_2)\,\right]
   \,\cdot\,\boldsymbol{\Lambda}^{nq}(\boldsymbol{G}) & 
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,\boldsymbol{A}\ \boldsymbol{G}\ 
   (\boldsymbol{B}_1 + \boldsymbol{B}_2)^T\,\right]\ =
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,\boldsymbol{A}\ \boldsymbol{G}\ 
   (\boldsymbol{B}_1^T + \boldsymbol{B}_2^T)\,\right]\ =
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}\,\boldsymbol{G}\,\boldsymbol{B}_1^T + \,
   \boldsymbol{A}\,\boldsymbol{G}\,\boldsymbol{B}_2^T\right)\ =
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}\,\boldsymbol{G}\,\boldsymbol{B}_1^T\right)\ +\ 
   \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}\,\boldsymbol{G}\,\boldsymbol{B}_2^T\right)\ =
   \\[6pt] &
   =\ \ (\boldsymbol{A}\otimes\boldsymbol{B}_1)\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\ +\ 
   (\boldsymbol{A}\otimes\boldsymbol{B}_2)\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\ =
   \\[6pt] &
   =\ \ \left[\,(\boldsymbol{A}\otimes\boldsymbol{B}_1)\ +\ 
   (\boldsymbol{A}\otimes\boldsymbol{B}_2)\,\right]\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})
   \end{array}

dla dowolnej macierzy :math:`\ \boldsymbol{G}\in M_{n\times q}(K).\ `
Wynika stąd równość macierzowa

.. math::
   
   \boldsymbol{A}\otimes(\boldsymbol{B}_1 +\,\boldsymbol{B}_2)\ \,=\ \,
   (\boldsymbol{A}\otimes\boldsymbol{B}_1)\ +\ 
   (\boldsymbol{A}\otimes\boldsymbol{B}_2)\,,

którą należało udowodnić.
Podstawiając w :eq:`main-1` 
:math:`\ \boldsymbol{A}\to\gamma\,\boldsymbol{A}\,,\ ` 
gdzie :math:`\ \gamma\in K,\ ` otrzymamy

.. math::
   
   \begin{array}{ll}
   \left[\,(\gamma\,\boldsymbol{A})\otimes\boldsymbol{B}\,\right]
   \,\cdot\,\boldsymbol{\Lambda}^{nq}(\boldsymbol{G}) & 
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,(\gamma\,\boldsymbol{A})\ 
   \boldsymbol{G}\,\boldsymbol{B}^T\,\right]\ =
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,\gamma\ (\boldsymbol{A}\,\boldsymbol{G}\,\boldsymbol{B}^T)\right]\ =
   \\[6pt] &
   =\ \ \gamma\,\cdot\,\boldsymbol{\Lambda}^{mp}
   \left(\,\boldsymbol{A}\,\boldsymbol{G}\,\boldsymbol{B}^T\,\right)\ =
   \\[6pt] &
   =\ \ \gamma\,\cdot\,
   \left[\,(\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\,\right]\ =
   \\[6pt] &
   =\ \ \left[\,\gamma\,\cdot\,(\boldsymbol{A}\otimes\boldsymbol{B})\,\right]\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})
   \end{array}

dla dowolnej macierzy :math:`\ \boldsymbol{G}\in M_{n\times q}(K).\ `
Oznacza to równość macierzy

.. math::
   
   (\gamma\,\boldsymbol{A})\otimes\boldsymbol{B}\ \,=\ \,
   \gamma\ \,(\boldsymbol{A}\otimes\boldsymbol{B}),\quad\gamma\in K.

Analogicznie dowodzi się, że :math:`\ \,\boldsymbol{A}\otimes
(\gamma\,\boldsymbol{B})\ =\ \gamma\ (\boldsymbol{A}\otimes\boldsymbol{B}),
\quad\gamma\in K.`





























