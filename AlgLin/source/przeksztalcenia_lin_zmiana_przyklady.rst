
Zmiana bazy w przykładach
-------------------------

**Przykład 0.**

W przestrzeni :math:`\,R^4\,` należy znaleźć macierz przejścia:

* | od bazy kanonicznej :math:`\ \mathcal{E}\,=\,
    (\boldsymbol{e}_1,\,\boldsymbol{e}_2,\,\boldsymbol{e}_3,\,\boldsymbol{e}_4)
    \ =\ \left(\ 
    \left[\begin{array}{c} 1 \\ 0 \\ 0 \\ 0 \end{array}\right]\,,  
    \left[\begin{array}{c} 0 \\ 1 \\ 0 \\ 0 \end{array}\right]\,,
    \left[\begin{array}{c} 0 \\ 0 \\ 1 \\ 0 \end{array}\right]\,,
    \left[\begin{array}{c} 0 \\ 0 \\ 0 \\ 1 \end{array}\right]
    \ \right)`
  |
  | do bazy :math:`\ \mathcal{F}\,=\,
    (\boldsymbol{f}_1,\,\boldsymbol{f}_2,\,\boldsymbol{f}_3,\,\boldsymbol{f}_4)
    \ =\ \left(\ 
    \left[\begin{array}{r}  1 \\  2 \\ -1 \\ 0 \end{array}\right]\,,  
    \left[\begin{array}{r}  1 \\ -1 \\  1 \\ 1 \end{array}\right]\,,
    \left[\begin{array}{r} -1 \\  2 \\  1 \\ 1 \end{array}\right]\,,
    \left[\begin{array}{r} -1 \\ -1 \\  0 \\ 1 \end{array}\right]
    \ \right)\,.`

* | od bazy :math:`\,\mathcal{F}\,=\,
    (\boldsymbol{f}_1,\,\boldsymbol{f}_2,\,\boldsymbol{f}_3,\,\boldsymbol{f}_4)`
  | do bazy :math:`\,\mathcal{G}\,=\,
    (\boldsymbol{g}_1,\,\boldsymbol{g}_2,\,\boldsymbol{g}_3,\,\boldsymbol{g}_4)
    \,=\,\left(\ 
    \left[\begin{array}{r}  2 \\ 1 \\ 0 \\ 1 \end{array}\right],  
    \left[\begin{array}{r}  0 \\ 1 \\ 2 \\ 2 \end{array}\right],
    \left[\begin{array}{r} -2 \\ 1 \\ 1 \\ 2 \end{array}\right],
    \left[\begin{array}{r}  1 \\ 3 \\ 1 \\ 2 \end{array}\right]
    \ \right).`

**Rozwiązanie.**

Wprowadzamy macierz :math:`\,\boldsymbol{F},\ ` złożoną kolumnowo 
z wektorów bazy :math:`\,\mathcal{F}:`

.. math::
   
   \boldsymbol{F}\ :\,=\ [\,\boldsymbol{f}_1\,|\,\boldsymbol{f}_2\,|\,
   \boldsymbol{f}_3\,|\,\boldsymbol{f}_4\,]\ =\ 
   \left[\begin{array}{rrrr}
          1 &  1 & -1 & -1 \\
          2 & -1 &  2 & -1 \\
         -1 &  1 &  1 &  0 \\
          0 &  1 &  1 &  1 \end{array}\right]\,.

Kolumny macierzy przejścia od bazy :math:`\,\mathcal{E}\,` do bazy 
:math:`\,\mathcal{F}\,` składają się ze współrzędnych wektorów bazy 
:math:`\ \mathcal{F}\ \,` w bazie :math:`\ \mathcal{E}:`

.. math::
   
   \boldsymbol{S}_{\mathcal{E}\rightarrow\mathcal{F}}\ =\ 
   [\,I_{\mathcal{E}}(\boldsymbol{f}_1)\,|\,
      I_{\mathcal{E}}(\boldsymbol{f}_2)\,|\,
      I_{\mathcal{E}}(\boldsymbol{f}_3)\,|\,
      I_{\mathcal{E}}(\boldsymbol{f}_4)\,]\,.

Ale w przestrzeni :math:`\,R^4\ ` każdy wektor jest 
kolumną swoich współrzędnych w bazie kanonicznej:

.. math::
   
   I_{\mathcal{E}}(\boldsymbol{x})\ =
   \ \boldsymbol{x}\,,\qquad \boldsymbol{x}\in R^4\,.

W takim razie szukana macierz przejścia jest dana po prostu przez

.. math::
   :label: S_EF
   
   \blacktriangleright\quad
   \boldsymbol{S}_{\mathcal{E}\rightarrow\mathcal{F}}\ =\   
   [\,\boldsymbol{f}_1\,|\,\boldsymbol{f}_2\,|\,
   \boldsymbol{f}_3\,|\,\boldsymbol{f}_4\,]\,=\,
   \boldsymbol{F}\ =\ 
   \left[\begin{array}{rrrr}
          1 &  1 & -1 & -1 \\
          2 & -1 &  2 & -1 \\
         -1 &  1 &  1 &  0 \\
          0 &  1 &  1 &  1 \\
   \end{array}\right]\,.

**Wniosek** (uogólnienie).

W przestrzeni :math:`\,K^n\ ` macierz przejścia od bazy kanonicznej 
:math:`\ \mathcal{E}\ ` do bazy :math:`\,\mathcal{B}\ ` jest macierzą 
:math:`\,\boldsymbol{B},\ ` otrzymaną przez zestawienie wektorów bazy 
:math:`\,\mathcal{B}\ ` zapisanych w postaci kolumnowej.

.. [\,\boldsymbol{f}_1\,|\,\boldsymbol{f}_2\,|\,
   \boldsymbol{f}_3\,|\,\boldsymbol{f}_4\,]\,=\,
   [\,\boldsymbol{g}_1\,|\,\boldsymbol{g}_2\,|\,
   \boldsymbol{g}_3\,|\,\boldsymbol{g}_4\,]\,=\,
   \boldsymbol{G}\ =\ 
   \left[\begin{array}{rrrr}
          2 & 0 & -2 & 1 \\
          1 & 1 &  1 & 3 \\
          0 & 2 &  1 & 1 \\
          1 & 2 &  2 & 2 \\
   \end{array}\right]\,.

Przy opisie przejścia :math:`\ \mathcal{F}\rightarrow\mathcal{G}\ ` 
przydatna będzie, oprócz macierzy :math:`\,\boldsymbol{F},\ ` również macierz

.. math::
   
   \boldsymbol{G}\ :\,=\ 
   [\,\boldsymbol{g}_1\,|\,\boldsymbol{g}_2\,|\,
   \boldsymbol{g}_3\,|\,\boldsymbol{g}_4\,]\ =\ 
   \left[\begin{array}{rrrr}
          2 & 0 & -2 & 1 \\
          1 & 1 &  1 & 3 \\
          0 & 2 &  1 & 1 \\
          1 & 2 &  2 & 2 \\
   \end{array}\right]\,.

Z definicji (patrz wzór :eq:`base_0`), :math:`\,j`-ta kolumna macierzy 
:math:`\,\boldsymbol{S}_{\mathcal{F}\rightarrow\mathcal{G}}\equiv\boldsymbol{S}=
[\,s_{ij}\,]_{4\times 4}(R)\ `
przejścia od bazy :math:`\ \mathcal{F}\ ` do bazy :math:`\ \mathcal{G}\ ` jest 
kolumną współrzędnych (w bazie :math:`\ \mathcal{F}`) :math:`\,j`-tego wektora
bazy :math:`\ \mathcal{G}:`

.. math::
   :label: S_4
   
   \boldsymbol{g}_j\ =\ \sum_{i\,=\,1}^4\ s_{ij}\:\boldsymbol{f}_i\,,
   \qquad j=1,2,3,4.

Relację :eq:`S_4` można zinterpretować w duchu kolumnowej reguły mnożenia 
macierzowego: :math:`\,j`-ta kolumna macierzy :math:`\,\boldsymbol{G}\ ` jest 
kombinacją liniową kolumn macierzy :math:`\,\boldsymbol{F},\ ` o współczynnikach 
z :math:`\,j`-tej kolumny macierzy :math:`\,\boldsymbol{S},\ \ j=1,2,3,4.\ ` 
Oznacza to, że 

.. math::
   
   \boldsymbol{G}\ =\ \boldsymbol{F}\boldsymbol{S}\,.

Macierz :math:`\,\boldsymbol{F},\ ` złożona z liniowo niezależnych kolumn
:math:`\ \boldsymbol{f}_1\,,\,\boldsymbol{f}_2\,,\,
\boldsymbol{f}_3\,,\,\boldsymbol{f}_4\,,\ ` jest nieosobliwa: 
:math:`\ \det\,\boldsymbol{F}\neq 0,\ \,` a więc odwracalna. 
Stąd szukana macierz przejścia

.. math::
   :label: S_FG

   \blacktriangleright\quad   
   \boldsymbol{S}_{\mathcal{F}\rightarrow\mathcal{G}}\ =\ 
   \boldsymbol{F}^{-1}\,\boldsymbol{G}\,.

**Wariant rozwiązania.**

Niech :math:`\ T\in\text{Aut}(R^4)\ ` będzie automorfizmem przejścia
od bazy :math:`\ \mathcal{F}\ ` do bazy :math:`\ \mathcal{G}.\ ` Wtedy
szukana macierz przejścia jest macierzą automorfizmu :math:`\,T\,` w bazie 
:math:`\,\mathcal{F}:\ \boldsymbol{S}_{\mathcal{F}\rightarrow\mathcal{G}}
\equiv\boldsymbol{S}=M_{\mathcal{F}}(T).\ ` Ponadto 

.. math::
   
   \boldsymbol{g}_j\,=\,T\,\boldsymbol{f}_j\,,
   \qquad\text{skąd}\qquad
   \boldsymbol{g}_j\,=\,\boldsymbol{T}\cdot\boldsymbol{f}_j\,,
   \qquad j=1,2,3,4\,,

gdzie :math:`\ \,\boldsymbol{T}:\,=M_{\mathcal{E}}(T)\ \,` 
jest macierzą automorfizmu :math:`\,T\ ` w bazie kanonicznej. 
Na podstawie kolumnowej reguły mnożenia macierzowego stwierdzamy, 
że z równości wektorowych

.. math::
   
   \boldsymbol{g}_1\,=\,\boldsymbol{T}\cdot\boldsymbol{f}_1\,,\quad
   \boldsymbol{g}_2\,=\,\boldsymbol{T}\cdot\boldsymbol{f}_2\,,\quad
   \boldsymbol{g}_3\,=\,\boldsymbol{T}\cdot\boldsymbol{f}_3\,,\quad
   \boldsymbol{g}_4\,=\,\boldsymbol{T}\cdot\boldsymbol{f}_4\,,

wynika równość macierzowa

.. math::
   
   [\,\boldsymbol{g}_1\,|\,\boldsymbol{g}_2\,|\,
   \boldsymbol{g}_3\,|\,\boldsymbol{g}_4\,]\ =\ 
   \boldsymbol{T}\,\cdot\,
   [\,\boldsymbol{f}_1\,|\,\boldsymbol{f}_2\,|\,
   \boldsymbol{f}_3\,|\,\boldsymbol{f}_4\,]\,,
   \qquad\text{czyli}\qquad
   \boldsymbol{G}\ =\ \boldsymbol{T}\boldsymbol{F}\,.

Stąd :math:`\ \,\boldsymbol{T}\equiv M_{\mathcal{E}}(T)\ =
\ \boldsymbol{G}\boldsymbol{F}^{-1}.\ \,`
Potrzebną macierz :math:`\,\boldsymbol{S}\equiv M_{\mathcal{F}}(T)\ ` można 
wyliczyć ze wzoru 

.. math::
   
   M_{\mathcal{F}}(T)\ =
   \ \boldsymbol{S}_{\mathcal{E}\rightarrow\mathcal{F}}^{-1}\,\cdot\, 
   M_{\mathcal{E}}(T)\,\cdot\,
   \boldsymbol{S}_{\mathcal{E}\rightarrow\mathcal{F}}\,.

Ale, jak zostało wcześniej pokazane (równanie :eq:`S_EF`):
:math:`\ \,\boldsymbol{S}_{\mathcal{E}\rightarrow\mathcal{F}}=
\boldsymbol{F},\ \,` wobec czego

.. math::
   
   \boldsymbol{S}_{\mathcal{F}\rightarrow\mathcal{G}}\ =\ 
   \boldsymbol{F}^{-1}\,(\boldsymbol{G}\boldsymbol{F}^{-1})\,\boldsymbol{F}\ =\ 
   \boldsymbol{F}^{-1}\,\boldsymbol{G}\,.

Dla sprawdzenia poprawności rozwiązania :eq:`S_FG` rozważmy szczególny 
przypadek, gdy baza :math:`\ \mathcal{F}\ \,` jest bazą kanoniczną: 
:math:`\ \mathcal{F}=\mathcal{E}.\ \,` Wtedy :math:`\ \boldsymbol{F}=
\boldsymbol{I}_4\ \ ` i :math:`\,` dochodzimy do wzoru 
:math:`\ \boldsymbol{S}_{\mathcal{E}\rightarrow\mathcal{G}}\ =
\ \boldsymbol{G},\ ` zgodnego (przy innym oznaczeniu) z poprzednim wynikiem 
:eq:`S_EF`.

.. .. math::
   
      \boldsymbol{S}_{\mathcal{E}\rightarrow\mathcal{G}}\ =\ \boldsymbol{G}\,,

Przechodząc do rachunków, trzeba obliczyć iloczyn macierzowy

.. math::
   
   \boldsymbol{F}^{-1}\,\boldsymbol{G}\ =\ 
      \left[\begin{array}{rrrr}
          1 &  1 & -1 & -1 \\
          2 & -1 &  2 & -1 \\
         -1 &  1 &  1 &  0 \\
          0 &  1 &  1 &  1 \\
      \end{array}\right]^{-1}
   \left[\begin{array}{rrrr}
          2 & 0 & -2 & 1 \\
          1 & 1 &  1 & 3 \\
          0 & 2 &  1 & 1 \\
          1 & 2 &  2 & 2 \\
   \end{array}\right]\,.

Komputerowe obliczenia przedstawiają się następująco:

.. code-block:: python

   sage: F = matrix(QQ,[[ 1, 1,-1,-1],
                        [ 2,-1, 2,-1],
                        [-1, 1, 1, 0],
                        [ 0, 1, 1, 1]])
   
   sage: G = matrix(QQ,[[ 2, 0,-2, 1],
                        [ 1, 1, 1, 3],
                        [ 0, 2, 1, 1],
                        [ 1, 2, 2, 2]])
   
   sage: F.I*G
   
   [1 0 0 1]
   [1 1 0 1]
   [0 1 1 1]
   [0 0 1 0]

**Przykład 1.**

W 4-wymiarowej przestrzeni :math:`\,V(R)\ ` wektor :math:`\,v\ ` ma w bazie
:math:`\,\mathcal{B}=(v_1,\,v_2,\,v_3,\,v_4)\ ` współrzędne 
:math:`\ 2,\ -3,\ 0,\ 4.\ ` Jakie współrzędne ma ten wektor w bazie 
:math:`\,\mathcal{B}'=(v_1',\,v_2',\,v_3',\,v_4'),\ ` gdzie

.. math::
   
   v_1'\,=\,-\ v_1\,,\quad v_2'\,=\,2\,v_1-\,v_3\,,\quad 
   v_3'\,=\,v_1+\,v_2-\,v_3-\,2\,v_4\,,\quad v_4'\,=\,v_2-\,v_3+\,v_4\quad ?

**Rozwiązanie.** :math:`\,` 
Punktem wyjścia jest Reguła 1. przedstawiająca transformację współrzędnych:

.. math::
   
   I_{\mathcal{B}'}(v)\ \ =\ \ \boldsymbol{S}^{-1}\,\cdot\,I_{\mathcal{B}}(v)\,.

Macierz przejścia :math:`\,\boldsymbol{S}\ ` wyznaczymy z relacji
pomiędzy wektorami starej i nowej bazy:

.. math::
   :nowrap:

   \begin{alignat*}{5}
   v_1' & {\ } = {\ } & -\ v_1 &             &     &             &     &                      \\
   v_2' & {\ } = {\ } & 2\,v_1 &             &     & {\,} - {\;} & v_3 &                      \\
   v_3' & {\ } = {\ } &    v_1 & {\,} + {\;} & v_2 & {\,} - {\;} & v_3 & {\,} - {\;} & 2\,v_4 \\
   v_4' & {\ } = {\ } &        &             & v_2 & {\,} - {\;} & v_3 & {\,} + {\;} &    v_4 \\
   \end{alignat*}

Mianowicie, na podstawie Wniosku 1. po definicji macierzy przejścia 
(równanie :eq:`S_col`) : 

.. math::
 
   \boldsymbol{S}
   \ \ =\ \ 
   \left[\begin{array}{rrrr} -1 &  2 &  1 &  0 \\
                              0 &  0 &  1 &  1 \\
                              0 & -1 & -1 & -1 \\
                              0 &  0 & -2 &  1 \\
   \end{array}\right]\,.

Z treści zadania:
:math:`\quad I_{\mathcal{B}}(v)\ =\ 
\left[\begin{array}{r} 2 \\ -3 \\ 0 \\ 4 \end{array}\right]\,;\quad`
przy oznaczeniu
:math:`\quad I_{\mathcal{B}'}(v)\ =\ 
\left[\begin{array}{r} a_1' \\ a_2' \\ a_3' \\ a_4' \end{array}\right]\quad`
mamy

.. math::
   :label: ex_1
   
   \left[\begin{array}{r} a_1' \\ a_2' \\ a_3' \\ a_4' \end{array}\right]
   \quad=\quad
   \left[\begin{array}{rrrr} -1 &  2 &  1 &  0 \\
                              0 &  0 &  1 &  1 \\
                              0 & -1 & -1 & -1 \\
                              0 &  0 & -2 &  1 \\
   \end{array}\right]^{-1}
   \cdot\quad
   \left[\begin{array}{r} 2 \\ -3 \\ 0 \\ 4 \end{array}\right]\,.

Dalsze obliczenia można wykonać dwoma sposobami. :math:`\\`
 
**Sposób 1.** :math:`\,` Bezpośrednie wyliczenie macierzy odwrotnej do 
:math:`\,\boldsymbol{S}.`

Macierz :math:`\,\boldsymbol{S}^{-1}\ ` można wyliczyć odręcznie, 
korzystając ze wzoru

.. math::
   
   (\boldsymbol{S}^{-1})_{ij}\ \,=\ \ \frac{1}{\det\boldsymbol{S}}\ \ S_{ji}\,,
   \qquad i,j=1,2,\dots,n\,,

gdzie :math:`\,S_{ij}\,` jest dopełnieniem algebraicznym elementu 
:math:`\,s_{ij}\,` macierzy :math:`\,\boldsymbol{S},\ \\`
albo komputerowo, korzystając z funkcji wbudowanych do pakietu Sage. :math:`\\`

W drugim przypadku, po wyliczeniu macierzy :math:`\,\boldsymbol{S}^{-1}\ `
można od razu wykonać mnożenie macierzowe po prawej stronie równania :eq:`ex_1`,
co daje wynik w postaci kolumny współrzędnych wektora :math:`\,v\,` 
w bazie :math:`\,\mathcal{B}'.`

.. code-block:: python
   
   sage: S = matrix(QQ,[[-1, 2, 1, 0],
                        [ 0, 0, 1, 1],
                        [ 0,-1,-1,-1],
                        [ 0, 0,-2, 1]])
   
   # Macierz odwrotna do S:
   sage: S_1 = S.I
   
   # Kolumna współrzędnych w bazie B:
   sage: I_B = vector(QQ,[2,-3,0,4]).column()
   
   sage: table([[S_1,'*',I_B,'=',S_1*I_B]])

.. math::
   :label: calc_comp
   
   \textstyle
   \left(\begin{array}{rrrr}
   -1 & -\frac{5}{3} & -2 & -\frac{1}{3} \\
    0 & -1           & -1 & 0            \\
    0 & \frac{1}{3}  &  0 & -\frac{1}{3} \\
    0 & \frac{2}{3}  &  0 & \frac{1}{3}
   \end{array}\right)
   \quad\ast\quad
   \left(\begin{array}{r} 2 \\ -3 \\ 0 \\ 4 \end{array}\right)
   \quad=\quad
   \left(\begin{array}{r} 
       \frac{5}{3} \\ 3 \\ -\frac{7}{3} \\ -\frac{2}{3} 
   \end{array}\right)

Dla przejrzystego zapisu liczbowych elementów macierzy i wektorów obliczenia 
zostały wykonane w ciele :math:`\,Q\,` liczb wymiernych.

**Odpowiedź.** :math:`\,` 
Współrzędne wektora :math:`\,v\ ` w bazie :math:`\,\mathcal{B}'\ ` wynoszą:
:math:`\textstyle\quad\frac{5}{3}\,,\ \ \ 3\,,\ \ -\ 
\frac{7}{3}\,,\ \ -\ \frac{2}{3}\,. \\`

**Sposób 2.** :math:`\,` 
Zamiast bezpośredniego wyliczania macierzy :math:`\,\boldsymbol{S}^{-1},\ ` 
odwrócimy relacje

.. math::
   :nowrap:

   \begin{alignat*}{6}
   v_1' & {\ } = {\ } & Tv_1 & {\ \,} = {\ \,} & -\ v_1 &             &     &             &     &                      \\
   v_2' & {\ } = {\ } & Tv_2 & {\ \,} = {\ \,} & 2\ v_1 &             &     & {\,} - {\;} & v_3 &                      \\
   v_3' & {\ } = {\ } & Tv_3 & {\ \,} = {\ \,} &    v_1 & {\,} + {\;} & v_2 & {\,} - {\;} & v_3 & {\,} - {\;} & 2\ v_4 \\
   v_4' & {\ } = {\ } & Tv_4 & {\ \,} = {\ \,} &        &             & v_2 & {\,} - {\;} & v_3 & {\,} + {\;} &    v_4 \\
   \end{alignat*}

Po prostych elementarnych rachunkach otrzymujemy wzory 

.. math::
   :nowrap:

   \begin{alignat*}{6}
   v_1 & {\ } = {\ } &
   T^{-1}\,v_1' &
   {\ \,} = {\ \,} & -\ v_1' & & & & & \\
   v_2 & {\ } = {\ } & T^{-1}\,v_2' & {\ \,} = {\ \,} & 
   -\ \textstyle\frac{5}{3}\ v_1' & {\,} - {\;} & v_2' & {\,} + {\;} & 
   \textstyle\frac{1}{3}\ v_3' & {\,} + {\;} & \textstyle\frac{2}{3}\ v_4' \\
   v_3 & {\ } = {\ } & T^{-1}\,v_3' & {\ \,} = {\ \,} & -\ 2\ v_1' & 
   {\,} - {\;} & v_2' & & & \\
   v_4 & {\ } = {\ } & T^{-1}\,v_4' & {\ \,} = {\ \,} &
   -\ \textstyle\frac{1}{3}\ v_1' & & & {\,} - {\;} & 
   \textstyle\frac{1}{3}\ v_3' & {\,} + {\;} & \textstyle\frac{1}{3}\ v_4'
   \end{alignat*}

na podstawie których można wypisać macierz automorfizmu :math:`\,T^{-1}\ `
w bazie :math:`\,\mathcal{B}':`

.. math::
   :label: MB_prim_T_1
   
   M_{\mathcal{B}'}(T^{-1})\ \ =\ \ \textstyle
   \left[\begin{array}{rrrr}
         -1 & -\frac{5}{3} & -2 & -\frac{1}{3} \\
          0 & -1           & -1 &   0          \\ 
          0 &  \frac{1}{3} &  0 & -\frac{1}{3} \\
          0 &  \frac{2}{3} &  0 &  \frac{1}{3} \\
         \end{array}\right]\,.

Nas interesuje raczej macierz 
:math:`\ \boldsymbol{S}^{-1}=[\,M_{\mathcal{B}}(T)\,]^{-1}.\ \,`
Ale, zgodnie z Regułą 2.:

.. math::
   
   M_{\mathcal{B}'}(T^{-1})\ \,=\ \,
   \boldsymbol{S}^{-1}\cdot M_{\mathcal{B}}(T^{-1})\cdot\boldsymbol{S}\ \,=\ \,
   \boldsymbol{S}^{-1}\cdot [\,M_{\mathcal{B}}(T)\,]^{-1}\cdot
   \boldsymbol{S}\ \,=\ \,
   \boldsymbol{S}^{-1}\cdot\boldsymbol{S}^{-1}\cdot\boldsymbol{S}\ \,=
   \ \,\boldsymbol{S}^{-1}\,.

Równanie :eq:`MB_prim_T_1` daje więc szukaną macierz 
:math:`\ \boldsymbol{S}^{-1},\ `
co prowadzi dalej do wyniku :eq:`calc_comp`.

.. a rozwiązanie przykładu daje wzór :eq:`calc_comp`.

**Wariant rozwiązania.** :math:`\,`

Związek :eq:`trans_coord` pomiędzy współrzędnymi wektora w nowej i starej bazie, 
zapisany w postaci

.. math::
   
   \boldsymbol{S}\cdot I_{\mathcal{B}'}(v)\ =\  I_{\mathcal{B}}(v)
   \qquad\text{czyli}\qquad
   \left[\begin{array}{rrrr} 
   -1 &  2 &  1 &  0 \\
    0 &  0 &  1 &  1 \\
    0 & -1 & -1 & -1 \\
    0 &  0 & -2 &  1 \\
   \end{array}\right]
   \left[\begin{array}{r} a_1' \\ a_2' \\ a_3' \\ a_4' \end{array}\right]\ =\ 
   \left[\begin{array}{r} 2 \\ -3 \\ 0 \\ 4 \end{array}\right]

przedstawia kramerowski układ równań

.. math::
   :nowrap:
   
   \begin{alignat*}{5}
   -\ a_1' & {\,} + {\,} & 2\,a_2' & {\,} + {\,} &    a_3' &             &      & {\;} = {} &  2 \\
           &             &         &             &    a_3' & {\,} + {\,} & a_4' & {\;} = {} & -3 \\
           & {\,} - {\,} &    a_2' & {\,} - {\,} &    a_3' & {\,} - {\,} & a_4' & {\;} = {} &  0 \\
           &             &         & {\,} - {\,} & 2\,a_3' & {\,} + {\,} & a_4' & {\;} = {} &  4 \\
   \end{alignat*}

który można rozwiązać odręcznie albo komputerowo z użyciem funkcji pakietu Sage:

.. code-block:: python
   
   sage: S = matrix(QQ,[[-1, 2, 1, 0],
                        [ 0, 0, 1, 1],
                        [ 0,-1,-1,-1],
                        [ 0, 0,-2, 1]])

   sage: I_B = vector(QQ,[2,-3,0,4]) # wektor wolnych wyrazów
   
   sage: S \ I_B

   (5/3, 3, -7/3, -2/3)

:math:`\;`

**Przykład 2.**

W bazie :math:`\,\mathcal{B}=(v_1,\,v_2,\,v_3)\ ` przestrzeni wektorowej 
:math:`\,V(R)\ ` operator :math:`\,F\in\text{End}(V)\ ` ma macierz

.. math::
   
   \boldsymbol{F}\ =\ 
   \left[\begin{array}{rrr}
         3 & -2 & -1 \\
         2 &  1 & -3 \\
         1 &  3 &  2 \end{array}\right]\,.

Należy podać macierz :math:`\,\boldsymbol{F}'\ ` tego operatora w bazie
:math:`\,\mathcal{B}'=(v_1',\,v_2',\,v_3'):\,=(v_3,\,v_2,\,v_1).`

**Rozwiązanie.**

**Sposób 1.** (bezpośredni) :math:`\,` 

Z definicji macierzy :math:`\,\boldsymbol{F}=[\,f_{ij}\,]_{3\times 3}\ ` oraz
:math:`\,\boldsymbol{F}'=[\,f_{ij}'\,]_{3\times 3}\ ` operatora :math:`\,F\ `
w bazach :math:`\,\mathcal{B}\ ` oraz :math:`\,\mathcal{B}':`

.. math::
   
   Fv_j\,=\ f_{1j}\,v_1+\,f_{2j}\,v_2+\,f_{3j}\,v_3\,,
   \qquad
   Fv_j'\,=\ f_{1j}'\,v_1'+\,f_{2j}'\,v_2'+\,f_{3j}'\,v_3'\,,
   \qquad j=1,2,3,

oraz z zależności :math:`\ v_1'=v_3,\ v_2'=v_2,\ v_3'=v_1\ ` wynikają związki

.. math::
   
   \begin{array}{l}
   Fv_1\,=\quad 3\,v_1+\,2\,v_2+\,1\,v_3 \\
   Fv_2\,=\  -2\,v_1+\,1\,v_2+\,3\,v_3 \\
   Fv_3\,=\  -1\,v_1-\,3\,v_2+\,2\,v_3\,,
   \end{array}
   \qquad\qquad
   \begin{array}{l}
   Fv_1'\,=\ 2\,v_1'-\,3\,v_2'-\,1\,v_3' \\
   Fv_2'\,=\ 3\,v_1'+\,1\,v_2'-\,2\,v_3' \\
   Fv_3'\,=\ 1\,v_1'+\,2\,v_2'+\,3\,v_3'\,.
   \end{array}

Z drugiego układu równości odczytujemy:

.. math::
   
   \boldsymbol{F}'\ =\ 
   \left[\begin{array}{rrr}
          2 &  3 & 1 \\
         -3 &  1 & 2 \\
         -1 & -2 & 3 \end{array}\right]\,.

**Sposób 2.** (standardowy)

Stosujemy Regułę 2. transformacji macierzy operatora liniowego 
(wzór :eq:`F_prim`):

.. math::
   :label: F_prim_bis
   
   \boldsymbol{F}'\ =\ \boldsymbol{S}^{-1}\,\boldsymbol{F}\ \boldsymbol{S}\,,

gdzie :math:`\,\boldsymbol{S}\ ` jest macierzą przejścia 
od bazy :math:`\,\mathcal{B}=(v_1,\,v_2,\,v_3)\ `
do bazy :math:`\,\mathcal{B}'=(v_3,\,v_2,\,v_1).`

Zapisując związki pomiędzy wektorami nowej i starej bazy

.. math::
   
   \begin{array}{l}
   v_1'\,=\ 0\,v_1+\,0\,v_2+\,1\,v_3 \\
   v_2'\,=\ 0\,v_1+\,1\,v_2+\,0\,v_3 \\
   v_3'\,=\ 1\,v_1+\,0\,v_2+\,0\,v_3
   \end{array}
   \qquad\text{otrzymujemy}\qquad
   \boldsymbol{S}\ =\ 
   \left[\begin{array}{ccc} 0 & 0 & 1 \\ 
                            0 & 1 & 0 \\ 
                            1 & 0 & 0 \end{array}\right]\,.

Zamiast wyliczać bezpośrednio macierz :math:`\,\boldsymbol{S}^{-1}\ `
zauważmy, że automorfizm przejścia :math:`\,T,\ ` który przekształca 
wektory bazy :math:`\,\mathcal{B}\ ` w odpowiednie 
wektory bazy :math:`\,\mathcal{B}':\ \ Tv_i=v_i',\ \ i=1,2,3,\ \ `
spełnia warunek :math:`\,T^2=I,\ ` gdzie :math:`\,I\ ` jest przekształceniem 
identycznościowym:

.. math::
   
   \begin{array}{l} Tv_1=v_3 \\ Tv_2=v_2 \\ Tv_3=v_1 \end{array}
   \qquad\Rightarrow\qquad
   \begin{array}{l}
    T^2\,v_1=\,Tv_3=\,v_1=\,I\,v_1 \\ 
    T^2\,v_2=\,Tv_2=\,v_2=\,I\,v_2 \\ 
    T^2\,v_3=\,Tv_1=\,v_3=\,I\,v_3
   \end{array}

Z multiplikatywności macierzowej reprezentacji operatorów liniowych wynika, 
że analogiczną własność ma macierz przejścia: 
:math:`\ \boldsymbol{S}^2\ =\ \boldsymbol{I}_3,\ \,` 
skąd :math:`\ \boldsymbol{S}^{-1}=\,\boldsymbol{S}.`

Wyznaczone macierze podstawiamy do wzoru :eq:`F_prim_bis`. :math:`\\`

.. code-block:: python

   sage: F = matrix(QQ,[[3, -2, -1],
                        [2,  1, -3],
                        [1,  3,  2]])

   sage: S = matrix(QQ,[[0,  0,  1],
                        [0,  1,  0],
                        [1,  0,  0]])

   sage: F_1 = S*F*S
   
   sage: table([[S, '*', F, '*', S, '=', F_1]])

.. math::
   
   \left(\begin{array}{ccc} 0 & 0 & 1 \\ 
                            0 & 1 & 0 \\ 
                            1 & 0 & 0 \end{array}\right)
   \ \ast\ 
   \left(\begin{array}{rrr} 3 & -2 & -1 \\
                            2 &  1 & -3 \\
                            1 &  3 &  2 \end{array}\right)
   \ \ast\ 
   \left(\begin{array}{ccc} 0 & 0 & 1 \\ 
                            0 & 1 & 0 \\ 
                            1 & 0 & 0 \end{array}\right)
   \ =\ 
   \left(\begin{array}{rrr}
          2 &  3 & 1 \\
         -3 &  1 & 2 \\
         -1 & -2 & 3 \end{array}\right)\,.
   
:math:`\\`



