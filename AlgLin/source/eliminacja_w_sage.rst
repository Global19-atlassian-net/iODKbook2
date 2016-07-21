Praktyczna eliminacja w Sage
----------------------------

W systemie Sage istnieją funkcje (dokładnie: metody),
które wykonują operacje elementarne na macierzach:

#. ``swap_rows(i,j)`` przestawia wiersze i-ty oraz j-ty;
#. ``rescale_row(i,a)`` mnoży i-ty wiersz przez czynnik a;
#. ``add_multiple_of_row(i,j,a)`` do i-tego wiersza 
   dodaje wiersz j-ty pomnożony przez czynnik a.

Jeżeli :math:`\,\boldsymbol{A}\,` jest macierzą, 
:math:`\ \,\boldsymbol{b}\ \ \,\text{-}\ ` wektorem albo macierzą o zgodnej 
z :math:`\,\boldsymbol{A}\,` liczbie wierszy, :math:`\,` to polecenie 
``A.augment(b)`` zwraca macierz, otrzymaną przez dopisanie 
:math:`\,\boldsymbol{b}\,` z prawej strony do :math:`\,\boldsymbol{A}\,`
(wektor :math:`\,\boldsymbol{b}\,` jest przekształcony wcześniej do macierzy 
1-kolumnowej). Metodę ``augment()`` można więc użyć do utworzenia macierzy 
rozszerzonej z macierzy współczynników i kolumny wolnych wyrazów. 

Metoda ``echelon_form()`` zwraca macierz (zadaną nad dowolnym pierścieniem 
z jednością) przekształconą do postaci schodkowej, natomiast ``rref()`` 
(ang.: reduced row echelon form) - macierz przekształconą do zredukowanej 
postaci schodkowej. Jeżeli pierścieniem bazowym macierzy nie jest ciało, 
to operacja ``rref()`` jest wykonywana na równoważnej macierzy nad ciałem liczb wymiernych.

Obie metody dają w wyniku przekształconą macierz, pozostawiając niezmieniony 
oryginał. Odmianą metody ``echelon_form()`` jest ``echelonize()``,
która wykonuje operację bezpośrednio na macierzy oryginalnej. 

Operacje ``echelon_form()`` oraz ``echelonize()`` mają opcjonalny argument logiczny
'transformation', którego wartość ``True`` daje dodatkowo macierz 
:math:`\ \boldsymbol{T}\,` transformującą wyjściową macierz 
:math:`\ \boldsymbol{A}\,` do postaci schodkowej
:math:`\ \boldsymbol{E}\,:\ \boldsymbol{E} = \boldsymbol{T} * \boldsymbol{A}`.

.. :math:`\;`

Dla ilustracji zastosujemy opisane metody 
do macierzy :math:`\ \boldsymbol{A}\ ` z poprzedniej sekcji:
 
.. math::

   \boldsymbol{A}\ =\   
   \left[\begin{array}{rrrr}
      2 & 5 &  3 &  0 \\
      2 & 0 & -2 & -1 \\
      0 & 0 &  4 &  5 \\
   \end{array}\right]\,.

Przekształcenie do postaci schodkowej oraz zredukowanej schodkowej 
przebiega teraz następująco:

.. :math:`\;`
   
.. sagecellserver::
   
   A = matrix([[2, 5, 3, 0],
               [2, 0,-2,-1],
               [0, 0, 4, 5]])
   
   pretty_print(table([[A, '$\\rightarrow$', 
                        A.echelon_form(), '$\\rightarrow$',
                        A.rref()]]))

   (E,T) = A.echelon_form(transformation=True)

   show((E,T))

   T*A == E
   

:math:`\;`

**Przykład 1.** :math:`\,` **Układ oznaczony.**

Zastosujemy metodę eliminacji
do układu równań nad ciałem :math:`\,Q:`

.. math::
   :nowrap:

   \begin{alignat*}{4}
      2\,x_1 & {\,} - {\,} &    x_2 & {\,} - {\,} &    x_3 & {\;} = {\;} &  4 \\
      3\,x_1 & {\,} + {\,} & 4\,x_2 & {\,} - {\,} & 2\,x_3 & {\;} = {\;} & 11 \\
      3\,x_1 & {\,} - {\,} & 2\,x_2 & {\,} + {\,} & 4\,x_3 & {\;} = {\;} & 11
   \end{alignat*}

Macierz współczynników :math:`\,\boldsymbol{A},\,`
kolumna wolnych wyrazów :math:`\,\boldsymbol{b}\,`
oraz macierz rozszerzona :math:`\,\boldsymbol{B}\ `
dane są przez

.. math::

   \boldsymbol{A}\ =\ 
   \left[\begin{array}{rrr}
      2 & -1 & -1 \\
      3 &  4 & -2 \\
      3 & -2 &  4 \\
   \end{array}\right]\,,\quad
   \boldsymbol{b}\ =\ 
   \left[\begin{array}{r}
      4 \\ 11 \\ 11
   \end{array}\right]\,,\qquad
   \boldsymbol{B}\ =\ 
   \left[\begin{array}{rrrr}
      2 & -1 & -1 &  4 \\
      3 &  4 & -2 & 11 \\
      3 & -2 &  4 & 11 \\ 
   \end{array}\right]\,.

   \;

Operacje elementarne na wierszach :math:`\,r0,\,r1,\,r2\,` 
macierzy :math:`\,\boldsymbol{B}:`

.. math::
   
   \begin{array}{cccccc}
      & & \small{r2=r2-r1:} 
      & & \begin{array}{c} 
          \small{r1=r1-r0,} \\ 
          \small{r2=-r2/6:} \\
          \end{array} &  \\ \\
      \left[\begin{array}{rrrr}
         2 & -1 & -1 &  4 \\
         3 &  4 & -2 & 11 \\
         3 & -2 &  4 & 11 \\
      \end{array}\right] & \rightarrow &
      \left[\begin{array}{rrrr}
         2 & -1 & -1 &  4 \\
         3 &  4 & -2 & 11 \\
         0 & -6 &  6 &  0 \\
      \end{array}\right] & \rightarrow &
      \left[\begin{array}{rrrr}
         2 & -1 & -1 & 4 \\
         1 &  5 & -1 & 7 \\
         0 &  1 & -1 & 0 \\
      \end{array}\right] & \rightarrow \\ \\
      \small{r0=r0-2\,r1:} & & \small{r0,r1,r2=r1,r2,r0:} & & 
      \small{r2=r2+11\,r1:} & \\ \\
      \left[\begin{array}{rrrr}
         0 & -11 &  1 & -10 \\
         1 &   5 & -1 &   7 \\
         0 &   1 & -1 &   0 \\
      \end{array}\right] & \rightarrow &
      \left[\begin{array}{rrrr}
         1 &   5 & -1 &   7 \\
         0 &   1 & -1 &   0 \\
         0 & -11 &  1 & -10 \\
      \end{array}\right] & \rightarrow &
      \left[\begin{array}{rrrr}
         1 & 5 &  -1 &   7 \\
         0 & 1 &  -1 &   0 \\
         0 & 0 & -10 & -10 \\
      \end{array}\right] & \rightarrow \\ \\
      \small{r2=-r2/10:} & & \begin{array}{l}
                             \small{r0=r0+r2,} \\
                             \small{r1=r1+r2:} \\
                             \end{array} 
      & & \small{r0=r0-5\,r1:} & \\ \\
      \left[\begin{array}{rrrr}
         1 & 5 & -1 & 7 \\
         0 & 1 & -1 & 0 \\
         0 & 0 &  1 & 1 \\
      \end{array}\right] & \rightarrow &
      \left[\begin{array}{rrrr}
         1 & 5 & 0 & 8 \\
         0 & 1 & 0 & 1 \\
         0 & 0 & 1 & 1 \\
      \end{array}\right] & \rightarrow & 
      \left[\begin{array}{rrrr}
         1 & 0 & 0 & 3 \\
         0 & 1 & 0 & 1 \\
         0 & 0 & 1 & 1 \\
      \end{array}\right]\,. &   
   \end{array}

Program, wykonujący krok po kroku te operacje, przedstawia się następująco:

.. code-block:: python

   sage: A = matrix(QQ,[[2,-1,-1],      # macierz współczynników
                        [3, 4,-2],
                        [3,-2, 4]])

   sage: b = vector([4,11,11])          # wektor wolnych wyrazów

   sage: B = A.augment(b)               # macierz rozszerzona
                                        
   sage: B.add_multiple_of_row(2,1,-1)  # od trzeciego wiersza odejmij drugi
                                        
   sage: B.add_multiple_of_row(1,0,-1)  # od drugiego wiersza odejmij pierwszy
   sage: B.rescale_row(2,-1/6)          # trzeci wiersz podziel przez -6
                                        
   sage: B.add_multiple_of_row(0,1,-2)  # od pierwszego wiersza 
                                        # odejmij podwojony drugi
                                        
   sage: B.swap_rows(0,1)               # przestaw wiersz pierwszy z drugim
   sage: B.swap_rows(1,2)               # przestaw wiersz drugi z trzecim 
                                        
   sage: B.add_multiple_of_row(2,1,11)  # do trzeciego wiersza dodaj drugi 
                                        # pomnożony przez 11
                                        
   sage: B.rescale_row(2,-1/10)         # trzeci wiersz podziel przez -10
                                        
   sage: B.add_multiple_of_row(0,2,1)   # do pierwszego wiersza dodaj trzeci
   sage: B.add_multiple_of_row(1,2,1)   # do drugiego wiersza dodaj trzeci
                                        
   sage: B.add_multiple_of_row(0,1,-5)  # od pierwszego wiersza odejmij drugi 
                                        # pomnożony przez 5

   sage: B                              # pokaż przekształconą macierz B

Funkcja ``rref()`` daje wynik bezpośrednio:

.. code-block:: python

   sage: A = matrix(QQ,[[2,-1,-1],      # macierz współczynników
                        [3, 4,-2],
                        [3,-2, 4]])

   sage: b = vector([4,11,11])          # wektor wolnych wyrazów

   sage: B = A.augment(b)               # macierz rozszerzona   

   sage: B.rref()                       # pokaż zredukowaną 
                                        # schodkową postać macierzy B

   [1 0 0 3]
   [0 1 0 1]
   [0 0 1 1]

Zredukowanej schodkowej macierzy :math:`\,\boldsymbol{B}\,`
odpowiada trywialna postać układu równań:

.. math::
   :nowrap:

   \begin{alignat*}{4}
      1\,x_1 & {\,} + {\,} & 0\,x_2 & {\,} + {\,} & 0\,x_3 & {\;} = {\;} & 3 \\
      0\,x_1 & {\,} + {\,} & 1\,x_2 & {\,} + {\,} & 0\,x_3 & {\;} = {\;} & 1 \\
      0\,x_1 & {\,} + {\,} & 0\,x_2 & {\,} + {\,} & 1\,x_3 & {\;} = {\;} & 1 
   \end{alignat*}

z której odczytujemy od razu rozwiązanie: 
:math:`\ \ x_1 = 3,\ x_2=x_3 = 1.` :math:`\\`

**Ćwiczenie.** :math:`\,`
W komórce z kodem programu zadana jest macierz współczynników 
:math:`\boldsymbol{A}\,` i wektor wolnych wyrazów :math:`\,\boldsymbol{b}\,` 
pewnego układu 4 równań o 4 niewiadomych nad ciałem Q.

1. :math:`\,` Utwórz macierz rozszerzoną :math:`\,\boldsymbol{B}\,`
   i sprowadź ją do zredukowanej postaci schodkowej.

2. | :math:`\,` Dla sprawdzenia otrzymanego rozwiązania zbadaj,
     czy iloczyn macierzy :math:`\boldsymbol{A}\,` przez 
   | kolumnę wyliczonych wartości niewiadomych
     równa się kolumnie wolnych wyrazów.

Wskazówki do punktu 2.: :math:`\,`
Kolumna wartości niewiadomych jest ostatnią kolumną
macierzy rozszerzonej w zredukowanej postaci schodkowej;
można ją wyodrębnić operacją wycinania. Do przekształcenia wektora w macierz 
jednokolumnową służy metoda ``column()``. :math:`\\`

.. sagecellserver::

   A = matrix(QQ,[[1, 2, 3,-2],
                  [2,-1,-2,-3],
                  [3, 2,-1, 2],
                  [2,-3, 2, 1]])
               
   sage: b = vector([6,8,4,-8])

:math:`\,`

**Przykład 2.** :math:`\,` **Układ nieoznaczony.**

Dany układ trzech równań o czterech niewiadomych
nad ciałem liczb wymiernych :math:`\,Q:`

.. math::
   :nowrap:

   \begin{alignat*}{5}
      x_1 & {\,} - {\,} &    x_2 & {\,} + {\,} & 2\,x_3 & {\,} - {\,} &    x_4 & {\;} = {\;} &  1 \\
   2\,x_1 & {\,} - {\,} & 3\,x_2 & {\,} - {\,} &    x_3 & {\,} + {\,} &    x_4 & {\;} = {\;} & -1 \\
      x_1 & {\,}   {\,} &        & {\,} + {\,} & 7\,x_3 & {\,} - {\,} & 4\,x_4 & {\;} = {\;} &  4 \\
   \end{alignat*}

   \;

Macierz rozszerzoną przekształcamy od razu do zredukowanej postaci schodkowej:

.. code-block:: python

   sage: B = matrix(QQ,[[1,-1, 2,-1, 1],
                        [2,-3,-1, 1,-1],
                        [1, 0, 7,-4, 4]])

   sage: table([[B, '$\\rightarrow$', B.rref()]])

.. math::

   \left(\begin{array}{rrrrr}
         1 & -1 &  2 & -1 &  1 \\
         2 & -3 & -1 &  1 & -1 \\
         1 &  0 &  7 & -4 &  4
         \end{array}\right)\quad\rightarrow\quad\left(\begin{array}{rrrrr}
                                                      1 & 0 & 7 & -4 & 4 \\
                                                      0 & 1 & 5 & -3 & 3 \\
                                                      0 & 0 & 0 &  0 & 0
                                                      \end{array}\right)\,,

   \;

której odpowiada równoważny wyjściowemu układ dwóch równań 
o czterech niewiadomych (trzecie równanie o wszystkich współczynnikach zerowych 
jest spełnione tożsamościowo):

.. .. math::
   :nowrap:

   \begin{alignat*}{5}
   1\,x_1 & {\,} + {\,} & 0\,x_2 & {\,} + {\,} & 7\,x_3 & {\,} - {\,} & 4\,x_4 & {\;} = {\;} &  4 \\
   0\,x_1 & {\,} + {\,} & 1\,x_2 & {\,} + {\,} & 5\,x_3 & {\,} - {\,} & 3\,x_4 & {\;} = {\;} &  3 \\
   \end{alignat*}

.. math::

   \begin{array}{l}
   1\,x_1 \ + \ 0\,x_2 \ + \ 7\,x_3 \ - \ 4\,x_4 \ = \ 4     \\
   0\,x_1 \ + \ 1\,x_2 \ + \ 5\,x_3 \ - \ 3\,x_4 \ = \ 3 \,. \\
   \end{array}

   \;

Przepisując go w postaci

.. math::
   
   \begin{array}{c} 
   x_1\ =\ 4\ -\ 7\,x_3\ +\ 4\,x_4 \\ x_2\ =\ 3\ -\ 5\,x_3\ +\ 3\,x_4
   \end{array}

.. .. math::
   :nowrap:

   \begin{alignat*}{4}
      x_1 & {\;} = {\;} & 4 & {\,} - {\,} & 7\,x_3 & {\,} + {\,} & 4\,x_4 \\
      x_2 & {\;} = {\;} & 3 & {\,} - {\,} & 5\,x_3 & {\,} + {\,} & 3\,x_4 \\
   \end{alignat*}

stwierdzamy, że każdemu układowi wartości :math:`\,x_3,\,x_4\,`
odpowiada dokładnie jedna para wartości :math:`\,x_1,\,x_2,` 
dla których układ jest spełniony. 
W tej sytuacji przyjmujemy :math:`\,x_3,\,x_4\,` za dowolne parametry:
:math:`\ x_3 = s,\ x_4 = t,\ ` a rozwiązanie zapisujemy jako

.. math::
   :nowrap:

   \begin{alignat*}{4}
      x_1 & {\;} = {\;} & 4 & {\,} - {\,} & 7\,s & {\,} + {\,} & 4\,t \\
      x_2 & {\;} = {\;} & 3 & {\,} - {\,} & 5\,s & {\,} + {\,} & 3\,t \\
      x_3 & {\;} = {\;} & s \\
      x_4 & {\;} = {\;} & t \\
   \end{alignat*}

gdzie :math:`\,s\ \,\text{i}\ \,t\,` są dowolnymi liczbami wymiernymi. 
:math:`\,` W zapisie wektorowym:

.. math::
   :label: 03

   \left[\begin{array}{c} x_1 \\ x_2 \\ x_3 \\ x_4 \end{array}\right]\ \ =\ \   
   \left[\begin{array}{c}
      4 - 7\,s + 4\,t \\
      3 - 5\,s + 3\,t \\
      s               \\
      t
   \end{array}\right]\ \  =\ \  
   \left[\begin{array}{r}  4 \\  3 \\ 0 \\ 0 \end{array}\right]\ +\ s\ \,
   \left[\begin{array}{r} -7 \\ -5 \\ 1 \\ 0 \end{array}\right]\ +\ t\ \,
   \left[\begin{array}{r} 4 \\ 3 \\ 0 \\ 1 \end{array}\right],\quad
   s,t\in Q.

   \;

Omówiony przykład sugeruje ogólną metodę postępowania z nieoznaczonym układem 
równań: po doprowadzeniu macierzy rozszerzonej do zredukowanej 
postaci schodkowej niewiadome, odpowiadające kolumnom z jedynkami wiodącymi 
wyrażamy poprzez pozostałe niewiadome, po czym te ostatnie przyjmujemy 
za parametry o dowolnych wartościach. :math:`\\`

**Przykład 3.** :math:`\,` **Układ sprzeczny.**

Zbadamy układ równań, różniący się od poprzedniego tylko jednym wolnym wyrazem:

.. math::
   :nowrap:

   \begin{alignat*}{5}
      x_1 & {\,} - {\,} &    x_2 & {\,} + {\,} & 2\,x_3 & {\,} - {\,} &    x_4 & {\;} = {\;} & 1 \\
   2\,x_1 & {\,} - {\,} & 3\,x_2 & {\,} - {\,} &    x_3 & {\,} + {\,} &    x_4 & {\;} = {\;} & 1 \\
      x_1 & {\,}   {\,} &        & {\,} + {\,} & 7\,x_3 & {\,} - {\,} & 4\,x_4 & {\;} = {\;} & 4
   \end{alignat*}

Ta drobna zmiana powoduje, że układ staje się sprzeczny.

Rzeczywiście, macierzy rozszerzonej przekształconej 
do zredukowanej postaci schodkowej:

.. .. code-block:: python

      sage: B = matrix(QQ,[[1,-1, 2,-1, 1],
                           [2,-3,-1, 1, 1],
                           [1, 0, 7,-4, 4]])
      
      sage: table([[B, '$\\rightarrow$', B.rref()]])

.. math::

   \left[\begin{array}{rrrrr}
         1 & -1 &  2 & -1 &  1 \\
         2 & -3 & -1 &  1 &  1 \\
         1 &  0 &  7 & -4 &  4 \\
         \end{array}\right]\quad\rightarrow\quad\left[\begin{array}{rrrrr}
                                                      1 & 0 & 7 & -4 & 0 \\
                                                      0 & 1 & 5 & -3 & 0 \\
                                                      0 & 0 & 0 &  0 & 1 \\
                                                      \end{array}\right]

odpowiada teraz (równoważny wyjściowemu) układ równań

.. math::
   :nowrap:

   \begin{alignat*}{5}
   1\,x_1 & {\,} + {\,} & 0\,x_2 & {\,} + {\,} & 7\,x_3 & {\,} - {\,} & 4\,x_4 & {\;} = {\;} &  0 \\
   0\,x_1 & {\,} + {\,} & 1\,x_2 & {\,} + {\,} & 5\,x_3 & {\,} - {\,} & 3\,x_4 & {\;} = {\;} &  0 \\
   0\,x_1 & {\,} + {\,} & 0\,x_2 & {\,} + {\,} & 0\,x_3 & {\,} + {\,} & 0\,x_4 & {\;} = {\;} &  1
   \end{alignat*}

który ewidentnie nie ma żadnych rozwiązań, 
bo dla żadnych wartości :math:`\,x_1,\,x_2,\,x_3,\,x_4\,`
nie będzie spełnione ostatnie równanie :math:`\ 0=1.`

**Przykład 4.** :math:`\,` **Układ jednorodny.** :math:`\\`

Rozwiążemy teraz układ jednorodny
stowarzyszony z układem w przykładzie 2.:

.. math::
   :nowrap:

   \begin{alignat*}{5}
      x_1 & {\,} - {\,} &    x_2 & {\,} + {\,} & 2\,x_3 & {\,} - {\,} &    x_4 & {\;} = {\;} & 0 \\
   2\,x_1 & {\,} - {\,} & 3\,x_2 & {\,} - {\,} &    x_3 & {\,} + {\,} &    x_4 & {\;} = {\;} & 0 \\
      x_1 & {\,}   {\,} &        & {\,} + {\,} & 7\,x_3 & {\,} - {\,} & 4\,x_4 & {\;} = {\;} & 0
   \end{alignat*}

Po przekształceniu macierzy rozszerzonej do zredukowanej postaci schodkowej:

.. code-block:: python

   sage: B = matrix(QQ,[[1,-1, 2,-1, 0],
                        [2,-3,-1, 1, 0],
                        [1, 0, 7,-4, 0]])

   sage: table([[B, '$\\rightarrow$', B.rref()]])

.. math::

   \left(\begin{array}{rrrrr}
         1 & -1 &  2 & -1 &  0 \\
         2 & -3 & -1 &  1 &  0 \\
         1 &  0 &  7 & -4 &  0
         \end{array}\right)\quad\rightarrow\quad\left(\begin{array}{rrrrr}
                                                      1 & 0 & 7 & -4 & 0 \\
                                                      0 & 1 & 5 & -3 & 0 \\
                                                      0 & 0 & 0 &  0 & 0
                                                      \end{array}\right)

otrzymujemy równoważny układ dwóch równań 
(trzecie jest spełnione tożsamościowo): :math:`\\`

.. math::
   :nowrap:

   \begin{alignat*}{5}
   1\,x_1 & {\,} + {\,} & 0\,x_2 & {\,} + {\,} & 7\,x_3 & {\,} - {\,} & 4\,x_4 & {\;} = {\;} &  0 \\
   0\,x_1 & {\,} + {\,} & 1\,x_2 & {\,} + {\,} & 5\,x_3 & {\,} - {\,} & 3\,x_4 & {\;} = {\;} &  0
   \end{alignat*}

Przepisujemy go jako

.. :math:`\qquad\qquad
   \begin{array}{c} 
   x_1\ =\ -\ 7\,x_3\ +\ 4\,x_4 \\ x_2\ =\ -\ 5\,x_3\ +\ 3\,x_4
   \end{array}`

.. math::
   :nowrap:

   \begin{alignat*}{3}
      x_1 & {\;} = {\,} - {\,} & 7\,x_3 & {\,} + {\,} & 4\,x_4 \\
      x_2 & {\;} = {\,} - {\,} & 5\,x_3 & {\,} + {\,} & 3\,x_4
   \end{alignat*}

i :math:`\,` tak jak w przykładzie 2., :math:`\,` przyjmujemy 
:math:`\,x_3,\,x_4\,` za dowolne parametry: :math:`\ x_3 = s,\ x_4 = t :` 

.. math::

   \begin{array}{l}
      x_1 \ =\ - 7\,s\ +\ 4\,t \\
      x_2 \ =\ - 5\,s\ +\ 3\,t \\
      x_3 \ =\quad s           \\
      x_4 \ =\quad t           \\ 
   \end{array}
   \qquad\qquad s,t\in Q\,.

Ostatecznie, rozwiązanie w postaci wektorowej dane jest przez :math:`\\`

.. math::
   :label: 04

   \left[\begin{array}{c} 
       x_1 \\ x_2 \\ x_3 \\ x_4 
   \end{array}\right]\quad =\quad  
   \left[\begin{array}{c}
      - 7\,s + 4\,t \\
      - 5\,s + 3\,t \\
      s             \\
      t             \\
   \end{array}\right]\quad =\quad 
   s\ \left[\begin{array}{r} -7 \\ -5 \\ 1 \\ 0 \end{array}\right]\ \, +\ \: 
   t\ \left[\begin{array}{r} 4 \\ 3 \\ 0 \\ 1 \end{array}\right]\,,\qquad
   s,t\in Q\,.

   \;

Porównanie rozwiązań :eq:`03` i :eq:`04` układów w przykładach 2. i 4. sugeruje 
związek pomiędzy rozwiązaniami układu niejednorodnego i stowarzyszonego z nim 
układu jednorodnego. Sprawa ta będzie omówiona ogólnie w dalszym rozdziale.




