
Zmiana bazy przestrzeni wektorowej
----------------------------------

Jeżeli w przestrzeni wektorowej została wybrana baza, to każdy wektor jest 
jednoznacznie określony przez swoje współrzędne, a każdy operator liniowy 
:math:`\,` - :math:`\,` przez swoją macierz w tej bazie. W różnych bazach ten 
sam wektor ma jednak różne współrzędne, a ten sam operator 
:math:`\,` - :math:`\,` różne macierze.

W tej sekcji wyprowadzimy wzory, opisujące transformację współrzędnych wektorów 
i macierzy operatorów liniowych przy przejściu od jednej do drugiej bazy.

Macierz przejścia
~~~~~~~~~~~~~~~~~

Niech układy :math:`\ \mathcal{B}\,=\,(v_1,\,v_2,\,\dots,\,v_n)\ ` 
i :math:`\ \,\mathcal{B'}\,=\,(v_1',\,v_2',\,\dots,\,v_n')\ ` będą dwiema bazami
przestrzeni wektorowej :math:`\,V\ ` nad ciałem :math:`\,K.`

.. admonition:: Lemat.
   
   Przekształcenie liniowe :math:`\ T:\,V\rightarrow V,\ ` zadane równaniem 
   
   .. math::
   
      Tv_i\ :\,=\ v_i'\,,\qquad i=1,2,\dots,n,
   
   jest automorfizmem przestrzeni wektorowej :math:`\,V.\ \\`
   Nazywamy go :math:`\,` *automorfizmem przejścia* :math:`\,` 
   od bazy :math:`\ \mathcal{B}\ ` do bazy :math:`\ \mathcal{B'}.`

.. które przekształca wektory bazy :math:`\ \mathcal{B}\ ` 
   w odpowiednie wektory bazy :math:`\ \mathcal{B}':`

**Dowód.** :math:`\, \\` 
Zadanie obrazów wektorów bazy :math:`\ \mathcal{B}\ ` określa przekształcenie 
liniowe :math:`\,T\ ` jednoznacznie (patrz wniosek do Twierdzenia 5.).

Dla dowolnego wektora 
:math:`\displaystyle\ \,v=\sum_{i\,=\,1}^n\ a_i\,v_i\,\in\,V\ \,` mamy

.. math::
   
   T\,\left(\,\sum_{i\,=\,1}^n\ a_i\,v_i\right)\ \ =\ \ 
   \sum_{i\,=\,1}^n\ a_i\;Tv_i\ \ =\ \ \sum_{i\,=\,1}^n\ a_i\,v_i'\,.


Wektor, którego współrzędnymi w bazie :math:`\ \mathcal{B}\ \,` są 
:math:`\ \,\,a_1,\,a_2,\,\dots,\,a_n\,,\ \,`
jest przekształcony w wektor o tych samych współrzędnych w bazie 
:math:`\ \mathcal{B}'.\ ` Ponieważ, przy ustalonej bazie, przyporządkowanie 
wektorom układów współrzędnych jest wzajemnie jednoznaczne, przekształcenie 
:math:`\ T\ ` jest endomorfizmem bijektywnym, czyli automorfizmem.

.. admonition:: Definicja.
   
   | *Macierz przejścia* :math:`\ \boldsymbol{S}\ ` 
     od bazy :math:`\ \mathcal{B}\ ` do bazy :math:`\ \mathcal{B}'\ `
     przestrzeni wektorowej :math:`\,V\,` 
   | jest macierzą automorfizmu przejścia :math:`\,T\ ` 
     w bazie :math:`\,\mathcal{B}:\quad\boldsymbol{S}\ :\,=
     \ M_{\mathcal{B}}(T)\,.`

Niech :math:`\ \boldsymbol{S}\ =\ [\,s_{ij}\,]_{n\times n}\,.\ `
Z definicji macierzy operatora liniowego wynikają związki

.. math::
   :label: base_0

   \begin{array}{lcl}
   & & v_j'\;=\ Tv_j\;=\ \displaystyle\sum_{i\,=\,1}^n\ s_{ij}\:v_i\,,\qquad 
   j=1,2,\dots,n\,, \\ \\
   \text{czyli} & \qquad\quad &
   \begin{array}{l}
   v_1'\ =\ s_{11}\,v_1\,+\ s_{21}\,v_2\,+\ \dots\ +\ s_{n1}\,v_n \\
   v_2'\ =\ s_{12}\,v_1\,+\ s_{22}\,v_2\,+\ \dots\ +\ s_{n2}\,v_n \\
   \ \dots \\
   v_n'\ =\ s_{1n}\,v_1\,+\ s_{2n}\,v_2\,+\ \dots\ +\ s_{nn}\,v_n
   \end{array}
   \end{array}

z których wynika praktyczny sposób konstrukcji macierzy przejścia:

.. admonition:: Wniosek 1. :math:`\\`
   
   :math:`j`-ta kolumna macierzy przejścia :math:`\ \boldsymbol{S}\ `
   od bazy :math:`\ \mathcal{B}\ ` do bazy :math:`\ \mathcal{B}'\ ` przestrzeni 
   :math:`\,V\,` jest kolumną współrzędnych :math:`\,` (w bazie 
   :math:`\ \mathcal{B}`) :math:`\,` :math:`j`-tego wektora bazy 
   :math:`\ \mathcal{B}',\ \ j=1,2,\dots,n:`
   
   .. math::
      :label: S_col
      
      \boldsymbol{S}\ \,=\ \,\left[\,I_{\mathcal{B}}(v_1')\,|\,
                                     I_{\mathcal{B}}(v_2')\,|\,
                                     \dots\,|\,
                                     I_{\mathcal{B}}(v_n')\,\right]\,.

Istotną własność macierzy przejścia stwierdza

.. admonition:: Wniosek 2. 
   
   Macierz przejścia jest nieosobliwa: :math:`\ \ \det\,\boldsymbol{S}\neq 0\,.`

**Dowód.** :math:`\,` Odwzorowanie :math:`\,I_{\mathcal{B}},\ ` jako izomorfizm
przestrzeni :math:`\,V\ ` na przestrzeń :math:`\,K^n,\ ` zachowuje liniową 
niezależność wektorów. Z liniowej niezależności wektorów 
:math:`\ v_1',\,v_2',\,\dots,\,v_n'\ ` bazy :math:`\ \mathcal{B'}\ `
wynika więc liniowa niezależność kolumn macierzy :math:`\ \boldsymbol{S},\ \,` 
a to implikuje niezerową wartość jej wyznacznika.

**Przykład.**

Rozważmy trójwymiarową przestrzeń :math:`\,V\ ` z bazami 
:math:`\ \mathcal{B}=(v_1,\,v_2,\,v_3)\ \,\text{i}\ \ \mathcal{B'}=
(v_1',\,v_2',\,v_3'),\ \,` gdzie :math:`\ \ v_1'=
\,v_1,` :math:`\ \ v_2'=\,v_1+\,v_2,` :math:`\ \ v_3'=\,v_1+\,v_2+\,v_3\,.`

Związki pomiędzy wektorami obydwu baz można zapisać jako

.. math::
   
   \begin{array}{l}
   v_1'\ =\ 1\cdot v_1\,+\;0\cdot v_2\,+\;0\cdot v_3    \\
   v_2'\ =\ 1\cdot v_1\,+\;1\cdot v_2\,+\;0\cdot v_3    \\
   v_3'\ =\ 1\cdot v_1\,+\;1\cdot v_2\,+\;1\cdot v_3\,, \\
   \end{array}
   \qquad\text{skąd macierz przejścia}\qquad
   \boldsymbol{S}\ =\ 
   \left[\begin{array}{ccc} 
    1 & 1 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 1 
   \end{array}\right]\,. 

Wzory transformacyjne
~~~~~~~~~~~~~~~~~~~~~

Odtąd bazy :math:`\ \mathcal{B}\,=\,(v_1,\,v_2,\,\dots,\,v_n)\ ` 
i :math:`\ \,\mathcal{B'}\,=\,(v_1',\,v_2',\,\dots,\,v_n')\ `
będą nazywane odpowiednio starą i nową bazą.
Relacje :eq:`base_0` pomiędzy ich wektorami można przepisać następująco:

.. math::

   \begin{array}{lcl}
   & & v_i'\;=\ Tv_i\;=\ \displaystyle\sum_{j\,=\,1}^n\ s_{ij}^T\:v_j\,,\qquad
    i=1,2,\dots,n\,, \\ \\
   \text{czyli} & \qquad\quad &
   \begin{array}{l}
   v_1'\ =\ s_{11}^T\,v_1\,+\ s_{12}^T\,v_2\,+\ \dots\ +\ s_{1n}^T\,v_n \\
   v_2'\ =\ s_{21}^T\,v_1\,+\ s_{22}^T\,v_2\,+\ \dots\ +\ s_{2n}^T\,v_n \\
   \ \dots                                                              \\
   v_n'\ =\ s_{n1}^T\,v_1\,+\ s_{n2}^T\,v_2\,+\ \dots\ +\ s_{nn}^T\,v_n \\
   \end{array}
   \end{array}

Ten układ :math:`\,n\ ` równości jest równoważny jednemu równaniu macierzowemu

.. math::
   :label: trans_base

   \blacktriangleright\quad   
   \left[\begin{array}{c} v_1' \\ v_2' \\ \dots \\ v_n' \end{array}\right]\ \,=
   \ \,\boldsymbol{S}^{\,T}\,
   \left[\begin{array}{c} v_1 \\ v_2 \\ \dots \\ v_n \end{array}\right]\,.
   
.. admonition:: Reguła 0. :math:`\,` Transformacja wektorów bazy.
   
   Kolumna złożona z wektorów nowej bazy równa się iloczynowi transponowanej 
   macierzy przejścia przez kolumnę, złożoną z wektorów starej bazy.

Warto zauważyć, że (inaczej niż w dotychczasowych równaniach macierzowych) 
elementami kolumn po obydwu stronach są nie *skalary* (liczby), ale *wektory*.
Natomiast macierz w tym równaniu jest zwykłą macierzą liczbową.

Aby określić sposób transformowania się współrzędnych wektorów 
przy zmianie bazy, zapiszemy przedstawienie dowolnego wektora 
:math:`\,v\in V\ ` w starej i nowej bazie:

.. math::
   :nowrap:
   
   \begin{eqnarray*}
   \sum_{i\,=\,1}^n\ a_i\:v_i\ 
    & = & \ \sum_{j\,=\,1}^n\ a_j'\ v_j' \ \ =            \\
    & = & \ \sum_{j\,=\,1}^n\ a_j'\ \left(\,
            \sum_{i\,=\,1}^n\ s_{ij}\:v_i\right) \ \ =    \\
    & = & \ \sum_{i\,=\,1}^n\ \left(\,
            \sum_{j\,=\,1}^n\ s_{ij}\:a_j'\right)\;v_i\,. \\
   \end{eqnarray*}

Z jednoznaczności przedstawienia wektora w bazie :math:`\ \mathcal{B}\ ` 
wynikają związki

.. math::
   
   \begin{array}{lcl}
   & & a_i\ =\ \displaystyle\sum_{j\,=\,1}^n\ s_{ij}\:a_j'\,,\qquad 
   i=1,2,\dots,n\,, \\ \\
   \text{czyli} & \qquad\quad &
   \begin{array}{l}
   a_1\ =\ s_{11}\,a_1'\,+\ s_{12}\,a_2'\,+\ \dots\ +\ s_{1n}\,a_n' \\
   a_2\ =\ s_{21}\,a_1'\,+\ s_{22}\,a_2'\,+\ \dots\ +\ s_{2n}\,a_n' \\
   \ \dots                                                          \\
   a_n\ =\ s_{n1}\,a_1'\,+\ s_{n2}\,a_2'\,+\ \dots\ +\ s_{nn}\,a_n' \\
   \end{array}
   \end{array}

Przechodząc do zapisu macierzowego, otrzymujemy

.. math::
   :label: trans_coord
   
   \left[\begin{array}{c} a_1 \\ a_2 \\ \dots \\ a_n \end{array}\right]
   \ \,=\ \,\boldsymbol{S}\;
   \left[\begin{array}{c} a_1' \\ a_2' \\ \dots \\ a_n' \end{array}\right]\,,
   \qquad\qquad\blacktriangleright\quad
   \left[\begin{array}{c} a_1' \\ a_2' \\ \dots \\ a_n' \end{array}\right]
   \ \,=\ \,\boldsymbol{S}^{-1}\,
   \left[\begin{array}{c} a_1 \\ a_2 \\ \dots \\ a_n \end{array}\right]\,.

.. admonition:: Reguła 1. :math:`\,` Transformacja współrzędnych wektora.
   
   .. Kolumna współrzędnych wektora w starej bazie równa się 
      iloczynowi macierzy przejścia przez kolumnę współrzędnych w nowej bazie.

   Kolumna współrzędnych wektora w nowej bazie równa się iloczynowi odwrotności 
   macierzy przejścia przez kolumnę współrzędnych w starej bazie.

   .. math::
      
      I_{\mathcal{B}'}(v)\ \ =
      \ \ \boldsymbol{S}^{-1}\,\cdot\,I_{\mathcal{B}}(v)\,,\qquad v\in V.
      

Zajmiemy się teraz transformacją macierzy operatora liniowego.

Niech :math:`\,F\in\text{End}(V),\quad 
M_{\mathcal{B}}(F)=\boldsymbol{F}=[\,f_{ij}\,]_{n\times n}\,,\quad
M_{\mathcal{B}'}(F)=\boldsymbol{F}'=[\,f_{ij}'\,]_{n\times n}\,.`

Wychodząc z definicji macierzy operatora :math:`\,F\ ` w bazie 
:math:`\,\mathcal{B}'\ ` otrzymujemy (:math:`j=1,2,\dots,n`):

.. math::
   :nowrap:
   
   \begin{eqnarray*}
   Fv_j' & = & \sum_{i\,=\,1}^n\ f_{ij}'\ v_i'\,,                          \\
   F\left(Tv_j\right) & = & \sum_{i\,=\,1}^n\ f_{ij}'\ Tv_i\,,             \\
   T^{-1}\left[\,F\left(Tv_j\right)\,\right] & = & \sum_{i\,=
   \,1}^n\ f_{ij}'\ T^{-1}(Tv_i)\,,                                        \\
   (T^{-1}\circ\,F\,\circ\,T)\ v_j & = & \sum_{i\,=\,1}^n\ f_{ij}'\ v_i\,. \\
   \end{eqnarray*}

Ostatnie równanie stwierdza, że :math:`\,\boldsymbol{F}'\ ` jest macierzą 
:math:`\,` (w bazie :math:`\,\mathcal{B}`) :math:`\,` operatora
:math:`\ \,T^{-1}\circ\,F\,\circ\,T` :

.. math::
   
   \boldsymbol{F}'\ =
   \ M_{\mathcal{B}}\left(\,T^{-1}\circ\,F\,\circ\,T\,\right)\ \,=\ \,
   M_{\mathcal{B}}(T^{-1})\,\cdot\,M_{\mathcal{B}}(F)\,
   \cdot\,M_{\mathcal{B}}(T)\ =
   
   =\  
   [\,M_{\mathcal{B}}(T)\,]^{-1}\,\cdot\,M_{\mathcal{B}}(F)\,
   \cdot\,M_{\mathcal{B}}(T)\ \,=\ \,\boldsymbol{S}^{-1}\,\boldsymbol{F}
   \ \boldsymbol{S}\,.

W ten sposób macierz :math:`\,\boldsymbol{F}'\ ` operatora liniowego 
:math:`\,F\ ` w bazie :math:`\,\mathcal{B}'\ ` dana jest przez

.. math::
   :label: F_prim
   
   \blacktriangleright\quad
   \boldsymbol{F}'\ =\ \boldsymbol{S}^{-1}\,\boldsymbol{F}\ \boldsymbol{S}\,.
   
.. .. math::

      \text{Ostatecznie}\qquad\blacktriangleright\quad
      \boldsymbol{F}'\ =\ \boldsymbol{S}^{-1}\,\boldsymbol{F}\ \boldsymbol{S}\,.
   
      Ostatecznie, macierz :math:`\,\boldsymbol{F}\ ` operatora liniowego 
      :math:`\,F\ ` przy zmianie bazy transformuje się następująco: 
   
      Ostatecznie, transformacja macierzy :math:`\,\boldsymbol{F}\ ` 
      operatora liniowego :math:`\,F\ ` wyraża się wzorem
   
.. admonition:: Reguła 2. :math:`\,` Transformacja macierzy operatora liniowego.
   
   Przy zmianie bazy opisanej przez macierz przejścia :math:`\,\boldsymbol{S}\ `
   macierz operatora liniowego :math:`\,F\ ` transformuje się według wzoru:
   
   .. math::
      
      M_{\mathcal{B}'}(F)\ \,=\ \,
      \boldsymbol{S}^{-1}\,\cdot\,M_{\mathcal{B}}(F)\,\cdot\,\boldsymbol{S}\,.

.. .. math::

      \begin{array}{lcc}
       & & \boldsymbol{F}'\ =\ 
       \boldsymbol{S}^{-1}\,\boldsymbol{F}\ \boldsymbol{S}\,, \\ \\
       \blacktriangleright & \quad & M_{\mathcal{B}'}(F)\ \,=\ \,
       \boldsymbol{S}^{-1}\,\cdot\,M_{\mathcal{B}}(F)\,\cdot\,\boldsymbol{S}\,.
      \end{array}

   .. math::

   \begin{array}{cccc}
    & & & \boldsymbol{F}'\ =\ 
    \boldsymbol{S}^{-1}\,\boldsymbol{F}\ \boldsymbol{S}\,, \\ \\
    \text{czyli}\quad & \quad\blacktriangleright & \quad & 
    M_{\mathcal{B}'}(F)\ \,=\ \,
    \boldsymbol{S}^{-1}\,\cdot\,M_{\mathcal{B}}(F)\,\cdot\,\boldsymbol{S}\,.
   \end{array}

**Uwaga.**

Z porównania wzorów :eq:`trans_base` oraz :eq:`trans_coord` wynika, 
że przy zmianie bazy współrzędne wektorów transformują się inaczej 
niż wektory bazy, :math:`\,` chyba że 

.. math::
   :label: orth_mat
   
   \boldsymbol{S}^{-1}\;=\ \boldsymbol{S}^{\,T}\,,
   \qquad\text{czyli}\qquad
   \boldsymbol{S}^{\,T}\boldsymbol{S}\ =\ \boldsymbol{I}_n\,.

Macierz :math:`\,\boldsymbol{S}\in M_n(K)\ ` spełniająca warunek :eq:`orth_mat` 
nazywa się :math:`\,` *macierzą ortogonalną*.

Przykładem jest macierz :math:`\,\boldsymbol{S}\,` przedstawiająca obrót 
bazy :math:`\,\mathcal{B}=(\vec{e}_1,\,\vec{e}_2,\,\vec{e}_3)\ ` trójwymiarowej 
przestrzeni wektorów geometrycznych, gdzie :math:`\,(\vec{e}_1,\,\vec{e}_2,
\,\vec{e}_3)\ ` jest trójką wzajemnie prostopadłych wektorów jednostkowych. 
Ortogonalne są również macierze permutacji.

.. Innym przykładem mogą być macierze permutacji.
  
**Ćwiczenie.**

1. Uzasadnij, że macierz przejścia :math:`\ \boldsymbol{S}\ ` od bazy 
   :math:`\,\mathcal{B}\ ` do bazy :math:`\,\mathcal{B}'\ ` można równoważnie 
   zdefiniować jako macierz automorfizmu przejścia :math:`\,T\ ` 
   w nowej bazie :math:`\,\mathcal{B}':`
   
   .. math::
      
      \boldsymbol{S}\ :\,=\ M_{\mathcal{B}}(T)\ =\ M_{\mathcal{B}'}(T)\,.

2. W uzupełnieniu wyprowadzenia wzoru :eq:`F_prim` pokaż, 
   że jeżeli :math:`\,T\in\text{Aut}(V),\ ` to

   .. math::
      
      M_{\mathcal{B}}(T^{-1})\ \ =\ \ [\,M_{\mathcal{B}}(T)\,]^{-1}\,.


