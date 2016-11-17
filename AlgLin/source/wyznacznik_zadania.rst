
Zadania
-------

**Zadanie 1.** :math:`\ ` Niech

.. math::
   
   \boldsymbol{C}\ \ =\ \ 
   \left[\begin{array}{cc}
   \boldsymbol{A} & \boldsymbol{0}\, \\[4pt]
   \cdots         & \boldsymbol{B}\,
   \end{array}\right]
   \ \ =\ \ 
   \left[\begin{array}{ccc|ccc}
   a_{11} & \ldots & a_{1p} &    0   & \ldots &    0   \\[4pt]
   \ldots & \ldots & \ldots & \ldots & \ldots & \ldots \\[4pt]
   a_{p1} & \ldots & a_{pp} &    0   & \ldots &    0   \\[4pt] \hline
   \ldots & \ldots & \ldots & b_{11} & \ldots & b_{1q} \\[4pt]
   \ldots & \ldots & \ldots & \ldots & \ldots & \ldots \\[4pt]
   \ldots & \ldots & \ldots & b_{q1} & \ldots & b_{qq}
   \end{array}\right]

gdzie w lewym dolnym prostokącie występują dowolne elementy.
Udowodnij, że

.. math::
   
   \det{\boldsymbol{C}}\ \,=\ \,
   \det{\boldsymbol{A}}\,\cdot\,\det{\boldsymbol{B}}\,.

**Dowód.** :math:`\ ` Indukcja ze względu na :math:`\ q.`

**I.** :math:`\ ` Sprawdzamy twierdzenie dla :math:`\ q = 1.\ ` 
Wtedy :math:`\ \boldsymbol{B}\ =\ [b_{11}]_{1 \times 1}:`

.. math::
   
   \boldsymbol{C}\ \ =\ \ 
   \left[\begin{array}{ccc|c}
   a_{11} & \ldots & a_{1p} &    0   \\[4pt]
   \ldots & \ldots & \ldots & \ldots \\[4pt]
   a_{p1} & \ldots & a_{pp} &    0   \\[4pt] \hline
   \ldots & \ldots & \ldots & b_{11}
   \end{array}\right]

Stosując rozwinięcie Laplace'a względem ostatniej kolumny otrzymujemy

.. math::
   
   \det{\boldsymbol{C}}\ \,=\ \,
   b_{11}\,\cdot\:(-1)^{2\,(p+1)}\ \det{\boldsymbol{A}}\ \,=\ \,
   \det{\boldsymbol{A}}\,\cdot\:b_{11}\ \,=\ \,
   \det{\boldsymbol{A}}\,\cdot\,\det{\boldsymbol{B}}\,.

**II.** :math:`\ `
Zakładamy, że twierdzenie jest prawdziwe dla :math:`\ q-1.\ \\`
Należy dowieść, że jest wtedy prawdziwe dla :math:`\ q.`

Oznaczenia (:math:`i=1,2,\ldots,q`):

:math:`M_{iq}\ -\ ` minor macierzy :math:`\ \boldsymbol{B}\ `
po skreśleniu :math:`\ i`-tego wiersza oraz :math:`\ q`-tej kolumny;

:math:`B_{iq}\ -\ ` dopełnienie algebraiczne elementu :math:`\ b_{iq}\ `
w macierzy :math:`\ \boldsymbol{B};`

:math:`C_{iq}\ -\ ` dopełnienie algebraiczne elementu :math:`\ b_{iq}\ `
w macierzy :math:`\ \boldsymbol{C}.`

Na podstawie założenia indukcyjnego mamy

.. math::
   
   \begin{array}{rl}
   C_{iq} & =\ \ (-1)^{(p+i)+(p+q)}\ \cdot\ 
   \det{\boldsymbol{A}}\ \cdot\ M_{iq}\ \ = \\
   & =\ \ (-1)^{2p+(i+q)}\ \cdot\ \det{\boldsymbol{A}}\ \cdot\ M_{iq}\ \ = \\
   & =\ \ \det{\boldsymbol{A}}\ \cdot\ (-1)^{i+q}\ \cdot\ M_{iq}\ \ =\ \ 
   \det{\boldsymbol{A}}\ \cdot\ B_{iq}\,.
   \end{array}

Rozwinięcie Laplace'a względem ostatniej kolumny 
macierzy :math:`\ \boldsymbol{C}\ ` daje

.. math::
   
   \det{\boldsymbol{C}}\ \,=\ \,
   \displaystyle\sum_{i=1}^q\ b_{iq}\,C_{iq}\ =\ 
   \det{\boldsymbol{A}}\ \cdot\ \displaystyle\sum_{i=1}^q\,b_{iq}\ B_{iq}\ =\ 
   \det{\boldsymbol{A}}\ \cdot\ \det{\boldsymbol{B}}\,,

co kończy dowód.

**Wniosek:** :math:`\\` Jeżeli 
:math:`\ \boldsymbol{A}_1,\,\boldsymbol{A}_2,\,\ldots,\,\boldsymbol{A}_k\ `
są macierzami kwadratowymi (być może różnych stopni), :math:`\\`
to dla wyznacznika utworzonej z nich diagonalnej macierzy klatkowej 
obowiązuje wzór

.. math::
   
   \left|\begin{array}{cccc}
   \boldsymbol{A}_1 & \boldsymbol{0}   & \ldots & \boldsymbol{0}   \\[4pt]
   \boldsymbol{0}   & \boldsymbol{A}_2 & \ldots & \boldsymbol{0}   \\[4pt]
   \cdots           & \cdots           & \cdots & \cdots           \\[4pt]
   \boldsymbol{0}   & \boldsymbol{0}   & \ldots & \boldsymbol{A}_k
   \end{array}\right|\ \ =\ \ 
   \det{\boldsymbol{A}_1}\ \cdot\ \det{\boldsymbol{A}_2}
   \ \cdot\ \ldots\ \cdot\ \det{\boldsymbol{A}_k}\,.

W szczególności, jeżeli :math:`\ \boldsymbol{I}_n\in M_n(K)\ `
jest macierzą jednostkową, :math:`\ \boldsymbol{A}\in M_m(K),\ ` to

.. math::
   
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\ \ =\ \ 
   \underbrace{
   \left|\begin{array}{cccc}
   \boldsymbol{A} & \boldsymbol{0} & \cdots & \boldsymbol{0} \\[3pt]
   \boldsymbol{0} & \boldsymbol{A} & \cdots & \boldsymbol{0} \\[3pt]
   \cdots & \cdots & \cdots & \cdots                         \\[3pt]
   \boldsymbol{0} & \boldsymbol{0} & \cdots & \boldsymbol{A}
   \end{array}\right|}_{n\ \text{bloków}}\ \ =\ \ 
   \left(\det{\boldsymbol{A}}\right)^n.

  



























   

