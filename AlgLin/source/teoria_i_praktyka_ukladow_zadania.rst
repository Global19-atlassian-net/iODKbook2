
Problems
--------

Rank of a Matrix
~~~~~~~~~~~~~~~~

**Zadanie 1.**

Dla macierzy :math:`\ \boldsymbol{A}\in M_{m\times p}(K),\ 
\boldsymbol{B}\in M_{p\times n}(K)\ `
pokazać, że :math:`\ \text{rz}\,\boldsymbol{A}\boldsymbol{B}\ \leq\ 
\text{rz}\boldsymbol{A},\,\text{rz}\boldsymbol{B}.`

**Lemat.**

Niech :math:`\,V_1\,` i :math:`\,\ V_2\ ` będą podprzestrzeniami 
skończonego wymiaru przestrzeni wektorowej :math:`\ V(K):`
:math:`V_1,\,V_2\ <\ V.\ ` Wtedy

.. math::
   
   V_1\ <\ V_2 \qquad\Rightarrow\qquad \dim{V_1}\ \leq\ \dim{V_2}\,.

**Dowód lematu** opiera się na stwierdzeniu, że w przestrzeni 
:math:`\ d`-wymiarowej każdy układ liczący więcej niż 
:math:`\ d\ ` wektorów jest liniowo zależny.

Oznaczmy :math:`\ \dim{V_1}=d_1,\ \dim{V_2}=d_2\ ` i :math:`\ ` 
przypuśćmy, że :math:`\ V_1 < V_2, \ \ \text{przy czym}\ \ d_1>\,d_2\,.`

Niech układ :math:`\ \mathcal{B}\,=\,(\boldsymbol{v}_1,\boldsymbol{v}_2,\dots,
\boldsymbol{v}_{d_1})\ ` będzie bazą podprzestrzeni :math:`\ V_1.`
Ponieważ :math:`\ V_1\subset V_2\,,\ ` to :math:`\ \mathcal{B}\ ` 
byłby również liniowo niezaleznym układem wektorów podprzestrzeni 
:math:`\ V_2,\ ` liczącym :math:`\ d_1>d_2\ ` wektorów 
:math:`\ -\ ` sprzeczność ze wspomnianym na wstępie stwierdzeniem.

A zatem musi być :math:`\ d_1\,\leq\,d_2\,,\ ` co należało udowodnić.

**Dowód twierdzenia.**

Rząd macierzy, równy z definicji liczbie liniowo niezależnych jej 
kolumn (wierszy), równa się wymiarowi przestrzeni rozpiętej na jej 
kolumnach (wierszach).

Stosując kolumnowy lub wierszowy zapis macierzy: 

.. math::

   \begin{array}{l}   
   \boldsymbol{A}\ \,=\ \,
   \left[\,\boldsymbol{A}_1\,|\,\boldsymbol{A}_2\,|
   \,\ldots\,|\,\boldsymbol{A}_p\,\right]\ \, =\ \,
   [a_{ij}]_{m\times p}\,,\qquad
   \boldsymbol{B}\ =\ 
   \left[\begin{array}{c}
   \boldsymbol{B}_1 \\ \boldsymbol{B}_2 \\ \dots \\ \boldsymbol{B}_p 
   \end{array}\right]\ \,=\ \,
   [b_{ij}]_{p\times n}\,,
   \\
   \boldsymbol{A}\boldsymbol{B}\ \,=\ \,
   \left[\,\boldsymbol{C}_1\,|\,\boldsymbol{C}_2\,|
   \,\ldots\,|\,\boldsymbol{C}_n\,\right]\ \, =\ \,
   \left[\begin{array}{c}
   \boldsymbol{R}_1 \\ \boldsymbol{R}_2 \\ \dots \\ \boldsymbol{R}_m 
   \end{array}\right]\ \,=\ \,
   [c_{ij}]_{m\times n}\,.
   \end{array}

otrzymujemy wyrażenia dla rzędów tych macierzy:

.. math::

   \begin{array}{l}
   \text{rz}\,\boldsymbol{A}\ =\ 
   \dim L(\boldsymbol{A}_1\,\boldsymbol{A}_2\,\dots\,\boldsymbol{A}_p)\,,\quad 
   \text{rz}\,\boldsymbol{B}\ =\ 
   \dim L(\boldsymbol{B}_1\,\boldsymbol{B}_2\,\dots\,\boldsymbol{B}_p) \\ \\
   \text{rz}\,\boldsymbol{A}\boldsymbol{B}\ =\ 
   \dim L(\boldsymbol{C}_1\,\boldsymbol{C}_2\,\dots\,\boldsymbol{C}_n)\ =\ 
   \dim L(\boldsymbol{R}_1\,\boldsymbol{R}_2\,\dots\,\boldsymbol{R}_m)\,.
   \end{array}

Według kolumnowej reguły mnożenia macierzowego, każda :math:`\,j`-ta kolumna
macierzy :math:`\ \boldsymbol{A}\boldsymbol{B}\ ` jest kombinacją liniową
kolumn macierzy :math:`\ \boldsymbol{A},\ ` o współczynnikach z :math:`\,j`-tej
kolumny macierzy :math:`\ \boldsymbol{B}`:

.. math::
   
   \boldsymbol{C}_j\ =\ b_{1j}\,\boldsymbol{A}_1\,+\,
                        b_{2j}\,\boldsymbol{A}_2\,+\,\dots\,+\,
                        b_{pj}\,\boldsymbol{A}_p,\quad j=1,2,\dots,n.

Kolumny :math:`\ \boldsymbol{C}_j\ ` należą więc do przestrzeni
generowanej przez kolumny macierzy :math:`\ \boldsymbol{A}\,`:

.. math::
   
   \boldsymbol{C}_j\,\in\,L(\boldsymbol{A}_1,\boldsymbol{A}_2,\dots,
                            \boldsymbol{A}_p),\quad j=1,2,\dots,n\,,

a przestrzeń, generowana przez kolumny :math:`\ \boldsymbol{C}_j`, 
zawiera się w (dokładnie: jest podprzestrzenią) 
przestrzeni generowanej przez kolumny macierzy :math:`\ \boldsymbol{A}\,`:

.. math::
   
   L(\boldsymbol{C}_1,\boldsymbol{C}_2,\dots,\boldsymbol{C}_n)\ <\ 
   L(\boldsymbol{A}_1,\boldsymbol{A}_2,\dots,\boldsymbol{A}_p)\,.

Wynika stąd relacja pomiędzy wymiarami rozważanych przestrzeni:

.. math::
   :label: rz_A

   \begin{array}{lc}   
   & \dim{L(\boldsymbol{C}_1,\boldsymbol{C}_2,\dots,\boldsymbol{C}_n)} 
   \ \leq\ 
   \dim{L(\boldsymbol{A}_1,\boldsymbol{A}_2,\dots,\boldsymbol{A}_p)}
   \\ \\
   \text{czyli} &
   \text{rz}\,\boldsymbol{A}\boldsymbol{B}\ \leq\ \text{rz}\boldsymbol{A}\,.
   \end{array}

.. co, wobec :eq:`ranks` oznacza, że

Według wierszowej reguły mnożenia macierzowego, każdy :math:`\,i`-ty wiersz
macierzy :math:`\ \boldsymbol{A}\boldsymbol{B}\ ` jest kombinacją liniową
wierszy macierzy :math:`\ \boldsymbol{B},\ ` o współczynnikach 
z :math:`\,i`-tego wiersza macierzy :math:`\ \boldsymbol{A}`:

.. math::
   
   \boldsymbol{R}_i\ =\ a_{i1}\,\boldsymbol{B}_1\,+\,
                        a_{i2}\,\boldsymbol{B}_2\,+\,\dots\,+\,
                        a_{ip}\,\boldsymbol{B}_p,\quad i=1,2,\dots,m.

Wiersze :math:`\ \boldsymbol{R}_i\ ` należą więc do przestrzeni
generowanej przez wiersze macierzy :math:`\ \boldsymbol{B}\,`:

.. math::
   
   \boldsymbol{R}_i\,\in\,L(\boldsymbol{B}_1,\boldsymbol{B}_2,\dots,
                            \boldsymbol{B}_p),\quad i=1,2,\dots,m\,,

a przestrzeń, generowana przez wiersze :math:`\ \boldsymbol{R}_i`, 
zawiera się w (dokładnie: jest podprzestrzenią) 
przestrzeni generowanej przez wiersze macierzy :math:`\ \boldsymbol{B}\,`:

.. math::
   
   L(\boldsymbol{R}_1,\boldsymbol{R}_2,\dots,\boldsymbol{R}_m)\ <\ 
   L(\boldsymbol{B}_1,\boldsymbol{B}_2,\dots,\boldsymbol{B}_p)\,.

Wynika stąd relacja pomiędzy wymiarami rozważanych przestrzeni:

.. math::
   :label: rz_B

   \begin{array}{lc}   
   & \dim{L(\boldsymbol{R}_1,\boldsymbol{R}_2,\dots,\boldsymbol{R}_m)} 
   \ \leq\ 
   \dim{L(\boldsymbol{B}_1,\boldsymbol{B}_2,\dots,\boldsymbol{B}_p)}
   \\ \\
   \text{czyli} &
   \text{rz}\,\boldsymbol{A}\boldsymbol{B}\ \leq\ \text{rz}\boldsymbol{B}\,.
   \end{array}

Z równań :eq:`rz_A` oraz :eq:`rz_B` wynika, że jednocześnie 

.. math::

   \begin{array}{lc}   
   & \text{rz}\,\boldsymbol{A}\boldsymbol{B}\ \leq\ \text{rz}\boldsymbol{A}
   \quad\text{oraz}\quad
   \text{rz}\,\boldsymbol{A}\boldsymbol{B}\ \leq\ \text{rz}\boldsymbol{B} 
   \\ \\
   \text{czyli} & \text{rz}\,\boldsymbol{A}\boldsymbol{B}\ \leq\ 
   \text{rz}\boldsymbol{A},\,\text{rz}\boldsymbol{B}\,,
   \end{array}

co właśnie należało wykazać.

**Wniosek.** :math:`\\`
Pomnożenie danej macierzy przez jakąkolwiek macierz 
(z lewej bądź z prawej strony) nie podwyższa rzędu:
otrzymujemy macierz, której rząd jest nie większy od rzędu wyjściowej macierzy.

**Zadanie 2.**

Dane macierze: 
:math:`\ \boldsymbol{A}\in M_{m\times n}(K),\ 
\boldsymbol{B}\in M_m(K),\ \boldsymbol{C}\in M_n(K),\ 
\det{\boldsymbol{B}},\,\det{\boldsymbol{C}}\neq 0`.

Udowodnić, że :math:`\ \text{rz}\,\boldsymbol{B}\boldsymbol{A}\ =\ 
\text{rz}\,\boldsymbol{A}\boldsymbol{C}\ =\ \text{rz}\,\boldsymbol{A}`.

**Rozwiązanie.**

.. .. math::
   
      \begin{cases}
      \begin{array}{ccc}
      \ 2\,x_1  {\,} &- {\,}  x_2  {\;} &= {\;}  1 \\ 
      x_1  {\,} &+ {\,} x_2  {\;} &= {\;}  5
      \end{array}
      \end{cases}`

Niech :math:`\ \boldsymbol{P}\,:\,=\,
\boldsymbol{B}\boldsymbol{A}\ \in M_{m\times n}(K).\ `
Wtedy :math:`\ \boldsymbol{A}\,=\,\boldsymbol{B}^{-1}\boldsymbol{P}\ ` oraz

.. math::

   \begin{array}{ccc}   
   \left.\begin{array}{l}
   \text{rz}\,\boldsymbol{P}\ \,=\ \,
   \text{rz}\,\boldsymbol{B}\,\boldsymbol{A}\ \ \leq\ \ 
   \text{rz}\,\boldsymbol{A} \\
   \text{rz}\,\boldsymbol{A}\ =\ 
   \text{rz}\,\boldsymbol{B}^{-1}\,\boldsymbol{P}\ \leq\ 
   \text{rz}\,\boldsymbol{P}
   \end{array}\right\}
   & \quad\Rightarrow &
   \quad\text{rz}\,\boldsymbol{P}\ =\ \text{rz}\,\boldsymbol{A} \\
   & & \quad\text{rz}\,\boldsymbol{B}\boldsymbol{A}\ =\ 
   \text{rz}\,\boldsymbol{A}
   \end{array}

Niech :math:`\ \boldsymbol{Q}\,:\,=\,
\boldsymbol{A}\boldsymbol{C}\ \in M_{m\times n}(K).\ `
Wtedy :math:`\ \boldsymbol{A}\,=\,\boldsymbol{Q}\boldsymbol{C}^{-1}\ ` oraz

.. math::

   \begin{array}{ccc}   
   \left.\begin{array}{l}
   \text{rz}\,\boldsymbol{Q}\ \,=\ \,
   \text{rz}\,\boldsymbol{A}\,\boldsymbol{C}\ \ \leq\ \ 
   \text{rz}\,\boldsymbol{A} \\
   \text{rz}\,\boldsymbol{A}\ =\ 
   \text{rz}\,\boldsymbol{Q}\,\boldsymbol{C}^{-1}\ \leq\ 
   \text{rz}\,\boldsymbol{Q}
   \end{array}\right\}
   & \quad\Rightarrow &
   \quad\text{rz}\,\boldsymbol{Q}\ =\ \text{rz}\,\boldsymbol{A} \\
   & & \quad\text{rz}\,\boldsymbol{A}\boldsymbol{C}\ =\ 
   \text{rz}\,\boldsymbol{A}
   \end{array}

**Wniosek.** :math:`\\`
Pomnożenie danej macierzy przez macierz kwadratową nieosobliwą
(z lewej bądź z prawej strony) nie zmienia rzędu: 
otrzymujemy macierz tego samego rzędu, co macierz wyjściowa.

Systems of Linear Equations
~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Zadanie 1.**
Używając tylko metod Sage'a dla operacji elementarnych na wierszach:
``swap_rows()``, ``rescale_row()``, ``add_multiple_of_row()``, :math:`\,`
doprowadź macierz :math:`\,\boldsymbol{A}\,` do zredukowanej postaci schodkowej. :math:`\,`
Sprawdź następnie wynik stosując metodę ``rref()``.

.. Aby wygenerować macierz, naciśnij "Wykonaj";
   aby zmienić rozmiar macierzy, wpisz nową wartość n.

.. sagecellserver::

   n = 4
   A = random_matrix(QQ, n, algorithm='echelonizable', rank=n, upper_bound=6)
   table([["A","=",A]])

:math:`\;`

**Zadanie 2.** :math:`\,`
Dana jest macierz rozszerzona :math:`\,\boldsymbol{B}\,` pewnego układu równań liniowych. :math:`\\`
Opierając się na ogólnych twierdzeniach, :math:`\,` jeszcze przed rozwiązaniem:
     
* | rozstrzygnij, czy układ jest oznaczony, nieoznaczony czy sprzeczny
  | (które z tych sytuacji wchodzą tutaj w rachubę?);

* | w przypadku nieoznaczonym określ ilość parametrów, 
  | od których zależy ogólne rozwiązanie.    

Rozwiąż następnie ten układ dwoma sposobami:
   
* | znajdując bezpośrednio jego rozwiązanie szczególne oraz bazę
  | przestrzeni rozwiązań stowarzyszonego z nim układu jednorodnego;
     
* metodą eliminacji, doprowadzając macierz :math:`\,\boldsymbol{B}\,`
  do zredukowanej postaci schodkowej.

.. sagecellserver::
   
   m = 4; n = 5
   B = random_matrix(QQ, m,n+1, algorithm='echelonizable', 
                                rank=3, upper_bound=6)
   table([["B","=",B]])


