Przekształcenie podobieństwa
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. admonition:: Definicja.
   
   Macierze :math:`\,\boldsymbol{A},\,\boldsymbol{B}\in M_n(C)\,`
   są *podobne*, gdy istnieje macierz 
   :math:`\ \boldsymbol{P}\in M_n(C)\ ` taka, że
   
   .. math::
      
      \boldsymbol{B}\ =\ \boldsymbol{P}^{-1} \boldsymbol{A}\,\boldsymbol{P}\,.
   
   Wtedy macierz :math:`\,\boldsymbol{B}\,` jest związana 
   z :math:`\,\boldsymbol{A}\,` *przekształceniem podobieństwa*.

**Twierdzenie 4.** :math:`\ `
Macierze podobne mają ten sam wielomian charakterystyczny.

Mianowicie, jeżeli :math:`\ \boldsymbol{B}\,=\,
\boldsymbol{P}^{-1} \boldsymbol{A}\,\boldsymbol{P},\ \ \ 
\boldsymbol{A},\boldsymbol{B},\boldsymbol{P}\in M_n(C),\ 
\det\boldsymbol{P}\neq 0\,,\ ` to
:math:`\ \ w_{\boldsymbol{B}}(\lambda) = w_{\boldsymbol{A}}(\lambda)\,,\ `
gdzie wielomian charakterystyczny :math:`\ w_{\boldsymbol{X}}(\lambda) = 
\det(\boldsymbol{X}-\lambda\,\boldsymbol{I}_n)\,,\ `
:math:`\boldsymbol{X} = \boldsymbol{A},\,\boldsymbol{B}\,;\ \ 
\boldsymbol{I}_n\ -\ ` macierz jednostkowa stopnia :math:`n`.

**Dowód** opiera się na twierdzeniu Cauchy'ego o wyznaczniku iloczynu macierzy:

.. math::
   
   \begin{array}{rl}
   w_{\boldsymbol{B}}(\lambda) \!\! & 
   =\ \ \det{(\boldsymbol{B}-\lambda\,\boldsymbol{I}_n)}\ = \\ 
   & =\ \ \det{(\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P} - 
   \boldsymbol{P}^{-1}\lambda\,\boldsymbol{I}_n\ \boldsymbol{P})}\ = \\
   & =\ \ \det{[\,\boldsymbol{P}^{-1}
   (\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)\,
   \boldsymbol{P}\,]}\ = \\
   & =\ \ \det{\boldsymbol{P}^{-1}}\cdot\ 
   \det{(\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)}\ \cdot\ 
   \det{\boldsymbol{P}}\ = \\
   & =\ \ (\det{\boldsymbol{P}})^{-1}\cdot\ 
   \det{(\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)}\,\cdot\,
   \det{\boldsymbol{P}}\ = \\
   & =\ \ \det{(\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)}\ \ =\ \ 
   w_{\boldsymbol{A}}(\lambda)\,.
   \end{array}

.. **Wniosek.** Macierze podobne mają takie same wartości własne, 
   o takich samych krotnościach algebraicznych.

**Wniosek.** Macierze podobne mają taki sam zbiór wartości własnych.
Odpowiednie wartości własne mają takie same krotności algebraiczne.

**Twierdzenie 5.** :math:`\\`
Odpowiednie wartości własne macierzy podobnych 
mają tę samą krotność geometryczną.

**Dowód.** :math:`\\`
Niech :math:`\ \lambda\in C\ ` będzie wartością własną macierzy 
:math:`\ \boldsymbol{A}\in M_n(C)\ ` o krotności geometrycznej :math:`\,k`.
Istnieje więc :math:`\,k\,` liniowo niezależnych wektorów własnych
:math:`\ \boldsymbol{x}_i\,` macierzy :math:`\ \boldsymbol{A}\ `
dla tej wartości:

.. math::
   :label: condition
   
   \boldsymbol{A}\,\boldsymbol{x}_i\ =\ \lambda\,\boldsymbol{x}_i\,,
   \quad i=1,2,\ldots,k\,;
   
   \sum_{i=1}^k\,\alpha_i\,\boldsymbol{x}_i\ =\ \boldsymbol{0}
   \quad\Rightarrow\quad\alpha_i=0,\ \ i=1,2,\ldots,k\,.

Niech :math:`\ \boldsymbol{B}\,=\,
\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P},\ `
:math:`\ \boldsymbol{y}_i\,=\,\boldsymbol{P}^{-1}\,\boldsymbol{x}_i,\ \ 
i=1,2,\ldots,k\,,\ ` :math:`\ \boldsymbol{P}\in M_n(C),\,
\det{\boldsymbol{P}}\neq 0.\ ` Wtedy

.. math::

   \boldsymbol{B}\,\boldsymbol{y}_i\ =\ 
   (\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P})\,
   (\boldsymbol{P}^{-1}\boldsymbol{x}_i)\ =\ 
   \boldsymbol{P}^{-1}\boldsymbol{A}\,(\boldsymbol{P}\,
   \boldsymbol{P}^{-1})\ \boldsymbol{x}_i\ =

   \quad =\ 
   \boldsymbol{P}^{-1}(\boldsymbol{A}\,\boldsymbol{x}_i)\ =\ 
   \boldsymbol{P}^{-1}(\lambda\,\boldsymbol{x}_i)\ =\ 
   \lambda\,(\boldsymbol{P}^{-1}\boldsymbol{x}_i)\ =\ 
   \lambda\,\boldsymbol{y}_i\,,

   \sum_{i=1}^k\,\alpha_i\,\boldsymbol{y}_i\ =\ \boldsymbol{0}
   \quad\Leftrightarrow\quad
   \sum_{i=1}^k\,\alpha_i\,(\boldsymbol{P}^{-1}\,\boldsymbol{x}_i)\ =\ 
   \boldsymbol{0}
   \quad\Leftrightarrow\quad
   \boldsymbol{P}^{-1}\,\sum_{i=1}^k\,\alpha_i\,\boldsymbol{x}_i\ =\ 
   \boldsymbol{0}
   \quad\Leftrightarrow\quad
   
   \Leftrightarrow\qquad\sum_{i=1}^k\,\alpha_i\,\boldsymbol{x}_i\ =\ 
   \boldsymbol{0}
   \quad\Rightarrow\quad
   \alpha_i=0,\ \ i=1,2,\ldots,k.

A zatem, w analogii do :eq:`condition`, spełnione są warunki

.. math::
   
   \boldsymbol{B}\,\boldsymbol{y}_i\ =\ \lambda\,\boldsymbol{y}_i\,,
   \quad i=1,2,\ldots,k\,;
   
   \sum_{i=1}^k\,\alpha_i\,\boldsymbol{y}_i\ =\ \boldsymbol{0}
   \quad\Rightarrow\quad\alpha_i=0,\ \ i=1,2,\ldots,k\,,

co oznacza, że :math:`\ \lambda\ ` jest wartością własną macierzy
:math:`\ \boldsymbol{B}\ ` o tej samej 
(co dla macierzy :math:`\,\boldsymbol{A})` krotności geometrycznej 
:math:`\,k`.

**Twierdzenie 6.** :math:`\\`
Dwie macierze podobne mają ten sam wyznacznik i ślad oraz są tego samego rzędu.

Dokładnie, jeżeli :math:`\ \boldsymbol{B}\,=\,
\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P},\ `
:math:`\boldsymbol{A},\boldsymbol{B},\boldsymbol{P}\in M_n(C),
\ \det{\boldsymbol{P}}\neq 0,\ \ ` to

.. math::
   
   \det{\boldsymbol{B}}\,=\det{\boldsymbol{A}},\quad 
   \text{Tr}\,{\boldsymbol{B}}\,=\,\text{Tr}\,{\boldsymbol{A}},\quad
   \text{rz}\,{\boldsymbol{B}}\,=\,\text{rz}\,{\boldsymbol{A}}\,.
   
Pierwsze dwie równości wynikają z udowodnionego twierdzenia o równości 
wielomianów charakterystycznych macierzy podobnych. 
Mianowicie, :math:`\ \det{\boldsymbol{A}},\,\det{\boldsymbol{B}}\ `
są wolnymi wyrazami (współczynnikami przy :math:`\ \lambda^0`), :math:`\ ` 
a :math:`\ \text{Tr}\,\boldsymbol{A},\,\text{Tr}\,\boldsymbol{B}\ -\ ` 
współczynnikami przy potędze :math:`\ \lambda^{(n-1)}\ ` w wielomianach charakterystycznych macierzy :math:`\ \boldsymbol{A},\,\boldsymbol{B}`.
Równość wielomianów implikuje równość współczynników przy tych samych 
potęgach :math:`\ \lambda.`

Związki te można też udowodnić bezpośrednio w oparciu o własności
wyznacznika i śladu macierzy. Na podstawie twierdzenia Cauchy'ego
o wyznaczniku iloczynu macierzy mamy

.. math::
   
   \det{\boldsymbol{B}}\ =\ 
   \det{(\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P})}\ =

   =\ 
   \det{\boldsymbol{P}^{-1}}\cdot\ 
   \det{\boldsymbol{A}}\ \cdot\ 
   \det{\boldsymbol{P}}\ =

   =\ 
   (\det{\boldsymbol{P}})^{-1}\cdot\ 
   \det{\boldsymbol{A}}\ \cdot\ 
   \det{\boldsymbol{P}}\ =\ \det{\boldsymbol{A}}\,,

a przestawiając cyklicznie czynniki pod symbolem śladu otrzymujemy

.. math::
   
   \text{Tr}\,\boldsymbol{B}\ =\ 
   \text{Tr}\,(\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P})\ =\ 
   \text{Tr}\,(\boldsymbol{A}\,\boldsymbol{P}\,\boldsymbol{P}^{-1})\ =\ 
   \text{Tr}\,\boldsymbol{A}\,.

Warunek równości rzędów macierzy podobnych wynika stąd, że pomnożenie danej
macierzy, z lewej bądź z prawej strony, przez nieosobliwą macierz kwadratową
nie zmienia jej rzędu:

.. math::
   \text{rz}\,\boldsymbol{A}\ =\ 
   \text{rz}\,(\boldsymbol{A}\,\boldsymbol{P})\ =\ 
   \text{rz}\,(\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P})\ =\ 
   \text{rz}\,{\boldsymbol{B}}\,.

.. .. math::
   
      \text{rz}\,{\boldsymbol{B}}\,=\,
      \text{rz}\,(\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P})\ =\ 
      \text{rz}\,(\boldsymbol{A}\,\boldsymbol{P})\ =\
      \text{rz}\,\boldsymbol{A}\,.

