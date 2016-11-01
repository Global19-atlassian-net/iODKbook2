Iloczyn prosty (tensorowy) macierzy
-----------------------------------

Definicja i przykłady
~~~~~~~~~~~~~~~~~~~~~

Dane macierze: 
:math:`\ \boldsymbol{A}\,=\,[a_{ij}]_{m\times n}\,,\ `
:math:`\ \boldsymbol{B}\,=\,[b_{ij}]_{p\times q}\in M(K).`

Iloczyn tensorowy tych macierzy ma w zapisie blokowym postać

.. math::
   
   \boldsymbol{A}\otimes\boldsymbol{B}\ :\,=\ 
   \left[\begin{array}{cccc}
   a_{11}\,\boldsymbol{B} & a_{12}\,\boldsymbol{B} & 
           \ldots         & a_{1n}\,\boldsymbol{B} \\
   a_{21}\,\boldsymbol{B} & a_{22}\,\boldsymbol{B} & 
           \ldots         & a_{2n}\,\boldsymbol{B} \\  
           \ldots         &         \ldots         &
           \ldots         &         \ldots         \\
   a_{m1}\,\boldsymbol{B} & a_{m2}\,\boldsymbol{B} & 
           \ldots         & a_{mn}\,\boldsymbol{B} 
   \end{array}\right]\ \in\ M_{mp\times nq}(K). 

Na przykład dla 
:math:`\ \boldsymbol{A}\,=\,\left[\begin{array}{rc}
3 & 2 \\ -1 & 1 \\ -2 & 0 \end{array}\right],\ `
:math:`\ \boldsymbol{B}\,=\,\left[\begin{array}{rc}
2 & -1 \\ 0 & 4 \end{array}\right]:`

.. math::
   
   \boldsymbol{A}\otimes\boldsymbol{B}\,=\,
   \left[\begin{array}{rr}
    3\ \left[\begin{array}{rr} 2 & -1 \\ 0 & 4 \end{array}\right] &
    2\ \left[\begin{array}{rr} 2 & -1 \\ 0 & 4 \end{array}\right] \\[8pt]
   -1\ \left[\begin{array}{rr} 2 & -1 \\ 0 & 4 \end{array}\right] &
    1\ \left[\begin{array}{rr} 2 & -1 \\ 0 & 4 \end{array}\right] \\[10pt]
   -2\ \left[\begin{array}{rr} 2 & -1 \\ 0 & 4 \end{array}\right] &
    0\ \left[\begin{array}{rr} 2 & -1 \\ 0 & 4 \end{array}\right]
   \end{array}\right]\ =\ 
   \left[\begin{array}{rrrr}
    6 & -3 & 4 & -2 \\ 0 & 12 & 0 & 8 \\
   -2 &  1 & 2 & -1 \\ 0 & -4 & 0 & 4 \\
   -4 &  2 & 0 &  0 \\ 0 & -8 & 0 & 0 
   \end{array}\right];

.. math::
   
   \boldsymbol{B}\otimes\boldsymbol{A}\,=\,
   \left[\begin{array}{rr}   
    2\ \left[\begin{array}{rr} 3 & 2 \\ -1 & 1 \\ -2 & 0 \end{array}\right] &
   -1\ \left[\begin{array}{rr} 3 & 2 \\ -1 & 1 \\ -2 & 0 \end{array}\right] 
   \\[16pt]
    0\ \left[\begin{array}{rr} 3 & 2 \\ -1 & 1 \\ -2 & 0 \end{array}\right] &
    4\ \left[\begin{array}{rr} 3 & 2 \\ -1 & 1 \\ -2 & 0 \end{array}\right]
   \end{array}\right]\ =\ 
   \left[\begin{array}{rrrr}
    6 & 4 & -3 & -2 \\
   -2 & 2 &  1 & -1 \\
   -4 & 0 &  2 &  0 \\
    0 & 0 & 12 &  8 \\
    0 & 0 & -4 &  4 \\
    0 & 0 & -8 &  0
   \end{array}\right].

Elementy iloczynu tensorowego macierzy są numerowane podwójnymi wskaźnikami:

.. math::
   
   \begin{array}{lr}
   (\boldsymbol{A}\otimes\boldsymbol{B})_{ij,kl}\,=\ 
   a_{ik}\,b_{jl}, &
   \begin{array}{ll}
   i=1,2,\ldots,m; & k=1,2,\ldots,n; \\
   j=1,2,\ldots,p; & l=1,2,\ldots,q.
   \end{array}
   \end{array}

Wskaźniki :math:`\ i,k\ ` określają odpowiednio 
wiersze, kolumny blokowe; :math:`\ \\`
wskaźniki :math:`\ j,l\ ` określają odpowiednio 
wiersze, kolumny elementarne.

Własności iloczynu prostego
~~~~~~~~~~~~~~~~~~~~~~~~~~~

**0.)** :math:`\,` Iloczyn prosty macierzy jest nieprzemienny:
:math:`\ \boldsymbol{A}\otimes\boldsymbol{B}
\neq\boldsymbol{B}\otimes\boldsymbol{A}.`

Jednak macierze :math:`\ \boldsymbol{A}\otimes\boldsymbol{B}\ `
i :math:`\ \boldsymbol{B}\otimes\boldsymbol{A}\ ` są permutacyjnie 
równoważne, tzn. istnieją macierze permutacji :math:`\ \boldsymbol{P}\ ` 
i :math:`\ \boldsymbol{Q}\ ` takie, że 
:math:`\ \boldsymbol{B}\otimes\boldsymbol{A} \ =\ 
\boldsymbol{P}\,(\boldsymbol{A}\otimes\boldsymbol{B})\,\boldsymbol{Q}.`

Jeżeli macierze :math:`\ \boldsymbol{A}\ ` i :math:`\ \boldsymbol{B}\ `
są kwadratowe, to iloczyny :math:`\ \boldsymbol{A}\otimes\boldsymbol{B}\ ` 
i :math:`\ \boldsymbol{B}\otimes\boldsymbol{A}\ ` są permutacyjnie podobne,
tzn. :math:`\ \boldsymbol{Q}=\boldsymbol{P}^{\,T}=\boldsymbol{P}^{-1}.\ `
Oznacza to, że iloczyn :math:`\ \boldsymbol{A}\otimes\boldsymbol{B}\ `
można przekształcić do postaci :math:`\ \boldsymbol{B}\otimes\boldsymbol{A}\ `
dokonując pewnej permutacji wierszy i takiej samej permutacji kolumn. [1]_

**1.)** :math:`\,` Iloczyn prosty jest łączny 
i rozdzielny względem dodawania macierzy: 

.. math::

   (\boldsymbol{A}\otimes\boldsymbol{B})\otimes\boldsymbol{C}\ =\ 
   \boldsymbol{A}\otimes(\boldsymbol{B}\otimes\boldsymbol{C})   

   (\boldsymbol{A}_1\pm\boldsymbol{A}_2)\otimes\boldsymbol{B}\ =\ 
   (\boldsymbol{A}_1\otimes\boldsymbol{B})\pm
   (\boldsymbol{A}_2\otimes\boldsymbol{B})

   \boldsymbol{A}\otimes(\boldsymbol{B}_1\pm\boldsymbol{B}_2)\ =\ 
   (\boldsymbol{A}\otimes\boldsymbol{B}_1)\pm
   (\boldsymbol{A}\otimes\boldsymbol{B}_2)

oraz jest jednorodny w tym sensie, że
   
.. math::
   
   (\gamma\,\boldsymbol{A})\otimes\boldsymbol{B}\ =\
   \boldsymbol{A}\otimes(\gamma\,\boldsymbol{B})\ =\ 
   \gamma\ (\boldsymbol{A}\otimes\boldsymbol{B}),\quad\gamma\in K.

**2.)** :math:`\,` Jeżeli rozmiary macierzy 
:math:`\ \boldsymbol{A},\boldsymbol{B},\boldsymbol{C},\boldsymbol{D}\ `
są takie, że istnieją iloczyny :math:`\ \boldsymbol{A}\boldsymbol{C}\ ` 
i :math:`\ \boldsymbol{B}\boldsymbol{D},\ ` to

.. math::
   :label: mixed-product
   
   \blacktriangleright\quad
   (\boldsymbol{A}\otimes\boldsymbol{B})\,(\boldsymbol{C}\otimes\boldsymbol{D})
   \ =\ (\boldsymbol{A}\boldsymbol{C})\otimes(\boldsymbol{B}\boldsymbol{D}).

**Dowód.** :math:`\ ` Przyjmiemy macierze 
:math:`\ \boldsymbol{A},\,\boldsymbol{B},\,\boldsymbol{C},\,\boldsymbol{D}\,`
w postaci

.. math::
   
   \begin{array}{lr}
   \boldsymbol{A}\,=\,[a_{ij}]_{m\times r}\,, & \quad
   \boldsymbol{B}\,=\,[b_{ij}]_{p\times s}\,, \\
   \boldsymbol{C}\,=\,[c_{ij}]_{r\times n}\,, & \quad
   \boldsymbol{D}\,=\,[d_{ij}]_{s\times q}\,.
   \end{array}

Sprawdzimy, że macierze po obydwu stronach równości :eq:`mixed-product` 
mają te same rozmiary oraz składają się z tych samych elementów.

a.) :math:`\ ` porównanie rozmiarów macierzy:

.. math::
   
   \begin{array}{rr}
   \begin{array}{rr}
   \boldsymbol{A}\otimes\boldsymbol{B}\ : & mp\times rs \\[4pt]
   \boldsymbol{C}\otimes\boldsymbol{D}\ : & rs\times nq \\[4pt]
   (\boldsymbol{A}\otimes\boldsymbol{B})
   (\boldsymbol{C}\otimes\boldsymbol{D})\ : & mp\times nq 
   \end{array} &
   \begin{array}{rr}
   \boldsymbol{A}\boldsymbol{C}\ : & m\times n \\[4pt]
   \boldsymbol{B}\boldsymbol{D}\ : & p\times q \\[4pt]
   \qquad (\boldsymbol{A}\boldsymbol{C})\otimes
   (\boldsymbol{B}\boldsymbol{D})\ : & mp\times nq 
   \end{array}
   \end{array}

b.) :math:`\ ` porównanie odpowiednich elementów:

.. math::
   
   \begin{array}{l}
   (\boldsymbol{A}\otimes\boldsymbol{B})
   (\boldsymbol{C}\otimes\boldsymbol{D})_{\ |\ ij,\,kl}\ \ = \ 
   \displaystyle\sum_{v=1}^r\ \sum_{w=1}^s\ 
   (\boldsymbol{A}\otimes\boldsymbol{B})_{\ |\ ij,\,vw}\ 
   (\boldsymbol{C}\otimes\boldsymbol{D})_{\ |\ vw,\,kl}\ \ = \\[16pt]
   =\ \ \displaystyle\sum_{v=1}^r\ \sum_{w=1}^s\ 
   a_{iv}\ b_{jw}\ c_{vk}\ d_{wl}\ \ = \ 
   \left(\displaystyle\sum_{v=1}^r\ a_{iv}\ c_{vk}\ \right)
   \left(\displaystyle\sum_{w=1}^s\ b_{jw}\ d_{wl}\ \right)\ \ = \\[26pt]
   =\ \ (\boldsymbol{A}\boldsymbol{C})_{\,|\,ik}\ \cdot\ 
   (\boldsymbol{B}\boldsymbol{D})_{\,|\,jl}\ \ = \ 
   (\boldsymbol{A}\boldsymbol{C})\otimes
   (\boldsymbol{B}\boldsymbol{D})_{\ |\ ij,\,kl}\,;
   \end{array}
   \\[8pt]
   \begin{array}{ll}
   \text{gdzie} &
   \begin{array}{ll}
   i=1,2,\ldots,m; & j=1,2,\ldots,p; \\
   k=1,2,\ldots,n; & l=1,2,\ldots,q.
   \end{array}
   \end{array}

Warto zauważyć szczególny przypadek wzoru :eq:`mixed-product`, w którym

.. math::
   
   \boldsymbol{A}\ =\ 
   \left[\begin{array}{ccc} 
   a_{11} & \ldots & a_{1m} \\ 
   \ldots & \ldots & \ldots \\ 
   a_{m1} & \ldots & a_{mm}
   \end{array}\right],\quad
   \boldsymbol{B}\ =\ 
   \left[\begin{array}{ccc} 
   b_{11} & \ldots & b_{1p} \\ 
   \ldots & \ldots & \ldots \\ 
   b_{p1} & \ldots & b_{pp}
   \end{array}\right],\quad
   \boldsymbol{x}\ =\ 
   \left[\begin{array}{c}
   x_1 \\ \ldots \\ x_m
   \end{array}\right],\quad
   \boldsymbol{y}\ =\ 
   \left[\begin{array}{c}
   y_1 \\ \ldots \\ y_p
   \end{array}\right]:

.. math::
   :label: mixed-product-2
   
   (\boldsymbol{A}\otimes\boldsymbol{B})
   (\boldsymbol{x}\otimes\boldsymbol{y})\ =\ 
   \boldsymbol{A}\boldsymbol{x}\otimes\boldsymbol{B}\boldsymbol{y}.
   
Wzór :eq:`mixed-product-2` ma zastosowanie przy opisie 
układu kwantowego złożonego z dwóch podukładów.

**3.)** :math:`\,` Jeżeli 
:math:`\ \boldsymbol{A}\,=\,[a_{ij}]_{m\times m}\in M_m(K),\   
\boldsymbol{B}\,=\,[b_{ij}]_{n\times n}\in M_n(K),\ ` to

*i*.) :math:`\quad\text{Tr}\ (\boldsymbol{A}\otimes\boldsymbol{B})\ =\ 
\text{Tr}\,\boldsymbol{A}\ \cdot\ \text{Tr}\,\boldsymbol{B}.`

*ii*.) :math:`\quad\det{(\boldsymbol{A}\otimes\boldsymbol{B})}\ =\ 
(\det{\boldsymbol{A}})^n\ \cdot\ (\det{\boldsymbol{B}})^m.`

*iii*.) :math:`\ \ ` Jeżeli dodatkowo :math:`\ \det{\boldsymbol{A}}\neq 0,\ `
:math:`\ \det{\boldsymbol{B}}\neq 0,\quad` to
:math:`\quad (\boldsymbol{A}\otimes\boldsymbol{B})^{-1}\ =\ \,
\boldsymbol{A}^{-1}\otimes\,\boldsymbol{B}^{-1}.`

**Dowód.**

.. math:
   
   \blacktriangleright\quad
   \text{Tr}\ (\boldsymbol{A}\otimes\boldsymbol{B})\ =\ 
   \text{Tr}\,\boldsymbol{A}\ \cdot\ \text{Tr}\,\boldsymbol{B}.

.. math:
   
   \begin{array}{lll}
   i.) \quad\text{Tr}\ (\boldsymbol{A}\otimes\boldsymbol{B}) &
   = \ \ \displaystyle\sum_{i=1}^m\displaystyle\sum_{j=1}^n\ 
   (\boldsymbol{A}\otimes\boldsymbol{B})_{\ |\ ij,\,ij}\ \ = & \\
   & = \ \ \displaystyle\sum_{i=1}^m
   \displaystyle\sum_{j=1}^n\ a_{ii}\ b_{jj}\ \ = & \\
   & = \ \ \left(\displaystyle\sum_{i=1}^m a_{ii}\right)\ 
   \left(\displaystyle\sum_{j=1}^n b_{jj}\right)\ \ = \ \ &
   \text{Tr}\,\boldsymbol{A}\ \cdot\ \text{Tr}\,\boldsymbol{B}.   
   \end{array}

.. math:

   \begin{array}{rl}
   \text{Tr}\ (\boldsymbol{A}\otimes\boldsymbol{B}) & 
   =\ \ \displaystyle\sum_{i=1}^m\sum_{j=1}^n\ 
   (\boldsymbol{A}\otimes\boldsymbol{B})_{\ |\ ij,\,ij}\ \ =\  
   \displaystyle\sum_{i=1}^m\sum_{j=1}^n\ a_{ii}\ b_{jj}\ \ = \\
   & =\ \ \left(\displaystyle\sum_{i=1}^m a_{ii}\right)\ 
   \left(\displaystyle\sum_{j=1}^n b_{jj}\right)\ \ =\ \ 
   \text{Tr}\,\boldsymbol{A}\ \cdot\ \text{Tr}\,\boldsymbol{B}.
   \end{array}

   \begin{array}{rll}
   \text{bo}\quad\text{Tr}\ (\boldsymbol{A}\otimes\boldsymbol{B}) & 
   =\ \ \displaystyle\sum_{i=1}^m\sum_{j=1}^n\ 
   (\boldsymbol{A}\otimes\boldsymbol{B})_{\ |\ ij,\,ij}\ \ = & \\[16pt]
   & =\ \ \displaystyle\sum_{i=1}^m\sum_{j=1}^n\ a_{ii}\ b_{jj}\ \ = & \\[20pt]
   & =\ \ \left(\displaystyle\sum_{i=1}^m a_{ii}\right)\ 
   \left(\displaystyle\sum_{j=1}^n b_{jj}\right)\ \ =\ \ 
   \text{Tr}\,\boldsymbol{A}\ \cdot\ \text{Tr}\,\boldsymbol{B}.
   \end{array}

.. :math:`\begin{array}{lll}
   i.) \quad\text{Tr}\ (\boldsymbol{A}\otimes\boldsymbol{B}) &
   = \ \ \displaystyle\sum_{i=1}^m\displaystyle\sum_{j=1}^n\ 
   (\boldsymbol{A}\otimes\boldsymbol{B})_{\ |\ ij,\,ij}\ \ = & \\
   & = \ \ \displaystyle\sum_{i=1}^m
   \displaystyle\sum_{j=1}^n\ a_{ii}\ b_{jj}\ \ = & \\
   & = \ \ \left(\displaystyle\sum_{i=1}^m a_{ii}\right)\ 
   \left(\displaystyle\sum_{j=1}^n b_{jj}\right)\ \ = \ \ &
   \text{Tr}\,\boldsymbol{A}\ \cdot\ \text{Tr}\,\boldsymbol{B}.   
   \end{array}`

:math:`\begin{array}{ll}
i.) \quad\text{Tr}\ (\boldsymbol{A}\otimes\boldsymbol{B}) &
= \ \ \displaystyle\sum_{i=1}^m\displaystyle\sum_{j=1}^n\ 
(\boldsymbol{A}\otimes\boldsymbol{B})_{\ |\ ij,\,ij}\ \ = \ \ 
\displaystyle\sum_{i=1}^m \displaystyle\sum_{j=1}^n\ a_{ii}\ b_{jj}\ \ = \\
& = \ \ \left(\displaystyle\sum_{i=1}^m a_{ii}\right)\ 
\left(\displaystyle\sum_{j=1}^n b_{jj}\right)\ \ = \ \ 
\text{Tr}\,\boldsymbol{A}\ \cdot\ \text{Tr}\,\boldsymbol{B}\,.   
\end{array}`

*ii*.) :math:`\,` Korzystamy ze wzoru :eq:`mixed-product`
oraz z uwag do punktu 0.) niniejszej dyskusji:

.. math::
   
   \boldsymbol{A}\otimes\boldsymbol{B}\ =\ 
   (\boldsymbol{A}\,\boldsymbol{I}_m)\otimes
   (\boldsymbol{I}_n\,\boldsymbol{B})\ =\ 
   (\boldsymbol{A}\otimes\boldsymbol{I}_n)\,
   (\boldsymbol{I}_m\otimes\boldsymbol{B})\,;
   
   \boldsymbol{A}\otimes\boldsymbol{I}_n\ \, = \ \,
   \boldsymbol{P}\ (\boldsymbol{I}_n\otimes
   \boldsymbol{A})\,\boldsymbol{P}^{-1}.

Tutaj :math:`\ \boldsymbol{I}_m\ ` oraz   :math:`\ \boldsymbol{I}_n\ `
są macierzami jednostkowymi stopnia :math:`\,m\,` oraz :math:`\,n,\ ` 
a :math:`\ \boldsymbol{P}\ ` jest pewną macierzą permutacji.
Na podstawie twierdzenia o wyznaczniku iloczynu macierzy mamy więc

.. math:
   
   \det{(\boldsymbol{A}\otimes\boldsymbol{B})}\ =\ 
   \det{(\boldsymbol{A}\otimes\boldsymbol{I}_n)}\,\cdot\,
   \det{(\boldsymbol{I}_m\otimes\boldsymbol{B})},
   
   \det{(\boldsymbol{A}\otimes\boldsymbol{I}_n)}\ =\ 
   \det{\left(\boldsymbol{P}^{-1}(\boldsymbol{I}_n\otimes\boldsymbol{A})\,
   \boldsymbol{P}\right)}\ =\ 
   \det{(\boldsymbol{P}^{-1})}\cdot\,\
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\,\cdot\,
   \det{\boldsymbol{P}}\ =

   =\ 
   (\det{\boldsymbol{P}})^{-1}\cdot\,\
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\,\cdot\,
   \det{\boldsymbol{P}}\ =\ 
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\,.

.. math::
   
   \det{(\boldsymbol{A}\otimes\boldsymbol{B})}\ =\ 
   \det{(\boldsymbol{A}\otimes\boldsymbol{I}_n)}\,\cdot\,
   \det{(\boldsymbol{I}_m\otimes\boldsymbol{B})},
   
   \begin{array}{lll}
   \det{(\boldsymbol{A}\otimes\boldsymbol{I}_n)} & 
   =\ \ \det{\left[\,\boldsymbol{P}\,
   (\boldsymbol{I}_n\otimes\boldsymbol{A})\,
   \boldsymbol{P}^{-1}\right]}\ \ = & \\
   & =\ \ \det{\boldsymbol{P}}\,\cdot\,
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\,\cdot\,
   \det{(\boldsymbol{P}^{-1})}\ \ = & \\
   & =\ \ \det{\boldsymbol{P}}\,\cdot\,\
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\,\cdot\,
   (\det{\boldsymbol{P}})^{-1}\ \ = & 
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\,.
   \end{array}

Tak więc wyznacznik iloczynu prostego dwóch macierzy wyraża się wzorem

.. math::
   :label: det_AxB
   
   \qquad\det{(\boldsymbol{A}\otimes\boldsymbol{B})}\ =\ 
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\,\cdot\,
   \det{(\boldsymbol{I}_m\otimes\boldsymbol{B})}\,.

Macierze :math:`\ \boldsymbol{I}_n\otimes\boldsymbol{A}\ ` oraz
:math:`\ \boldsymbol{I}_m\otimes\boldsymbol{B}\ ` są macierzami
blokowo-diagonalnymi:

.. math::
   
   \boldsymbol{I}_n\otimes\boldsymbol{A}\ =\ 
   \underbrace{
   \left[\begin{array}{cccc}
   \boldsymbol{A} & \boldsymbol{0} & \cdots & \boldsymbol{0} \\
   \boldsymbol{0} & \boldsymbol{A} & \cdots & \boldsymbol{0} \\
   \cdots & \cdots & \cdots & \cdots \\
   \boldsymbol{0} & \boldsymbol{0} & \cdots & \boldsymbol{A}
   \end{array}\right]}_{n\ \text{bloków}}\,,
   \qquad
   \boldsymbol{I}_m\otimes\boldsymbol{B}\ =\ 
   \underbrace{
   \left[\begin{array}{cccc}
   \boldsymbol{B} & \boldsymbol{0} & \cdots & \boldsymbol{0} \\
   \boldsymbol{0} & \boldsymbol{B} & \cdots & \boldsymbol{0} \\
   \cdots & \cdots & \cdots & \cdots \\
   \boldsymbol{0} & \boldsymbol{0} & \cdots & \boldsymbol{B}
   \end{array}\right]}_{m\ \text{bloków}} \,,

których wyznaczniki dane są przez

.. math::
   :label: I_AB

   \begin{array}{ll}
   \det{(\boldsymbol{I}_n\otimes\boldsymbol{A})}\ =\ 
   (\det{\boldsymbol{A}})^n \,, & \qquad
   \det{(\boldsymbol{I}_m\otimes\boldsymbol{B})}\ =\ 
   (\det{\boldsymbol{B}})^m\,.
   \end{array}

Podstawienie wyników :eq:`I_AB` do :eq:`det_AxB` daje relację: 
:math:`\ \det{(\boldsymbol{A}\otimes\boldsymbol{B})}\,=\,
(\det{\boldsymbol{A}})^n\,\cdot\,(\det{\boldsymbol{B}})^m,\ `
którą należało udowodnić.
e
*iii*.) :math:`\,` 
Iloczyn prosty dwóch macierzy odwracalnych jest macierzą odwracalną:

.. math::
   
   \left(\ \det{\boldsymbol{A}}\neq 0\,,\ \det{\boldsymbol{B}}\neq 0\ \right)
   \quad\Rightarrow\quad
   \det{(\boldsymbol{A}\otimes\boldsymbol{B})}\ \equiv\ 
   (\det{\boldsymbol{A}})^n\,\cdot\,(\det{\boldsymbol{B}})^m\ \neq\ 0\,.

Ponadto, korzystając ponownie ze wzoru :eq:`mixed-product`, można zapisać

.. math::
   
   (\boldsymbol{A}\otimes\boldsymbol{B})\,
   (\boldsymbol{A}^{-1}\otimes\,\boldsymbol{B}^{-1})\ =\ 
   (\boldsymbol{A}\boldsymbol{A}^{-1})\otimes
   (\boldsymbol{B}\boldsymbol{B}^{-1})\ =\ 
   \boldsymbol{I}_m\otimes\boldsymbol{I}_n\ =\ 
   \boldsymbol{I}_{mn}\,,
   
   (\boldsymbol{A}^{-1}\otimes\,\boldsymbol{B}^{-1})\,
   (\boldsymbol{A}\otimes\boldsymbol{B})\ =\ 
   (\boldsymbol{A}^{-1}\boldsymbol{A})\otimes
   (\boldsymbol{B}^{-1}\boldsymbol{B})\ =\ 
   \boldsymbol{I}_m\otimes\boldsymbol{I}_n\ =\ 
   \boldsymbol{I}_{mn}\,,

co oznacza, że: :math:`\quad (\boldsymbol{A}\otimes\boldsymbol{B})^{-1}\,=\ 
\boldsymbol{A}^{-1}\otimes\,\boldsymbol{B}^{-1},\quad` co należało udowodnić. 

**4.)** :math:`\,` Jeżeli 
:math:`\ \boldsymbol{A}\,=\,[a_{ij}]_{m\times n}\in M_{m\times n}(K),\   
\boldsymbol{B}\,=\,[b_{ij}]_{p\times q}\in M_{p\times q}(K),\ ` to

*i*.) :math:`\quad(\boldsymbol{A}\otimes\boldsymbol{B})^T\ =\ 
\boldsymbol{A}^T\ \otimes\ \boldsymbol{B}^{\,T}.`

Dla macierzy zespolonych (:math:`K=C`) zachodzą dodatkowo związki:

*ii*.) :math:`\quad(\boldsymbol{A}\otimes\boldsymbol{B})^*\ =\ 
\boldsymbol{A}^*\otimes\ \boldsymbol{B}^*.`

*iii*.) :math:`\quad(\boldsymbol{A}\otimes\boldsymbol{B})^+\ =\ 
\boldsymbol{A}^+\otimes\ \boldsymbol{B}^+.`

**Dowód.**

*i*.) :math:`\,` 
Macierze po obydwu stronach równości mają 
te same rozmiary oraz te same elementy:

a.) :math:`\ ` porównanie rozmiarów macierzy:

.. math::
   
   \begin{array}{lcr}
   \begin{array}{rr}
   \boldsymbol{A}                          \ : & m\times n   \\[4pt]
   \boldsymbol{B}                          \ : & p\times q   \\[4pt]
   \boldsymbol{A}\otimes\boldsymbol{B}     \ : & mp\times nq \\[4pt]
   (\boldsymbol{A}\otimes\boldsymbol{B})^T \ : & nq\times mp
   \end{array} 
   & 
   \begin{array}{c}
   \qquad
   \end{array}
   &
   \begin{array}{rr}
   \boldsymbol{A}^T                        \ : & n\times m \\[4pt]
   \boldsymbol{B}^T                        \ : & q\times p \\[4pt]
   \boldsymbol{A}^T\otimes\boldsymbol{B}^T \ : & nq\times mp 
   \end{array}
   \end{array}

b.) :math:`\ ` porównanie odpowiednich elementów:

.. math::
   
   \begin{array}{l}
   (\boldsymbol{A}\otimes\boldsymbol{B})^T_{\ |\ ij,\,kl}\ \ =\ \ 
   (\boldsymbol{A}\otimes\boldsymbol{B})_{\ |\ kl,\,ij}\ \ =\ \ 
   a_{ki}\,b_{lj}
   \\[4pt]   
   (\boldsymbol{A}^T\otimes\boldsymbol{B}^T)_{\ |\ ij,\,kl}\ \ =\ \ 
   a^T_{ik}\,b^T_{jl}\ =\ a_{ki}\,b_{lj}
   \end{array}
   \\[8pt]
   \begin{array}{ll}
   \text{gdzie} &
   \begin{array}{ll}
   i=1,2,\ldots,n; & j=1,2,\ldots,q; \\
   k=1,2,\ldots,m; & l=1,2,\ldots,p.
   \end{array}
   \end{array}

A zatem transpozycja iloczynu prostego dwóch macierzy równa się 
iloczynowi prostemu :math:`\\` macierzy transponowanych 
(z zachowaniem kolejności czynników).

*ii*.) :math:`\,`
Macierze :math:`\ (\boldsymbol{A}\otimes\boldsymbol{B})^*\ ` 
oraz :math:`\ \boldsymbol{A}^*\otimes\boldsymbol{B}^*\ ` 
mają te same rozmiary, :math:`\ ` a ponadto

.. math::
   
   (\boldsymbol{A}\otimes\boldsymbol{B})^{*}_{\ |\ ij,\,kl}\ \ =\ \ 
   (a_{ik}\,b_{jl})^*\,=\ \,a^*_{ik}\ b^*_{jl}\ \,=\ \,
   (\boldsymbol{A}^*\otimes\,\boldsymbol{B}^*)_{\ |\ ij,\,kl}\,,
   \\[8pt]
   \begin{array}{ll}
   \text{gdzie} &
   \begin{array}{ll}
   i=1,2,\ldots,m; & j=1,2,\ldots,p; \\
   k=1,2,\ldots,n; & l=1,2,\ldots,q.
   \end{array}
   \end{array}

Tak więc sprzężenie zespolone iloczynu prostego dwóch macierzy równa się 
iloczynowi :math:`\\` prostemu macierzy sprzężonych
(z zachowaniem kolejności czynników).

*iii*.) :math:`\,`
Sprzężenie hermitowskie macierzy jest złożeniem transpozycji 
i sprzężenia zespolonego:

.. math::
   
   (\boldsymbol{A}\otimes\boldsymbol{B})^+\,=\ 
   \left[\,(\boldsymbol{A}\otimes\boldsymbol{B})^T\right]^* =\ \,
   \left(\boldsymbol{A}^T\otimes\,\boldsymbol{B}^T\right)^*\ =\ \,
   (\boldsymbol{A}^T)^*\otimes\,(\boldsymbol{B}^T)^*\ =\ \,
   \boldsymbol{A}^+\otimes\,\boldsymbol{B}^+.
 

Iloczyn prosty jako macierz przekształcenia liniowego
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. Zbiór :math:`\ M_{m\times n}(K)\ ` macierzy prostokątnych o :math:`\,m\ `
   wierszach i :math:`\,n\ ` kolumnach nad ciałem :math:`\,K\ ` jest 
   przestrzenią wektorową nad tym ciałem ze względu na dodawanie macierzy
   i mnożenie ich przez skalary z :math:`\,K.`

Ze względu na dodawanie macierzy i mnożenie ich przez skalary, 
zbiór :math:`\ M_{m\times n}(K)\ ` macierzy prostokątnych o :math:`\,m\ `
wierszach i :math:`\,n\ ` kolumnach nad ciałem :math:`\,K\ ` jest 
:math:`\ mn`-wymiarową przestrzenią wektorową nad tym ciałem. 
Naturalną (dalej: kanoniczną) bazą jest układ macierzy

.. math::
   
   \mathcal{E}_{m\times n}\ =\ 
   \left(\ \boldsymbol{E}_{11},\ \boldsymbol{E}_{12},\ 
   \ldots,\ \boldsymbol{E}_{1n},\ \ 
   \boldsymbol{E}_{21},\ \boldsymbol{E}_{22},\ 
   \ldots,\ \boldsymbol{E}_{2n},\ \ 
   \ldots,\ \ \boldsymbol{E}_{m1},\ \boldsymbol{E}_{m2},\ 
   \ldots,\ \boldsymbol{E}_{mn}\,\right)

   \left(\boldsymbol{E}_{ij}\right)_{\,|\,kl}\ =\ \ 
   \delta_{ik}\ \delta_{jl}\,,
   \qquad
   \begin{array}{l}
   i,k=1,2,\ldots,m, \\
   j,l=1,2,\ldots,n.
   \end{array}

Każda macierz :math:`\ \boldsymbol{A} \in M_{m\times n}(K)\ ` 
może być teraz przedstawiona w bazie :math:`\ \mathcal{E}_{m\times n}:`

.. math::
   
   \boldsymbol{A}\ =\ [a_{ij}]_{m\times n}\ =\ \,
   \displaystyle\sum_{i=1}^m \displaystyle\sum_{j=1}^n\ 
   a_{ij}\ \boldsymbol{E}_{ij}\,.

Niech :math:`\ \boldsymbol{\Lambda}^{mn}(\boldsymbol{A})\ ` 
oznacza wektor kolumnowy utworzony przez kolejne wiersze macierzy 
:math:`\ \boldsymbol{A}:`

.. math::
   
   \boldsymbol{\Lambda}^{mn}(\boldsymbol{A})\ :\,=\ 
   \left[\ a_{11}\ a_{12}\ \ldots\ a_{1n}\ \ a_{21}\ a_{22}\ \ldots\ a_{2n}\ \ 
   \ldots\ \ a_{m1}\ a_{m2}\ \ldots\ a_{mn}\,\right]^T\ 
   \in\ K^{mn}.

Tak zdefiniowany wektor :math:`\ \boldsymbol{\Lambda}^{mn}(\boldsymbol{A})\ `
jest kolumną współrzędnych macierzy :math:`\ \boldsymbol{A}\ ` w bazie 
:math:`\ \mathcal{E}_{m\times n}\,.`

**Przykład.** :math:`\\` 
W przestrzeni :math:`\ M_{2\times 3}(Q)\ ` bazą kanoniczną jest
:math:`\ \mathcal{E}_{2\times 3}\ =\ 
\left(\,\boldsymbol{E}_{11},\ \boldsymbol{E}_{12},\ \boldsymbol{E}_{13},\ 
\boldsymbol{E}_{21},\ \boldsymbol{E}_{22},\ \boldsymbol{E}_{23}\,\right)`:

.. math::
   
   \begin{array}{lll}
   \boldsymbol{E}_{11}\ =\ 
   \left[\begin{array}{ccc} 
   1 & 0 & 0 \\ 0 & 0 & 0
   \end{array}\right], 
   &
   \boldsymbol{E}_{12}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 1 & 0 \\ 0 & 0 & 0
   \end{array}\right],
   &
   \boldsymbol{E}_{13}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 0 & 1 \\ 0 & 0 & 0
   \end{array}\right]
   \\[12pt]
   \boldsymbol{E}_{21}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 0 & 0 \\ 1 & 0 & 0
   \end{array}\right],
   &
   \boldsymbol{E}_{22}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 0 & 0 \\ 0 & 1 & 0
   \end{array}\right],
   &
   \boldsymbol{E}_{23}\ =\ 
   \left[\begin{array}{ccc} 
   0 & 0 & 0 \\ 0 & 0 & 1
   \end{array}\right]
   \end{array}

Dla macierzy :math:`\ \boldsymbol{A}\ =\ 
\left[\begin{array}{ccc} 1 & 2 & 3 \\ 4 & 5 & 6 \end{array}\right]\ `
wektor 
:math:`\ \boldsymbol{\Lambda}^{23}(\boldsymbol{A})\ =\ 
\left[\begin{array}{c} 1 \\ 2 \\ 3 \\ 4 \\ 5 \\ 6 \end{array}\right].`

Niech będą dane macierze 
:math:`\ \boldsymbol{A} = [a_{ij}]_{m\times n}\in M_{m\times n}(K)\ ` oraz
:math:`\ \boldsymbol{B} = [b_{ij}]_{p\times q}\in M_{p\times q}(K).\ ` 
:math:`\\`
Wtedy, :math:`\,` jeżeli 
:math:`\ \boldsymbol{G} = [g_{ij}]_{n\times q}\in M_{n\times q}(K),\ ` to
:math:`\ \boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T\in M_{m\times p}(K).`

Odwołując się do własności iloczynu macierzowego można łatwo uzasadnić,
że odwzorowanie

.. math::
   :label: homo
   
   F_{AB}\,:\qquad 
   M_{n\times q}(K)\ni\boldsymbol{G}\ \ \mapsto\ \ F_{AB}(\boldsymbol{G}) :\,=
   \boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T\in M_{m\times p}(K)

jest liniowe, czyli jest homomorfizmem przestrzeni wektorowych:

.. math::
   
   F_{AB}\ \in\ \text{Hom}\left(M_{n\times q}(K),\,M_{m\times p}(K)\right).

Przyjmując oznaczenie :math:`\boldsymbol{H}\ =\ [h_{ij}]_{m\times p}\ =\ 
\boldsymbol{A}\,\boldsymbol{G}\,\boldsymbol{B}^T\ ` otrzymujemy

.. math::
   
   h_{ij}
   \ =\ \displaystyle\sum_{v=1}^n\sum_{w=1}^q a_{iv}\ g_{vw}\ b^T_{wj}
   \ =\ \displaystyle\sum_{v=1}^n\sum_{w=1}^q (a_{iv}\,b_{jw})\ g_{vw}
   \ =\ \displaystyle\sum_{v=1}^n\sum_{w=1}^q 
   (\boldsymbol{A}\otimes\boldsymbol{B})_{\,|\,ij,\,vw}\ g_{vw}
   
   \text{gdzie}\quad i=1,2,\ldots,m;\ j=1,2,\ldots,p.

A zatem dla dowolnych macierzy 
:math:`\ \boldsymbol{G}\in M_{n\times q}(K),\,`
:math:`\,\boldsymbol{H}\in M_{m\times p}(K):`

.. math::
   
   \boldsymbol{H}\ =\ F_{AB}(\boldsymbol{G})
   \quad\Leftrightarrow\quad
   \boldsymbol{\Lambda}^{mp}(\boldsymbol{H})\ \,=\ \,
   (\boldsymbol{A}\otimes\boldsymbol{B})\ \cdot\ 
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G}),

co oznacza, że iloczyn prosty :math:`\ \boldsymbol{A}\otimes\boldsymbol{B}\ `
jest macierzą homomorfizmu :math:`\ F_{AB}\ ` danego przez :eq:`homo`
w bazach kanonicznych 
:math:`\ \mathcal{E}_{n\times q}\ ` i :math:`\ \mathcal{E}_{m\times p}\ `
przestrzeni :math:`\ M_{n\times q}(K)\ ` i :math:`\ M_{m\times p}(K).`
   
Wykorzystamy teraz wyprowadzone zależności do ponownego udowodnienia
niektórych własności iloczynu prostego macierzy.

Stwierdziliśmy, że jeżeli dane są macierze 
:math:`\ \boldsymbol{A}\in M_{m\times n}(K)\ ` oraz 
:math:`\ \boldsymbol{B}\in M_{p\times q}(K),\ ` :math:`\\` 
to dla dowolnej macierzy :math:`\ \boldsymbol{G}\in M_{n\times q}(K):`

.. math::
   :label: main
   
   \blacktriangleright\quad
   (\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\ \,=\ \,
   \boldsymbol{\Lambda}^{mp}
   (\boldsymbol{A}\boldsymbol{G}\boldsymbol{B}^T).

Podstawiając w :eq:`main` 
:math:`\ \boldsymbol{A}\to\boldsymbol{A}_1 + \boldsymbol{A}_2\,,\ ` gdzie 
:math:`\ \boldsymbol{A}_1,\ \boldsymbol{A}_2 \in M_{m\times n}(K),\ `
otrzymamy

.. math::
   
   \begin{array}{ll}
   \left[\,(\boldsymbol{A}_1 + \boldsymbol{A}_2)\otimes\boldsymbol{B}\,\right]
   \,\cdot\,\boldsymbol{\Lambda}^{nq}(\boldsymbol{G}) & 
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,(\boldsymbol{A}_1 + \boldsymbol{A}_2)\ 
   \boldsymbol{G}\,\boldsymbol{B}^T\,\right]\ =
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}_1\,\boldsymbol{G}\,\boldsymbol{B}^T + \,
   \boldsymbol{A}_2\,\boldsymbol{G}\,\boldsymbol{B}^T\right)\ =
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}_1\,\boldsymbol{G}\,\boldsymbol{B}^T\right)\ +\ 
   \boldsymbol{\Lambda}^{mp}
   \left(\boldsymbol{A}_2\,\boldsymbol{G}\,\boldsymbol{B}^T\right)\ =
   \\[6pt] &
   =\ \ (\boldsymbol{A}_1\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\ +\ 
   (\boldsymbol{A}_2\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\ =
   \\[6pt] &
   =\ \ \left[\,(\boldsymbol{A}_1\otimes\boldsymbol{B})\ +\ 
   (\boldsymbol{A}_2\otimes\boldsymbol{B})\,\right]\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})
   \end{array}

dla dowolnej macierzy :math:`\ \boldsymbol{G}\in M_{n\times q}(K).\ `
Podstawiając w miejsce :math:`\ \boldsymbol{G}\ ` kolejne macierze 
bazy kanonicznej: :math:`\ \boldsymbol{G} = \boldsymbol{E}_{11},\ 
\boldsymbol{E}_{12},\ \ldots,\ \boldsymbol{E}_{nq}\,,\ ` stwierdzamy
równość odpowiednich kolumn macierzy 
:math:`\ (\boldsymbol{A}_1 + \boldsymbol{A}_2)\otimes\boldsymbol{B}\ `
oraz :math:`\ (\boldsymbol{A}_1\otimes\boldsymbol{B})\ +\ 
(\boldsymbol{A}_2\otimes\boldsymbol{B})\,,\ ` co oznacza równość
samych macierzy:

.. math::
   
   (\boldsymbol{A}_1 + \boldsymbol{A}_2)\otimes\boldsymbol{B}\ \,=\ \,
   (\boldsymbol{A}_1\otimes\boldsymbol{B})\ +\ 
   (\boldsymbol{A}_2\otimes\boldsymbol{B})\,.

Podobnie przebiega dowód rozdzielności iloczynu prostego względem
dodawania w drugim czynniku macierzowym oraz dowód jednorodności:

.. math::
   
   \boldsymbol{A}\otimes(\boldsymbol{B}_1\ +\ \boldsymbol{B}_2)\ \,=\ \,
   (\boldsymbol{A}\otimes\boldsymbol{B}_1)\ +\ 
   (\boldsymbol{A}\otimes\boldsymbol{B}_2)\,,

   (\gamma\,\boldsymbol{A})\otimes\boldsymbol{B}\ =\
   \boldsymbol{A}\otimes(\gamma\,\boldsymbol{B})\ =\ 
   \gamma\ (\boldsymbol{A}\otimes\boldsymbol{B}),\quad\gamma\in K.
   
Dla udowodnienia wzoru :eq:`mixed-product` podstawiamy w równaniu :eq:`main` :

.. math::
   
   \begin{array}{lr}
   \boldsymbol{A}\to\boldsymbol{A}\,\boldsymbol{C},\ \ &
   \begin{array}{r}
   \boldsymbol{A}\ :\ m \times r \\
   \boldsymbol{C}\ :\ r \times n
   \end{array};
   \end{array}
   \qquad
   \begin{array}{ll}
   \boldsymbol{B}\to\boldsymbol{B}\,\boldsymbol{D},\ \ &
   \begin{array}{l}
   \boldsymbol{B}\ :\ p \times s \\
   \boldsymbol{D}\ :\ s \times q
   \end{array}:
   \end{array}
   \\[8pt]
   \begin{array}{ll}
   \left[\,(\boldsymbol{A}\boldsymbol{C})\otimes
   (\boldsymbol{B}\boldsymbol{D})\,\right]\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G}) & 
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,(\boldsymbol{A}\boldsymbol{C})\ \boldsymbol{G}\ 
   (\boldsymbol{B}\boldsymbol{D})^T\,\right]\ \ =\ 
   \\[6pt] &
   =\ \ \boldsymbol{\Lambda}^{mp}
   \left[\,\boldsymbol{A}\ 
   (\boldsymbol{C}\boldsymbol{G}\boldsymbol{D}^T)\ 
   \boldsymbol{B}^T\,\right]\ \ =
   \\[6pt] &
   =\ \ (\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
   \boldsymbol{\Lambda}^{rs}
   (\boldsymbol{C}\boldsymbol{G}\boldsymbol{D}^T)\ \ =
   \\[6pt] &
   =\ \ (\boldsymbol{A}\otimes\boldsymbol{B})\,\cdot\,
   \left[\,(\boldsymbol{C}\otimes\boldsymbol{D})\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G})\,\right]\ \ =
   \\[6pt] &
   =\ \ \left[\,(\boldsymbol{A}\otimes\boldsymbol{B})\cdot
   (\boldsymbol{C}\otimes\boldsymbol{D})\,\right]\,\cdot\,
   \boldsymbol{\Lambda}^{nq}(\boldsymbol{G}).
   \end{array}

Ponieważ macierz :math:`\ \boldsymbol{G}\in M_{n\times q}(K)\ `
jest dowolna, wynika stąd równość macierzowa

.. math::
   
   (\boldsymbol{A}\boldsymbol{C})\otimes
   (\boldsymbol{B}\boldsymbol{D})\ =\ 
   (\boldsymbol{A}\otimes\boldsymbol{B})\ 
   (\boldsymbol{C}\otimes\boldsymbol{D})\,,

którą należało udowodnić.

.. [1] H. V. Henderson; S. R. Searle (1980). "The vec-permutation matrix, 
   the vec operator and Kronecker products: a review". 
   LINEAR AND MULTILINEAR ALGEBRA. 9 (4): 271–288.
   https://dx.doi.org/10.1080%2F03081088108817379















