Definition and Properties of the Tensor Product
-----------------------------------------------

Definition and Examples
~~~~~~~~~~~~~~~~~~~~~~~

Niech będą dane macierze 
:math:`\ \boldsymbol{A}\,=\,[a_{ij}]_{m\times n}\,,\ `
:math:`\ \boldsymbol{B}\,=\,[b_{ij}]_{p\times q}\in M(K).\ `
Iloczyn tensorowy (iloczyn prosty, iloczyn Kroneckera) 
tych macierzy ma w zapisie blokowym postać

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

Properties of the Tensor Product
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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

.. [1] H. V. Henderson; S. R. Searle (1980). "The vec-permutation matrix, 
   the vec operator and Kronecker products: a review". 
   LINEAR AND MULTILINEAR ALGEBRA. 9 (4): 271–288.
   https://dx.doi.org/10.1080%2F03081088108817379



