Diagonalization by a Similarity Transformation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. admonition:: Definicja.
   
   Macierz :math:`\ \boldsymbol{A}\in M_n(C)\ ` może być zdiagonalizowana 
   przekształceniem podobieństwa, gdy istnieje odwracalna macierz
   :math:`\ \boldsymbol{P}\in M_n(C)\ ` taka, że
   
   .. math::
      :label: similarity
      
      \boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P}\ =\ \boldsymbol{D}
   
   gdzie :math:`\ \boldsymbol{D}\in M_n(C)\ ` jest macierzą diagonalną.
   
   Wówczas :math:`\ \boldsymbol{P}\ ` jest macierzą diagonalizującą
   macierz :math:`\ \boldsymbol{A}.`

**Lemat.** 

Niech będą dana macierze :math:`\ \boldsymbol{A},\,\boldsymbol{P}\in M_n(C).`
Kolumny 
:math:`\ \boldsymbol{X}_1,\ \boldsymbol{X}_2,\ldots, \boldsymbol{X}_n\ `
macierzy :math:`\ \boldsymbol{P}\ ` są wektorami własnymi
macierzy :math:`\ \boldsymbol{A}:`

.. math::
   :label: eigen
   
   \boldsymbol{A}\,\boldsymbol{X}_1\,=\,\lambda_1\,\boldsymbol{X}_1,\quad
   \boldsymbol{A}\,\boldsymbol{X}_2\,=\,\lambda_2\,\boldsymbol{X}_2,\quad
   \ldots\quad
   \boldsymbol{A}\,\boldsymbol{X}_n\,=\,\lambda_n\,\boldsymbol{X}_n

wtedy i tylko wtedy, gdy

.. math::
   :label: products
   
   \boldsymbol{A}\,\boldsymbol{P}\,=\,\boldsymbol{P}\,\boldsymbol{D}

gdzie :math:`\ \boldsymbol{D}\,=\,
\text{diag}(\lambda_1,\lambda_2,\ldots,\lambda_n)\,.`

Rzeczywiście, według kolumnowej reguły mnożenia macierzowego:

.. math::
   
   \begin{array}{rl}
   \boldsymbol{A}\,\boldsymbol{P} \!\! & 
   =\ \ \boldsymbol{A}\ \,[\ \boldsymbol{X}_1\,|\ \boldsymbol{X}_2\,|
   \ \ldots\,|\ \boldsymbol{X}_n\,]\ \ = \\[6pt]
   & =\ \ [\ \boldsymbol{A}\,\boldsymbol{X}_1\,|\ 
   \boldsymbol{A}\,\boldsymbol{X}_2\,|\ \ldots\,|\ 
   \boldsymbol{A}\,\boldsymbol{X}_n\,]
   \\[10pt]
   \boldsymbol{P}\,\boldsymbol{D} \!\! & 
   =\ \ [\ \lambda_1\,\boldsymbol{X}_1\,|\ 
   \lambda_2\,\boldsymbol{X}_2\,|\  \ldots\,|\ 
   \lambda_n\,\boldsymbol{X}_n\,]
   \end{array}

.. .. math::
   
   \boldsymbol{A}\boldsymbol{P}\ =\ 
   \boldsymbol{A}\ [\ \boldsymbol{X}_1\,|\ \boldsymbol{X}_2\,|
   \ \ldots\,|\ \boldsymbol{X}_n\,]\ =\ 
   [\ \boldsymbol{A}\,\boldsymbol{X}_1\,|\ 
   \boldsymbol{A}\,\boldsymbol{X}_2\,|\ \ldots\,|\ 
   \boldsymbol{A}\,\boldsymbol{X}_n\,]
   
   \boldsymbol{P}\boldsymbol{D}\ =\ 
   [\ \lambda_1\,\boldsymbol{X}_1\,|\ 
   \lambda_2\,\boldsymbol{X}_2\,|\  \ldots\,|\ 
   \lambda_n\,\boldsymbol{X}_n\,]

wobec czego warunki :eq:`eigen` i :eq:`products` są równoważne.

**Twierdzenie 7.**

Macierz :math:`\ \boldsymbol{A}\ ` może być zdiagonalizowana przekształceniem
podobieństwa :eq:`similarity` wtedy i tylko wtedy, :math:`\ ` gdy w przestrzeni
:math:`\,C^n\,` istnieje baza :math:`\,\mathcal{B} = (\boldsymbol{X}_1,\, 
\boldsymbol{X}_2,\,\ldots,\,\boldsymbol{X}_n),\ ` 
złożona z wektorów własnych macierzy :math:`\ \boldsymbol{A}:`

.. math::
   
   \boldsymbol{A}\,\boldsymbol{X}_1\,=\,\lambda_1\,\boldsymbol{X}_1,\quad
   \boldsymbol{A}\,\boldsymbol{X}_2\,=\,\lambda_2\,\boldsymbol{X}_2,\quad
   \ldots,\quad
   \boldsymbol{A}\,\boldsymbol{X}_n\,=\,\lambda_n\,\boldsymbol{X}_n\,,\quad
   \lambda_1,\lambda_2,\ldots,\lambda_n\in C\,.

Wówczas macierzą diagonalizującą jest macierz :math:`\ \boldsymbol{P}\,=\,
[\ \boldsymbol{X}_1\,|\,\boldsymbol{X}_2\,|\,\ldots\,|\,\boldsymbol{X}_n\ ],\ `
której kolumny są wektorami bazy :math:`\,\mathcal{B}.`

.. złożona kolumnowo z wektorów bazy :math:`\ \mathcal{B}.`

**Dowód.**

Macierz :math:`\ \boldsymbol{A}\ ` może być zdiagonalizowana 
poprzez przekształcenie podobieństwa, gdy
istnieje odwracalna macierz :math:`\ \boldsymbol{P}\,\equiv\,
[\ \boldsymbol{X}_1\,|\ \boldsymbol{X}_2\,|\ \ldots\,|\ \boldsymbol{X}_n\,],\ `
taka, że

.. math::
   
   \boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P}\ =\ \boldsymbol{D}
   
gdzie macierz :math:`\ \boldsymbol{D}\ ` jest diagonalna: 
:math:`\ \boldsymbol{D}\,=\,\text{diag}(\lambda_1,\lambda_2,\ldots,\lambda_n).\ `
Jest to równoważne warunkom

.. math::
   
   \boldsymbol{A}\,\boldsymbol{P}\,=\,\boldsymbol{P}\,\boldsymbol{D}
   \quad\text{i}\quad \det{\boldsymbol{P}}\neq 0.

Warunek :math:`\ \det{\boldsymbol{P}}\neq 0\ ` oznacza, 
że :math:`\ \mathcal{B} = 
(\boldsymbol{X}_1,\, \boldsymbol{X}_2,\,\ldots,\,\boldsymbol{X}_n)\ `
jest liniowo niezależnym układem wektorów przestrzeni :math:`\ C^n.\ `
Ponadto, na podstawie Lematu:

.. math::
   
   \boldsymbol{A}\,\boldsymbol{X}_1\,=\,\lambda_1\,\boldsymbol{X}_1,\quad
   \boldsymbol{A}\,\boldsymbol{X}_2\,=\,\lambda_2\,\boldsymbol{X}_2,\quad
   \ldots\quad
   \boldsymbol{A}\,\boldsymbol{X}_n\,=\,\lambda_n\,\boldsymbol{X}_n

W :math:`\ n`-wymiarowej przestrzeni wektorowej każdy liniowo niezależny 
układ :math:`\,n\,` wektorów jest bazą. Ponieważ :math:`\ \dim{C^n}=n,\ ` to
:math:`\,\mathcal{B}\ ` jest bazą przestrzeni :math:`\ C^n,\ `
złożoną z wektorów własnych macierzy :math:`\,\boldsymbol{A}.`

Odwrotnie, jeżeli wektory własne :math:`\ \boldsymbol{X}_1,\,\boldsymbol{X}_2,\,
\ldots,\,\boldsymbol{X}_n\ ` macierzy :math:`\,\boldsymbol{A}\in M_n(C)\,`
rozpinają przestrzeń :math:`\,C^n,\ ` to macierz :math:`\,\boldsymbol{P}\,` 
zestawiona kolumnowo z tych wektorów diagonalizuje macierz 
:math:`\,\boldsymbol{A}.`
 
**Komentarze i wnioski.**

**1.)** Każda macierz :math:`\,\boldsymbol{A}\in M_n(C)\,` ma co najmniej 
jedną wartość własną :math:`\,\lambda\,` i odpowiedni wektor własny 
:math:`\,\boldsymbol{X}.\ ` Ponieważ w równaniu :eq:`eigen` wartości
:math:`\,\lambda_i\ ` i :math:`\,` odpowiednie wektory 
:math:`\,\boldsymbol{X}_i\ ` mogą się powtarzać, zawsze istnieje macierz 
:math:`\,\boldsymbol{P},\ ` spełniająca :eq:`products`. 
W szczególności można przyjąć

.. math::
   
   \lambda_1\,=\,\lambda_2=\,\ldots\,\lambda_n\,=\lambda,\quad
   \boldsymbol{X}_1\,=\,\boldsymbol{X}_2\,=\,\ldots\boldsymbol{X}_n\,=\,
   \boldsymbol{X}.

Wtedy :math:`\,\boldsymbol{A}\boldsymbol{P}=
\boldsymbol{P}\boldsymbol{D}=\lambda\,\boldsymbol{P},\ `
ale macierz :math:`\ \boldsymbol{P}\ ` nie jest odwracalna
i nie zachodzi związek :eq:`similarity`.

**2.)** Wzór :math:`\ \boldsymbol{D}\,=\,
\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P}\ ` można interpretować
w terminach transformacji macierzy operatora liniowego przy zmianie bazy.
:math:`\boldsymbol{A}\ ` jest macierzą, w bazie kanonicznej 
:math:`\ \mathcal{E}\,=\,(\boldsymbol{e}_1,\boldsymbol{e}_2,\ldots\,
\boldsymbol{e}_n)\ ` przestrzeni :math:`\,C^n,\ ` operatora liniowego
:math:`F\in \text{End}(C^n)\ ` określonego wzorem 
:math:`\ F(\boldsymbol{x})\,:\,=\,\boldsymbol{A}\boldsymbol{x},\ `
:math:`\,\boldsymbol{x}\in C^n.\ ` Jeżeli wektory własne 
:math:`\ \boldsymbol{X}_1,\boldsymbol{X}_2,\ldots,\boldsymbol{X}_n\ ` 
operatora :math:`\,F\,` są liniowo niezależne, to macierz 
:math:`\ \boldsymbol{P}\,=\,
[\ \boldsymbol{X}_1\,|\,\boldsymbol{X}_2\,|\,\ldots\,|\,\boldsymbol{X}_n\ ]\ ` 
jest macierzą przejścia od bazy kanonicznej
:math:`\,\mathcal{E}\,` do bazy wektorów własnych :math:`\,\mathcal{B}\,=\,
(\boldsymbol{X}_1,\boldsymbol{X}_2,\ldots\,\boldsymbol{X}_n).`

:math:`\boldsymbol{D}\ ` jest więc macierzą operatora :math:`\,F\ ` w bazie 
:math:`\,\mathcal{B}\ ` jego wektorów własnych. Jak należało oczekiwać, 
jest to macierz diagonalna, z wartościami własnymi operatora :math:`\,F\ ` na przekątnej.

**3.)** Wiadomo, że wektory własne operatora liniowego, należące do różnych 
wartości własnych, są liniowo niezależne.

**Wniosek.** Jeżeli macierz :math:`\,\boldsymbol{A}\in M_n(C)\ ` ma 
:math:`\,n\,` różnych wartości własnych, to istnieje transformacja podobieństwa
diagonalizująca tę macierz.

Rzeczywiście, macierz :math:`\,\boldsymbol{P}\,` złożona kolumnowo z wektorów
własnych macierzy :math:`\,\boldsymbol{A}\,` dla tych różnych wartości jest 
nieosobliwa: :math:`\,\det{\boldsymbol{P}}\neq 0,\ ` a więc odwracalna.

**4.)** Wektory własne operatora normalnego, należące do różnych wartości 
własnych, tworzą układ ortogonalny, a po unormowaniu - układ ortonormalny.
Macierz, której kolumny tworzą układ ortonormalny, jest macierzą unitarną.

**Wniosek.** Niech :math:`\,\boldsymbol{A}\in M_n(C)\ ` będzie macierzą 
normalną (np. hermitowską albo unitarną). Jeżeli :math:`\,\boldsymbol{A}\ `
ma :math:`\,n\,` różnych wartości własnych, to istnieje unitarna 
transformacja podobieństwa diagonalizująca tę macierz (macierz diagonalizująca 
:math:`\,\boldsymbol{P}\ ` jest unitarna: 
:math:`\ \boldsymbol{P}^+\boldsymbol{P}=\boldsymbol{I}_n).`
   
**Uwaga.** Warunek istnienia :math:`\,n\,` różnych wartości własnych macierzy
normalnej nie jest konieczny. Można mianowicie udowodnić ogólne

**Twierdzenie 8.**

Macierz :math:`\,\boldsymbol{A}\in M_n(C)\ ` może być sprowadzona do postaci
diagonalnej poprzez unitarną transformację podobieństwa wtedy i tylko wtedy,
gdy jest normalna.

**Zastosowanie do macierzy rzeczywistych.**

Niech :math:`\,\boldsymbol{A}\ ` będzie macierzą rzeczywistą:
:math:`\,\boldsymbol{A}\in M_n(R).\ ` Wtedy
:math:`\,\boldsymbol{A}^+=\boldsymbol{A}^T,\ ` wobec czego

.. math::
   
   \boldsymbol{A}^+=\boldsymbol{A}
   \quad\Leftrightarrow\quad
   \boldsymbol{A}^T=\boldsymbol{A}

(rzeczywista macierz hermitowska jest macierzą symetryczną),

.. math::
   
   \boldsymbol{A}^+\boldsymbol{A}=\boldsymbol{I}_n
   \quad\Leftrightarrow\quad
   \boldsymbol{A}^T\boldsymbol{A}=\boldsymbol{I}_n

(rzeczywista macierz unitarna jest macierzą ortogonalną).

**Twierdzenie 9.**

Każda rzeczywista macierz symetryczna albo ortogonalna może być
zdiagonalizowana poprzez unitarną transformację podobieństwa.

Wartości własne, a więc również wektory własne, 
rzeczywistej macierzy symetrycznej są rzeczywiste.
Unitarna macierz diagonalizująca jest zatem tutaj 
rzeczywistą macierzą ortogonalną.

**Wniosek.** Każda rzeczywista macierz symetryczna może być sprowadzona 
do postaci diagonalnej poprzez rzeczywistą ortogonalną transformację
podobieństwa.

W odróżnieniu od poprzedniego przypadku, wartości własne
rzeczywistej macierzy ortogonalnej (a więc i jej wektory własne)
mogą być zespolone nierzeczywiste. Wtedy unitarna macierz diagonalizująca
będzie również zespolona nierzeczywista.

**Twierdzenie 10.**

Jeżeli macierz :math:`\ \boldsymbol{A}\ ` można zdiagonalizować
przekształceniem podobieństwa, to dla każdej jej wartości własnej
krotność algebraiczna równa się krotności geometrycznej.

**Dowód.** :math:`\ ` 
Jeżeli przekształcenie :math:`\ \boldsymbol{A}\ \rightarrow\ 
\boldsymbol{P}^{-1}\boldsymbol{A}\,\boldsymbol{P}\ \equiv\boldsymbol{D}\ `
diagonalizuje macierz :math:`\ \boldsymbol{A},\ ` 
to :math:`\ \boldsymbol{D}\,=
\text{diag}(\lambda_1,\,\lambda_2,\,\ldots,\,\lambda_k),\ ` gdzie
:math:`\ \lambda_1,\lambda_2,\ldots,\lambda_k\ ` są wartościami własnymi
macierzy :math:`\,\boldsymbol{A}.\ `
Liczba wystąpień danej wartości :math:`\,\lambda_i\,` na przekątnej 
macierzy :math:`\ \boldsymbol{D}\ ` jest jednocześnie
krotnością algebraiczną i krotnością geometryczną tej wartości własnej.





