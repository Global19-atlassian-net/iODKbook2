
Operacje na macierzach
----------------------

Operacje i macierze elementarne
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Aby wykonać operację elementarną :math:`\,O\,` na iloczynie dwóch macierzy
:math:`\,\boldsymbol{A}\ \ \text{i}\ \ \boldsymbol{B},\ ` :math:`\\` 
należy zastosować ją tylko do pierwszego czynnika iloczynu:
:math:`\ O(\boldsymbol{A}\boldsymbol{B}) = (O\boldsymbol{A})\,\boldsymbol{B}.\ ` 
:math:`\\` Dokładniej wyraża to

.. admonition:: Lemat. :math:`\,`
   
   Jeżeli 
   :math:`\,\boldsymbol{A}\in M_{m\times p}(K),\ 
   \boldsymbol{B}\in M_{p\times n}(K),\ ` 
   to :math:`\,` dla :math:`\ i,j=0,1,\ldots,m-1:`
   
   #. :math:`\ O_1(i,j)\,(\boldsymbol{A}\boldsymbol{B})\ \ =\ \ 
      [\,O_1(i,j)\,\boldsymbol{A}\,]\ \boldsymbol{B}\,,`

   #. :math:`\ O_2(i,a)\,(\boldsymbol{A}\boldsymbol{B})\ \ =\ \ 
      [\,O_2(i,a)\,\boldsymbol{A}\,]\ \boldsymbol{B}\,,\qquad (a\ne 0)`

   #. :math:`\ O_3(i,j,a)\,(\boldsymbol{A}\boldsymbol{B})\ \ =\ \ 
      [\,O_3(i,j,a)\,\boldsymbol{A}\,]\ \boldsymbol{B}\,.`

**Dowód** wykorzystuje wierszową regułę mnożenia macierzowego:

.. math::

   \boldsymbol{A}\boldsymbol{B}\ \equiv\    
   \left[\begin{array}{c}
         \boldsymbol{A}_1 \\ 
         \boldsymbol{A}_2 \\
         \dots            \\
         \boldsymbol{A}_m \end{array}\right]\boldsymbol{B}
   \ \ =\ \   
   \left[\begin{array}{c}
         \boldsymbol{A}_1\,\boldsymbol{B} \\ 
         \boldsymbol{A}_2\,\boldsymbol{B} \\
         \dots            \\
         \boldsymbol{A}_m\,\boldsymbol{B} \end{array}\right]\,.

Wobec tego wyprowadzenie związków 
:math:`\,` 1., :math:`\,` 2. :math:`\,` i :math:`\,` 3. :math:`\,`
przebiega następująco:

.. math::
   
   O_1(i,j)\,(\boldsymbol{A}\boldsymbol{B})\ =\ 
   O_1(i,j)\,
   \left[\begin{array}{c}
         \dots                            \\ 
         \boldsymbol{A}_i\,\boldsymbol{B} \\ 
         \dots                            \\ 
         \boldsymbol{A}_j\,\boldsymbol{B} \\
         \dots                            \\
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \dots                            \\ 
         \boldsymbol{A}_j\,\boldsymbol{B} \\ 
         \dots                            \\ 
         \boldsymbol{A}_i\,\boldsymbol{B} \\
         \dots                            \\
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \dots            \\ 
         \boldsymbol{A}_j \\ 
         \dots            \\ 
         \boldsymbol{A}_i \\
         \dots            \\   
         \end{array}
   \right]\,\boldsymbol{B}\ =\ 
   [\,O_1(i,j)\,\boldsymbol{A}\,]\,\boldsymbol{B}\ ;

   O_2(i,a)\,(\boldsymbol{A}\boldsymbol{B})\ =\ 
   O_2(i,a)\,
   \left[\begin{array}{c}
         \boldsymbol{A}_1\,\boldsymbol{B} \\ 
         \dots                            \\ 
         \boldsymbol{A}_i\,\boldsymbol{B} \\ 
         \dots                            \\ 
         \boldsymbol{A}_m\,\boldsymbol{B} \\
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \boldsymbol{A}_1\,\boldsymbol{B}    \\ 
         \dots                               \\ 
         a\,\boldsymbol{A}_i\,\boldsymbol{B} \\ 
         \dots                               \\ 
         \boldsymbol{A}_m\,\boldsymbol{B}    \\
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \boldsymbol{A}_1    \\ 
         \dots               \\ 
         a\,\boldsymbol{A}_i \\ 
         \dots               \\ 
         \boldsymbol{A}_m    \\
         \end{array}
   \right]\boldsymbol{B}\ =\ 
   [\,O_2(i,a)\,\boldsymbol{A}\,]\ \boldsymbol{B}\,;

.. math::

   O_3(i,j,a)\,(\boldsymbol{A}\boldsymbol{B})\ \ =\ \  
   O_3(i,j,a)\,
   \left[\begin{array}{c}
         \dots                            \\ 
         \boldsymbol{A}_i\,\boldsymbol{B} \\ 
         \dots                            \\ 
         \boldsymbol{A}_j\,\boldsymbol{B} \\
         \dots                            \\
         \end{array}
   \right]\ \ =\ \ 
   \left[\begin{array}{c}
         \dots                                      \\ 
         \boldsymbol{A}_i\,\boldsymbol{B}\, +\, a\,
         \boldsymbol{A}_j\,\boldsymbol{B}           \\ 
         \dots                                      \\ 
         \boldsymbol{A}_j\,\boldsymbol{B}           \\
         \dots                                      \\
         \end{array}
   \right]\ \ =
               
   =\ \ \ 
   \left[\begin{array}{c}
         \dots                                                      \\ 
         (\boldsymbol{A}_i\ + \, a\boldsymbol{A}_j)\,\boldsymbol{B} \\ 
         \dots                                                      \\ 
         \boldsymbol{A}_j\,\boldsymbol{B}                           \\
         \dots                                                      \\
         \end{array}
   \right]\ \ \ =\ \ \ 
   \left[\begin{array}{c}
         \dots                                 \\ 
         \boldsymbol{A}_i\ + a\boldsymbol{A}_j \\ 
         \dots                                 \\ 
         \boldsymbol{A}_j                      \\
         \dots                                 \\    
         \end{array}
   \right]\,\boldsymbol{B}\ \ \ =\ \ \ 
   [\,O_3(i,j,a)\,\boldsymbol{A}\,]\ \boldsymbol{B}\,.


Wykonanie operacji elementarnej na prostokątnej macierzy 
:math:`\,\boldsymbol{A}\ ` jest równoważne pomnożeniu (z lewej strony)
tej macierzy przez odpowiednią macierz elementarną. Zapiszemy to jako

.. admonition:: Twierdzenie. :math:`\,` 

   Niech :math:`\,\boldsymbol{A}\in M_{m\times n}(K).\ ` 
   Wtedy :math:`\,` dla :math:`\ i,j=0,1,\ldots,m-1:`

   #. :math:`\ O_1(i,j)\,\boldsymbol{A}\ =
      \ \boldsymbol{E}_1(i,j)\,\boldsymbol{A}\,,`
   #. :math:`\ O_2(i,a)\,\boldsymbol{A}\ =
      \ \boldsymbol{E}_2(i,a)\,\boldsymbol{A}\,,\qquad (a\ne 0)`
   #. :math:`\ O_3(i,j,a)\,\boldsymbol{A}\ =
      \ \boldsymbol{E}_3(i,j,a)\,\boldsymbol{A}\,,`

   gdzie 
   :math:`\ \ \boldsymbol{E}_1(i,j),\ 
   \boldsymbol{E}_2(i,a),\ \boldsymbol{E}_3(i,j,a)\in M_m(K).`

**Dowód.** :math:`\,` Biorąc pod uwagę że 
:math:`\,\boldsymbol{A} = \boldsymbol{I}_m\boldsymbol{A},\ `
korzystając z lematu i odwołując się do definicji macierzy elementarnych, 
otrzymujemy:

:math:`\ O_1(i,j)\,\boldsymbol{A}\ =
\ O_1(i,j)\,(\boldsymbol{I}_m\boldsymbol{A})\ =
\ [\,O_1(i,j)\,\boldsymbol{I}_m\,]\,\boldsymbol{A}\ =
\ \boldsymbol{E}_1(i,j)\,\boldsymbol{A}\,,`

:math:`\ O_2(i,a)\,\boldsymbol{A}\ =
\ O_2(i,a)\,(\boldsymbol{I}_m\boldsymbol{A})\ =
\ [\,O_2(i,a)\,\boldsymbol{I}_m\,]\,\boldsymbol{A}\ =
\ \boldsymbol{E}_2(i,a)\,\boldsymbol{A}\,,`

:math:`\ O_3(i,j,a)\,\boldsymbol{A}\ =
\ O_3(i,j,a)\,(\boldsymbol{I}_m\boldsymbol{A})\ =
\ [\,O_3(i,j,a)\,\boldsymbol{I}_m\,]\,\boldsymbol{A}\ =
\ \boldsymbol{E}_3(i,j,a)\,\boldsymbol{A}\,.`

Macierze elementarne są odwracalne, przy czym odwrotność 
macierzy elementarnej jest macierzą elementarną. Dokładnie przedstawia to

.. admonition:: Twierdzenie. :math:`\,`
   
   Jeżeli :math:`\ i,j=0,1,\ldots,m-1;\ i \neq j\,,\ m=1,2,\ldots ,\ ` to
   
   #. :math:`\,[\boldsymbol{E}_1(i,j)]^{-1}\,=\ \boldsymbol{E}_1(i,j),`
   #. :math:`\,[\boldsymbol{E}_2(i,a)]^{-1}\,=
      \ \boldsymbol{E}_2(i,a^{-1}),\qquad (a\ne 0)`
   #. :math:`\,[\boldsymbol{E}_3(i,j,a)]^{-1}\,=\ \boldsymbol{E}_3(i,j,-a).`

**Dowód** przebiega podobnie dla wszystkich trzech rodzajów 
macierzy elementarnych.

1.) :math:`\:`\ Dwukrotne przestawienie :math:`i`-tego oraz :math:`j`-tego 
wiersza jest operacją identycznościową:

.. math::
   
   [\,O_1(i,j)\,\circ\,O_1(i,j)\,]\ \ \boldsymbol{I}_m\ \ =
   \ \ \boldsymbol{I}_m\,.

Lewą stronę można przekształcić następująco:

.. math::
   
   [\,O_1(i,j)\,\circ\,O_1(i,j)\,]\ \,\boldsymbol{I}_m\ =\ 
   O_1(i,j)\ [\,O_1(i,j)\,\boldsymbol{I}_m\,]\ =\ 
   O_1(i,j)\,\boldsymbol{E}_1(i,j)\ =
   
   =\ O_1(i,j)\ [\,\boldsymbol{I}_m\,\boldsymbol{E}_1(i,j)\,]\ =\ 
   [\,O_1(i,j)\ \boldsymbol{I}_m\,]\ \boldsymbol{E}_1(i,j)\ =\ 
   \boldsymbol{E}_1(i,j) \cdot \boldsymbol{E}_1(i,j)

W ten sposób 
:math:`\ \ \boldsymbol{E}_1(i,j) \cdot \boldsymbol{E}_1(i,j)\ =
\ \boldsymbol{I}_m\,,\ ` co oznacza, że
:math:`\ [\boldsymbol{E}_1(i,j)]^{-1} =\ \boldsymbol{E}_1(i,j)\,.`

2.) :math:`\:` Złożenie operacji :math:`\,O_2(i,a)\ \,` i 
:math:`\ \ O_2(i,a^{-1})\,` jest operacją identycznościową:

.. math::
   
   [\,O_2(i,a^{-1})\,\circ\,O_2(i,a)\,]\ \ \boldsymbol{I}_m\ \ =
   \ \ \boldsymbol{I}_m\,.

Lewą stronę można przepisać jako

.. math::
   
   [\,O_2(i,a^{-1})\,\circ\,O_2(i,a)\,]\ \,\boldsymbol{I}_m\ =\ 
   O_2(i,a^{-1})\ [\,O_2(i,a)\,\boldsymbol{I}_m\,]\ =\ 
   O_2(i,a^{-1})\,\boldsymbol{E}_2(i,a)\ =
   
   =\ O_2(i,a^{-1})\ [\,\boldsymbol{I}_m\,\boldsymbol{E}_2(i,a)\,]\ =\ 
   [\,O_2(i,a^{-1})\ \boldsymbol{I}_m\,]\ \boldsymbol{E}_2(i,a)\ =\ 
   \boldsymbol{E}_2(i,a^{-1}) \cdot \boldsymbol{E}_2(i,a)

A zatem
:math:`\ \ \boldsymbol{E}_2(i,a^{-1}) \cdot \boldsymbol{E}_2(i,a)\ =
\ \boldsymbol{I}_m\,,\ ` wobec czego
:math:`\ [\boldsymbol{E}_2(i,a)]^{-1} =\ \boldsymbol{E}_2(i,a^{-1})\,.`

3.) :math:`\ ` Złożenie operacji :math:`\,O_3(i,j,a)\ \,` i 
:math:`\ \ O_3(i,j,-a)\,` jest operacją identycznościową:

.. math::
   
   [\,O_3(i,j,-a)\,\circ\,O_3(i,j,a)\,]\ \ \boldsymbol{I}_m\ \ =
   \ \ \boldsymbol{I}_m\,.

Lewa strona przyjmuje teraz postać
   
.. math::
   
   [\,O_3(i,j,-a)\,\circ\,O_3(i,j,a)\,]\ \,\boldsymbol{I}_m\ =\ 
   O_3(i,j,-a)\ [\,O_3(i,j,a)\,\boldsymbol{I}_m\,]\ =\ 
   O_3(i,j,-a)\,\boldsymbol{E}_3(i,j,a)\ =
   
   =\ O_3(i,j,-a)\ [\,\boldsymbol{I}_m\,\boldsymbol{E}_3(i,j,a)\,]\ =\ 
   [\,O_3(i,j,-a)\ \boldsymbol{I}_m\,]\ \boldsymbol{E}_3(i,j,a)\ =\ 
   \boldsymbol{E}_3(i,j,-a) \cdot \boldsymbol{E}_3(i,j,a)
   
Tak więc
:math:`\ \ \boldsymbol{E}_3(i,j,-a) \cdot \boldsymbol{E}_3(i,j,a)\ =
\ \boldsymbol{I}_m\,,\ ` skąd
:math:`\ [\boldsymbol{E}_3(i,j,a)]^{-1} =\ \boldsymbol{E}_3(i,j,-a)\,.`


Macierze permutacji
~~~~~~~~~~~~~~~~~~~

Aby wykonać operację permutacji wierszy :math:`\,O_{\sigma}\,` 
na iloczynie dwóch macierzy 
:math:`\,\boldsymbol{A}\ \ \text{i}\ \ \boldsymbol{B},\ ` :math:`\\` 
należy zastosować ją tylko do pierwszego czynnika iloczynu.

Wykonanie operacji permutacji wierszy :math:`\,O_{\sigma}\,` 
na prostokątnej macierzy :math:`\,\boldsymbol{A}\ ` jest równoważne 
pomnożeniu (z lewej strony) tej macierzy przez odpowiednią macierz permutacji.

Dokładnie ujmuje to następujące

.. admonition:: Twierdzenie. :math:`\,`
   
   Jeżeli :math:`\,\boldsymbol{A}\in M_{m\times p}(K),\ \boldsymbol{B}
   \in M_{p\times n}(K),\ \ \sigma\in S_m,\ \ ` to: 

   1. :math:`\ \,O_\sigma\,(\boldsymbol{A}\boldsymbol{B})\ =
      \ (O_\sigma\boldsymbol{A})\,\boldsymbol{B}\,;`
   2. :math:`\ \,O_\sigma\,\boldsymbol{A}\ =
      \ \boldsymbol{P}_\sigma\,\boldsymbol{A}\,,\qquad
      \text{gdzie}\quad\boldsymbol{P}_\sigma\,=
      \,O_\sigma\,\boldsymbol{I}_m\in M_m(K)\,.`

**Dowód** opiera się na wierszowej regule mnożenia macierzowego:

.. math::

   \boldsymbol{A}\boldsymbol{B}\ \equiv\    
   \left[\begin{array}{c}
         \boldsymbol{A}_1 \\ 
         \boldsymbol{A}_2 \\
         \dots            \\
         \boldsymbol{A}_m \\ 
         \end{array}
   \right]\boldsymbol{B}\ \ =\ \   
   \left[\begin{array}{c}
         \boldsymbol{A}_1\,\boldsymbol{B} \\ 
         \boldsymbol{A}_2\,\boldsymbol{B} \\
         \dots                            \\
         \boldsymbol{A}_m\,\boldsymbol{B} \\ 
         \end{array}
   \right]\,.

Na tej podstawie otrzymujemy 1. część tezy:

.. math::
   
   O_\sigma\,(\boldsymbol{A}\boldsymbol{B})\ =\ 
   O_\sigma
   \left[\begin{array}{c}
         \boldsymbol{A}_1\,\boldsymbol{B} \\ 
         \boldsymbol{A}_2\,\boldsymbol{B} \\
         \dots                            \\
         \boldsymbol{A}_m\,\boldsymbol{B} \\ 
         \end{array}
   \right]\ =
   \left[\begin{array}{c}
         \boldsymbol{A}_{\sigma(1)}\,\boldsymbol{B} \\ 
         \boldsymbol{A}_{\sigma(2)}\,\boldsymbol{B} \\
         \dots                                      \\
         \boldsymbol{A}_{\sigma(m)}\,\boldsymbol{B} \\ 
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \boldsymbol{A}_{\sigma(1)} \\ 
         \boldsymbol{A}_{\sigma(2)} \\
         \dots                      \\
         \boldsymbol{A}_{\sigma(m)} \\ 
         \end{array}
   \right]\boldsymbol{B}\ =\ 
   (O_\sigma\boldsymbol{A})\,\boldsymbol{B}\,.

Wykorzystując poprzedni wynik łatwo wyprowadzamy 2. część tezy twierdzenia:

.. math::

   O_\sigma\,\boldsymbol{A}\ \ =\ \ 
   O_\sigma\,(\boldsymbol{I}_m\,\boldsymbol{A})\ \ =\ \    
   (O_\sigma\,\boldsymbol{I}_m)\,\boldsymbol{A}\ \ =\ \ 
   \boldsymbol{P}_\sigma\,\boldsymbol{A}\,,
   \qquad\sigma\in S_m\,.

:math:`\;`

Iloczyn dwóch macierzy permutacji jest macierzą permutacji. 
Dokładniej formułuje to

.. admonition:: Twierdzenie. :math:`\,`
   
   Jeżeli 
   :math:`\quad P_\rho = O_\rho\,\boldsymbol{I}_m,\ \,P_\sigma = 
   O_\sigma\,\boldsymbol{I}_m,\quad`
   to 
   :math:`\quad\boldsymbol{P}_\rho\,\boldsymbol{P}_\sigma\ =
   \ \boldsymbol{P}_{\sigma\,\circ\,\rho}\,,\qquad\rho,\sigma\in S_m\,.`

**Dowód.**

Zauważmy najpierw, że

.. :math:`\boldsymbol{P}_\rho\,\boldsymbol{P}_\sigma\ =\ 
   (\boldsymbol{P}_\rho\,\boldsymbol{P}_\sigma)\,\boldsymbol{I}_n\ =\ 
   \boldsymbol{P}_\rho\,(\boldsymbol{P}_\sigma\,\boldsymbol{I}_n)\,;`

.. math::
   
   \boldsymbol{P}_\sigma\,\boldsymbol{I}_m\ =\ 
   \boldsymbol{P}_\sigma\,
   \left[\begin{array}{c}
         \boldsymbol{e}_1 \\
         \boldsymbol{e}_2 \\
         \dots            \\
         \boldsymbol{e}_m \\
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \boldsymbol{e}_{\sigma(1)} \\
         \boldsymbol{e}_{\sigma(2)} \\
         \dots                      \\
         \boldsymbol{e}_{\sigma(m)} \\
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \boldsymbol{e}'_1 \\
         \boldsymbol{e}'_2 \\
         \dots             \\
         \boldsymbol{e}'_m \\
         \end{array}
   \right]\,,
   \quad\text{gdzie}\quad
   \boldsymbol{e}'_i\ =\ \boldsymbol{e}_{\sigma(i)}\,,\quad i=1,2,\ldots,m.

A zatem iloczyn dwóch macierzy permutacji można zapisać w postaci

.. math::
   
   \boldsymbol{P}_\rho\,\boldsymbol{P}_\sigma\ =\ 
   (\boldsymbol{P}_\rho\,\boldsymbol{P}_\sigma)\,\boldsymbol{I}_m\ =\ 
   \boldsymbol{P}_\rho\,(\boldsymbol{P}_\sigma\,\boldsymbol{I}_m)\ =\ 
   \boldsymbol{P}_\rho\,
   \left[\begin{array}{c}
         \boldsymbol{e}'_1 \\
         \boldsymbol{e}'_2 \\
         \dots             \\
         \boldsymbol{e}'_m \\
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \boldsymbol{e}'_{\rho(1)} \\
         \boldsymbol{e}'_{\rho(2)} \\
         \dots                     \\
         \boldsymbol{e}'_{\rho(m)} \\
         \end{array}
   \right]\,.

Podstawienie :math:`\ \ i\rightarrow\rho(i)\ \ ` w równaniu 
:math:`\ \ \boldsymbol{e}'_i\ =\ \boldsymbol{e}_{\sigma(i)}\ \ ` daje

.. math::

   \boldsymbol{e}'_{\rho(i)}\ =\ \boldsymbol{e}_{\sigma[\rho(i)]}\ =\ 
   \boldsymbol{e}_{(\sigma\,\circ\,\rho)(i)}\,,\qquad i=1,2,\ldots,m.

Wobec tego

.. math::
   
   \boldsymbol{P}_\rho\,\boldsymbol{P}_\sigma\ =\ 
   \left[\begin{array}{c}
         \boldsymbol{e}'_{\rho(1)} \\
         \boldsymbol{e}'_{\rho(2)} \\
         \dots                     \\
         \boldsymbol{e}'_{\rho(m)} \\
         \end{array}
   \right]\ =\ 
   \left[\begin{array}{c}
         \boldsymbol{e}_{(\sigma\,\circ\,\rho)(1)} \\
         \boldsymbol{e}_{(\sigma\,\circ\,\rho)(2)} \\
         \dots                                     \\
         \boldsymbol{e}_{(\sigma\,\circ\,\rho)(m)} \\
         \end{array}
   \right]\ =\ 
   \boldsymbol{P}_{\sigma\,\circ\,\rho}
   \left[\begin{array}{c}
         \boldsymbol{e}_1 \\
         \boldsymbol{e}_2 \\
         \dots            \\
         \boldsymbol{e}_m \\
         \end{array}
   \right]\ =\ 
   \boldsymbol{P}_{\sigma\,\circ\,\rho}\ \boldsymbol{I}_m\ =\ 
   \boldsymbol{P}_{\sigma\,\circ\,\rho}\,.

   



