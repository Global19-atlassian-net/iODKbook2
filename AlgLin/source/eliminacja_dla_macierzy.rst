.. -*- coding: utf-8 -*-

Metoda eliminacji w ujęciu macierzowym
--------------------------------------

Omówiona wcześniej metoda eliminacji wykorzystuje przekształcenia elementarne 
dla doprowadzenia układu równań liniowych do postaci schodkowej. 

Ten sam efekt można osiągnąć, zastępując operacje elementarne na równaniach 
odpowiednimi operacjami na wierszach macierzy rozszerzonej, 
reprezentującej układ równań.

Macierz rozszerzona układu równań
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Dla układu :math:`\,m\,` równań o :math:`\,n\,` niewiadomych:

.. math::
   :label: 01

   \begin{array}{c}
   a_{11}\,x_1\; + \ \,a_{12}\,x_2\; + \ \,\ldots\  + \ \;a_{1n}\,x_n \ \, =
   \ \ b_1      \\
   a_{21}\,x_1\; + \ \,a_{22}\,x_2\; + \ \,\ldots\  + \ \;a_{2n}\,x_n \ \, =
   \ \ b_2      \\
   \quad\,\ldots\qquad\quad\ldots\qquad\ \,\ldots\qquad\ \ \ldots\qquad
   \ \ \,\ldots \\
   a_{m1}\,x_1\; + \ \,a_{m2}\,x_2\; + \ \,\ldots\  + \ \;a_{mn}\,x_n \ \, =
   \ \ b_m      \\
   \end{array}

gdzie współczynniki :math:`\,a_{ij}\,` 
oraz wolne wyrazy :math:`\,b_i\ \ (i=1,2,\ldots,m;\ j=1,2,\ldots,n)\,`
należą do pewnego ciała :math:`\,K,\,`
definiujemy :math:`\,` *macierz współczynników* :math:`\,\boldsymbol{A},\ \ `
*kolumnę wolnych wyrazów* :math:`\,\boldsymbol{b}\ \,` i :math:`\ `
*kolumnę niewiadomych* :math:`\,\boldsymbol{x}:`

.. math::

   \boldsymbol{A}\  =\  \left[\;\begin{array}{cccc}
                           a_{11} & a_{12} & \ldots & a_{1n} \\
                           a_{21} & a_{22} & \ldots & a_{2n} \\
                           \ldots & \ldots & \ldots & \ldots \\
                           a_{m1} & a_{m2} & \ldots & a_{mn} \\
                        \end{array}\right]\,,\qquad
   \boldsymbol{b}\,=\,\left[\begin{array}{c} 
                      b_{1} \\ b_{2} \\ \ldots \\ b_{m} 
                      \end{array}\right]\,,\qquad
   \boldsymbol{x}\,=\,\left[\begin{array}{c} 
                      x_{1} \\ x_{2} \\ \ldots \\ x_{n} 
                      \end{array}\right]\,.

Układ :eq:`01` można wtedy zapisać zwięźle jako

.. math::
   :label: 02

   \boldsymbol{A}\,\boldsymbol{x}\,=\,\boldsymbol{b}.

Gdy wszystkie wolne wyrazy znikają: :math:`\ \boldsymbol{b} = \boldsymbol{0},\ ` 
układ równań jest *jednorodny*. Jednorodny układ równań

.. math::

   \boldsymbol{A}\,\boldsymbol{x}\ =\ \boldsymbol{0}

jest :math:`\,` *stowarzyszony* :math:`\,` z niejednorodnym układem :eq:`02`.

Dwa układy równań są :math:`\,` *równoważne*, :math:`\,` 
gdy mają ten sam zbiór rozwiązań. :math:`\\`

Dla układu :eq:`01` definiujemy również :math:`\,` 
*macierz rozszerzoną* :math:`\ \boldsymbol{B}\,:`

.. math::

   \boldsymbol{B}\ \,:\,=\ \,[\,\boldsymbol{A}\,|\,\boldsymbol{b}\;]\ \,
                     =\ \,\left[\begin{array}{ccccc}
                                a_{11} & a_{12} & \ldots & a_{1n} & b_1    \\
                                a_{21} & a_{22} & \ldots & a_{2n} & b_2    \\
                                \ldots & \ldots & \ldots & \ldots & \ldots \\
                                a_{m1} & a_{m2} & \ldots & a_{mn} & b_m
                          \end{array}\right]\,.

Podanie macierzy :math:`\ \boldsymbol{B}\,`
określa całkowicie układ równań :eq:`01`,
a operacjom elementarnym na równaniach odpowiadają 
analogiczne operacje na wierszach tej macierzy:

1. :math:`\,` przestawienie dwóch wierszy,
2. :math:`\,` pomnożenie dowolnego wiersza przez liczbę różną od zera,
3. | :math:`\,` dodanie do jednego z wierszy 
     dowolnej wielokrotności innego wiersza
   | (w szczególności: :math:`\,` dodanie bądź odjęcie dwóch wierszy).

Przekształcenia te dają układ równoważny wyjściowemu.
Operacje elementarne na kolumnach macierzy :math:`\,\boldsymbol{B}\,`
zmieniają na ogół zbiór rozwiązań, a więc nie są dopuszczalne 
przy rozwiązywaniu problemów liniowych. Czasem warto jednak zmienić kolejność 
kolumn macierzy :math:`\,\boldsymbol{A},\,` co prowadzi do układu równań 
różniącego się od wyjściowego jedynie numeracją niewiadomych.

Postać schodkowa macierzy
~~~~~~~~~~~~~~~~~~~~~~~~~

Zaczniemy od kilku definicji.

* Wiersz macierzy składający się z samych zer nazywamy *wierszem zerowym*.
* Wiersz, w którym nie wszystkie elementy znikają, jest *wierszem niezerowym*.
* *Element wiodący* (ang. pivot) danego wiersza niezerowego jest pierwszym
  od lewej elementem różnym od zera.

Macierz ma :math:`\,` *wierszową postać schodkową*, :math:`\,` gdy:

1. :math:`\,` wszystkie wiersze zerowe (jeśli takie występują) 
   są pod wierszami niezerowymi;
2. :math:`\,` jeżeli dwa sąsiednie wiersze są niezerowe, 
   to element wiodący wiersza dolnego jest przesunięty w prawo 
   względem elementu wiodącego wiersza górnego.

.. (począwszy od wiersza drugiego, element wiodący każdego wiersza niezerowego
   jest przesunięty w prawo względem elementu wiodącego wiersza leżącego 
   bezpośrednio nad nim)

Wynika stąd, że jeżeli w danej kolumnie występuje element wiodący pewnego 
wiersza, to wszystkie elementy tej kolumny leżące pod tym elementem wiodącym są 
równe zeru (a zatem poniżej głównej przekątnej macierzy występują tylko zera).

.. | (nie ma elementów niezerowych poniżej głównej przekątnej macierzy).

Przykład macierzy w wierszowej postaci schodkowej (zaznaczone elementy wiodące):

.. math::
   
   \left[\begin{array}{rrrrr}
   \boxed{2} &       -1  & 0 &        5  &        4  \\
          0  & \boxed{5} & 3 &        1  &       -1  \\
          0  &        0  & 0 & \boxed{1} &        8  \\
          0  &        0  & 0 &        0  & \boxed{7}
   \end{array}\right]\,.

   \;

Macierz jest w :math:`\,` *zredukowanej wierszowej postaci schodkowej*, 
:math:`\,` gdy dodatkowo:

3. :math:`\,` wszystkie elementy wiodące są równe 1 :math:`\,` 
   (nazywamy je wtedy jedynkami wiodącymi);
4. :math:`\,` każda jedynka wiodąca jest jedynym 
   elementem niezerowym w swojej kolumnie.

Przykład zredukowanej wierszowej postaci schodkowej 
(zaznaczone jedynki wiodące):

.. math::
   
   \left[\begin{array}{rrrrr}
   \boxed{1} &        0  & 6 &        0  &  2 \\
          0  & \boxed{1} & 3 &        0  & -1 \\
          0  &        0  & 0 & \boxed{1} &  4 \\
          0  &        0  & 0 &        0  &  0
   \end{array}\right]\,.
   
   \;

W analogiczny sposób można zdefiniować (*zredukowaną*) 
*kolumnową postać schodkową* macierzy.
Macierz będzie w (zredukowanej) kolumnowej postaci schodkowej wtedy,
gdy jej transpozycja ma (zredukowaną) wierszową postać schodkową.

Ponieważ operacjom na równaniach odpowiadają odpowiednie operacje na wierszach 
macierzy rozszerzonej, w dalszym ciągu interesować nas będzie wyłącznie 
wierszowa wersja postaci schodkowej. :math:`\\`

Rozważania te można uogólnić na przypadek macierzy
określonej nad dowolnym pierścieniem :math:`\,P\,` z jednością
(np. nad pierścieniem liczb całkowitych :math:`\,Z).`

Operacje elementarne na wierszach są teraz następujące:

1. :math:`\,` przestawienie dwóch wierszy,
2. :math:`\,` pomnożenie wybranego wiersza przez 
   dowolny *odwracalny* element pierścienia,
3. :math:`\,` dodanie do jednego z wierszy innego wiersza, 
   pomnożonego przez dowolny element pierścienia 
   (w szczególności: dodanie bądź odjęcie dwóch wierszy).

Wykonując operacje elementarne na wierszach, można każdą macierz 
nad pierścieniem :math:`\,P\,` z jednością przekształcić do postaci schodkowej. 
Postępowanie takie nazywa się eliminacją Gaussa.
Natomiast każdą macierz nad ciałem :math:`\,K\,` da się w ten sposób doprowadzić
do (jednoznacznie określonej) zredukowanej postaci schodkowej
:math:`\,` - :math:`\,` mówi się wtedy o eliminacji Gaussa-Jordana.

Poniższa macierz :math:`\,\boldsymbol{A}\,` może być określona 
zarówno nad pierścieniem liczb całkowitych :math:`\,Z,\,`
jak i nad ciałem liczb wymiernych :math:`\,Q:`

.. math::

   \boldsymbol{A}\ =\   
   \left[\begin{array}{rrrr}
      2 & 5 &  3 &  0 \\
      2 & 0 & -2 & -1 \\
      0 & 0 &  4 &  5 \\
   \end{array}\right]\,.

Jeżeli :math:`\,\boldsymbol{A}\,` jest macierzą nad pierścieniem :math:`\,Z,\,`
to wykonując operacje elementarne na jej wierszach :math:`\,r0,\,r1,\,r2\,`
(w Sage numeracja zaczyna się od zera!)
da się ją doprowadzić jedynie do postaci schodkowej:

.. math::

   \begin{array}{ccccc}
      & & \begin{array}{c}\small{r1=r1-r0,} \\
                          \small{r1=r1+r2:}\end{array} 
      & & \begin{array}{c}\small{r0=r0+r1,} \\
                          \small{r1=-r1:} \end{array} \\ \\
      \left[\begin{array}{rrrr}
         2 & 5 &  3 &  0 \\
         2 & 0 & -2 & -1 \\
         0 & 0 &  4 &  5 \\
      \end{array}\right] & \rightarrow & 
      \left[\begin{array}{rrrr}
         2 &  5 &  3 & 0 \\
         0 & -5 & -1 & 4 \\
         0 &  0 &  4 & 5 \\
      \end{array}\right] & \rightarrow & 
      \left[\begin{array}{rrrr}
         2 & 0 & 2 &  4 \\
         0 & 5 & 1 & -4 \\
         0 & 0 & 4 &  5 \\
      \end{array}\right]
   \end{array}

Postać schodkowa jest faktycznie osiągnięta już w pierwszym kroku.
Dalsze przekształcenia zmierzają do postaci zredukowanej, 
której jednak nie da się otrzymać
w ramach operacji elementarnych w pierścieniu :math:`\,Z.`

Jeżeli przyjąć, że :math:`\,\boldsymbol{A}\,` 
jest macierzą nad ciałem :math:`\,Q,\,`
to przekształcenia można kontynuować aż do zredukowanej postaci schodkowej:

.. math::

   \begin{array}{cccccc}
        & \begin{array}{c} \small{r0=2\ r0,} \\ 
                           \small{r1=4\ r1:} \end{array} 
      & & \begin{array}{c} \small{r0=r0-r2,} \\
                           \small{r1=r1-r2:} \end{array}
      & & \begin{array}{c} \small{r0=r0/4,}  \\
                           \small{r1=r1/20,} \\
                           \small{r2=r2/4:} \end{array} \\ \\
      \rightarrow &
      \left[\begin{array}{rrrr}
         4 &  0 & 4 &   8 \\
         0 & 20 & 4 & -16 \\
         0 &  0 & 4 &   5 \\
      \end{array}\right] & \rightarrow & 
      \left[\begin{array}{rrrr}
         4 &  0 & 0 &   3 \\
         0 & 20 & 0 & -21 \\
         0 &  0 & 4 &   5 \\
      \end{array}\right] & \rightarrow & 
      \left[\begin{array}{cccc}
         1 & 0 & 0 &   3/4  \\
         0 & 1 & 0 & -21/20 \\
         0 & 0 & 1 &   5/4  \\
      \end{array}\right]\,.
   \end{array}

   \;


