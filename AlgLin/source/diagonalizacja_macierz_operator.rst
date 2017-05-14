Square Matrix as a Linear Operator
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Dla danej macierzy :math:`\,\boldsymbol{A}\,\in M_n(C)\,` 
definiujemy odwzorowanie

.. math::
   :label: transf
   
   F:\quad C^n \ni \,\boldsymbol{x} \ \,\to\ \, F(\boldsymbol{x})\,:\,=\,
   \boldsymbol{A}\,\boldsymbol{x} \,\in\, C^n\,.

Dokładniej, :math:`\,` jeżeli :math:`\ \ \boldsymbol{A}=
[\,\boldsymbol{A}_1\,|\,\boldsymbol{A}_2\,|\,\ldots\,|\,\boldsymbol{A}_n\,]=
[a_{ij}]_{n\times n}\,,\ \ \boldsymbol{x}\ =\ [x_{i}]_n\,,\ ` to

.. math::
   
   F\ \left[\begin{array}{c} 
            x_{1} \\ x_{2} \\ \ldots \\ x_{n} 
            \end{array}\right]\ =
   \ \left[\begin{array}{cccc}
           a_{11} & a_{12} & \ldots & a_{1n} \\
           a_{21} & a_{22} & \ldots & a_{2n} \\
           \ldots & \ldots & \ldots & \ldots \\
           a_{n1} & a_{n2} & \ldots & a_{nn}
           \end{array}\right]\ 
   \left[\begin{array}{c} 
         x_{1} \\ x_{2} \\ \ldots \\ x_{n} 
         \end{array}\right]\,.

Przyjmujemy uproszczone oznaczenie dla obrazu wektora 
:math:`\,\boldsymbol{x}\,` przy odwzorowaniu :math:`\,F`:

.. math::
   
   F(\boldsymbol{x})\rightarrow F\boldsymbol{x}\,.

**Twierdzenie 0.** :math:`\\ \ `
Odwzorowanie :eq:`transf` jest operatorem liniowym na przestrzeni 
:math:`\,C^n\,`: :math:`\ \ F\in\text{End}\,(C^n)`.

**Dowód.** :math:`\\`
Liniowość odwzorowania :math:`F` jest 
konsekwencją własności mnożenia macierzowego:

.. math::
   
   F(\boldsymbol{x}+\boldsymbol{y})\ =\  
   \boldsymbol{A}\,(\boldsymbol{x}+\boldsymbol{y})\ =\  
   \boldsymbol{A}\,\boldsymbol{x}\ +\ \boldsymbol{A}\,\boldsymbol{y}\ =\ 
   F(\boldsymbol{x})\, +\, F(\boldsymbol{y})\,,

   F(\lambda\,\boldsymbol{x})\ =\ 
   \boldsymbol{A}\,(\lambda\,\boldsymbol{x})\ =\ 
   \lambda\ (\boldsymbol{A}\,\boldsymbol{x})\ =\ 
   \lambda\ F(\boldsymbol{x})\,,
   \quad \boldsymbol{x},\boldsymbol{y}\,\in C^n,\ \ \lambda \in C.

**Twierdzenie 1.** :math:`\\ \ `
:math:`\boldsymbol{A}\,` jest macierzą operatora :math:`\,F\,`
w bazie kanonicznej :math:`\,\mathcal{E}\,` przestrzeni :math:`\,C^n :`
:math:`\ \boldsymbol{A}\,=\,M_{\mathcal{E}}(F)`.

**Dowód.** :math:`\\`
Jeżeli układ :math:`\,\mathcal{E}\,=\,(\boldsymbol{e}_1,\,
\boldsymbol{e}_2,\,\dots,\,\boldsymbol{e}_n)\,` jest bazą kanoniczną
przestrzeni :math:`\,C^n,\ ` to

.. math::

   \begin{array}{rl}
   M_{\mathcal{E}}(F) \!\!\! 
   & =\ \ [\ F(\boldsymbol{e}_1)\ |\ F(\boldsymbol{e}_2)\ |
   \ \ldots\,|\ F(\boldsymbol{e}_n)\,]\ \ = \\ 
   & =\ \ [\ \boldsymbol{A}\boldsymbol{e}_1\,|
   \ \boldsymbol{A}\boldsymbol{e}_2\,|
   \,\ldots\,|\ \boldsymbol{A}\boldsymbol{e}_n\,]\ \ = \\
   & = \ \ [\ \boldsymbol{A}_1\,|\ \boldsymbol{A}_2\,|
   \ \ldots\,|\ \boldsymbol{A}_n\,]\ \ =\ \ \boldsymbol{A}\,.
   \end{array}

**Twierdzenie 2.** :math:`\\ \ `
Wartości własne operatora :math:`\,F\,` są pierwiastkami 
równania charakterystycznego macierzy :math:`\boldsymbol{A}.`

**Dowód.** :math:`\\`
Wektor :math:`\,\boldsymbol{x} \in C^n\setminus\{\boldsymbol{0}\}\,` 
jest wektorem własnym operatora :math:`\,F\,` dla wartości 
:math:`\,\lambda \in C`, :math:`\,` gdy 

.. :math:`\ F(\boldsymbol{x})\,=\,\lambda\,\boldsymbol{x},\ `
   czyli gdy :math:`\boldsymbol{A}\,\boldsymbol{x} = \lambda\,\boldsymbol{x}`,

.. math::
   :label: eigen_1
   
   \begin{array}{rc}
   & F(\boldsymbol{x})\,=\,\lambda\,\boldsymbol{x}, \\
   \text{czyli} & \boldsymbol{A}\,\boldsymbol{x} = \lambda\,\boldsymbol{x}\,,
   \end{array}

   (\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)\ \boldsymbol{x}\ =\ 
   \boldsymbol{0}\,.

Jednorodny problem liniowy :eq:`eigen_1` ma niezerowe rozwiązanie 
:math:`\,\boldsymbol{x}\,` wtedy i tylko wtedy, :math:`\\` 
gdy :math:`\ \det{(\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)}\ =\ 0\,,\ `
czyli gdy :math:`\,\lambda\,` jest pierwiastkiem charakterystycznym macierzy :math:`\,\boldsymbol{A}`.

Liczby :math:`\,\lambda\,` oraz odpowiadające im niezerowe wektory 
:math:`\,\boldsymbol{x}\,` wyznaczone przez równanie :eq:`eigen_1`
będziemy nazywać wartościami własnymi oraz wektorami własnymi macierzy
:math:`\,\boldsymbol{A}`.

A zatem wektor :math:`\,\boldsymbol{x} \in C^n\,` jest wektorem własnym 
macierzy :math:`\,\boldsymbol{A} \in M_n(C)\ ` dla wartości 
:math:`\,\lambda \in C,\ ` gdy :math:`\,\boldsymbol{x}\neq\boldsymbol{0}\ \ ` 
i :math:`\ \ \boldsymbol{A}\,\boldsymbol{x} = \lambda\,\boldsymbol{x}`.

**Twierdzenie 3.** 

1. :math:`\ ` Jeżeli :math:`\boldsymbol{A}\,` jest macierzą hermitowską,
   :math:`\ ` to :math:`\,F\,` jest operatorem hermitowskim:

   .. math::
   
      \boldsymbol{A}^+=\ \boldsymbol{A}\quad\Rightarrow\quad F^+=\ F\,.

2. :math:`\ ` Jeżeli :math:`\boldsymbol{A}\,` jest macierzą unitarną, 
   :math:`\ ` to :math:`\,F\,` jest operatorem unitarnym:
   
   .. math::
      
      \boldsymbol{A}^+\boldsymbol{A}\,=\,\boldsymbol{I}_n
      \quad\Rightarrow\quad F^+F\,=\,I\,,
   
   (:math:`I\ ` - :math:`\ ` operator jednostkowy w przestrzeni :math:`\ C^n`).

3. :math:`\ ` Jeżeli :math:`\boldsymbol{A}\,` jest macierzą normalną, 
   :math:`\ ` to :math:`\,F\,` jest operatorem normalnym:
   
   .. math::
      
      \boldsymbol{A}^+\boldsymbol{A}\,=\,\boldsymbol{A}\,\boldsymbol{A}^+
      \quad\Rightarrow\quad F^+F\,=\,F\,F^+\,.

Wobec powyższego, twierdzenia o wartościach własnych i wektorach własnych 
operatorów hermitowskich (unitarnych, normalnych) mają zastosowanie
do wartości własnych i wektorów własnych 
macierzy hermitowskich (unitarnych, normalnych).

.. **Dowód Twierdzenia 3.** opiera się na poniższych przesłankach.

**Wprowadzenie do dowodu Twierdzenia 3.**

Sprzężenie hermitowskie macierzy :math:`\boldsymbol{A} \in M_n(C)`:

.. math::
   
   \boldsymbol{A}^+:\,=\,(\boldsymbol{A}^T)^* =\,(\boldsymbol{A}^*)^T\,.

Sprzężenie hermitowskie operatora
:math:`\ F\in\text{End}(V),\ V=V(C)\ `  - :math:`\ ` przestrzeń unitarna:

.. math::
   
   \langle\boldsymbol{x},F^+\boldsymbol{y}\rangle:\,=\,
   \langle F\boldsymbol{x},\boldsymbol{y}\rangle\,,\quad
   \boldsymbol{x},\boldsymbol{y}\in V\,.

Warunek konieczny i wystarczający równości dwóch wektorów.
:math:`\\` Niech :math:`\ \boldsymbol{x},\boldsymbol{y} \in V\,,\ `
gdzie :math:`\ V=V(C)\ ` - :math:`\ ` przestrzeń unitarna. Wtedy

.. math::
   
   \boldsymbol{x} = \boldsymbol{y} \quad \Leftrightarrow \quad 
   \langle \boldsymbol{z}, \boldsymbol{x} \rangle =
   \langle \boldsymbol{z}, \boldsymbol{y} \rangle \quad
   \text{dla wszystkich } \boldsymbol{z} \in V\,.
  
Warunek konieczny i wystarczający równości dwóch operatorów liniowych. 
:math:`\\` Niech :math:`\ F,G\in\text{End}(V)\,,\ ` 
gdzie :math:`\ V=V(C)\ ` - :math:`\ ` przestrzeń unitarna. Wtedy

.. math::
   
   F = G \quad \Leftrightarrow \quad 
   \langle \boldsymbol{x}, F \boldsymbol{y} \rangle =
   \langle \boldsymbol{x}, G \boldsymbol{y} \rangle \quad
   \text{dla wszystkich } \boldsymbol{x},\boldsymbol{y} \in V\,.

Iloczyn skalarny w przestrzeni :math:`C^n`.
Dla :math:`\ \ \boldsymbol{x}\ =\ 
\left[\begin{array}{c} x_1 \\ x_2 \\ \ldots \\ x_n \end{array}\right],\ \  
\boldsymbol{y}\ =\ 
\left[\begin{array}{c} y_1 \\ y_2 \\ \ldots \\ y_n \end{array}\right] 
\in C^n\,:`

.. iloczyn skalarny dany jest przez \sum_{i\,=\,1}^n\ x_i^*\,y_i\,=\;

.. math::
   
   \langle \boldsymbol{x},\boldsymbol{y} \rangle \ =\ 
   x_1^*\,y_1\,+\;x_2^*\,y_2\,+\;\dots\;+\;x_n^*\,y_n
   \,=\;[\,x_1^*,\,x_2^*,\,\dots,\,x_n^*\,]\ 
   \left[\begin{array}{c} 
   y_1 \\ y_2 \\ \dots \\ y_n 
   \end{array}\right]\ =\ 
   \boldsymbol{x}^+\boldsymbol{y}\,.

.. **Lemat** :math:`\,` określa sprzężenie hermitowskie :math:`\ F^+\ ` 
   operatora :math:`\ F\ ` danego przez :eq:`transf`:

Sprzężenie hermitowskie :math:`\ F^+\ ` operatora :math:`\ F\ ` 
danego przez :eq:`transf` określa 

**Lemat**.

.. math::
   :label: lemma
   
   \begin{array}{lc}
   & F(\boldsymbol{x})=\boldsymbol{A}\,\boldsymbol{x}\quad\Rightarrow\quad
   F^+(\boldsymbol{x})=\boldsymbol{A}^+\boldsymbol{x}, \\
   \text{czyli}
   & F\,\boldsymbol{x}=\boldsymbol{A}\,\boldsymbol{x}\quad\Rightarrow\quad
   F^+\,\boldsymbol{x}=\boldsymbol{A}^+\boldsymbol{x}.
   \end{array}

**Dowód** lematu. 
Dla każdego wektora :math:`\ \boldsymbol{y}\in C^n:`

.. math::
   
   \begin{array}{rcl}
   \langle\boldsymbol{y},F^+\boldsymbol{x}\rangle \!\! &
   =\ \ \ \langle F\boldsymbol{y},\boldsymbol{x}\rangle
   \ =\ \langle \boldsymbol{A}\,\boldsymbol{y},\boldsymbol{x}\rangle\ = & \\
   & =\ (\boldsymbol{A}\,\boldsymbol{y})^+\,\boldsymbol{x}\ =\ \ 
   \boldsymbol{y}^+\boldsymbol{A}^+\boldsymbol{x}\ = & \!\!
   \langle\boldsymbol{y},\boldsymbol{A}^+\boldsymbol{x}\rangle\,,
   \end{array}

a zatem
:math:`\ F^+\boldsymbol{x}=\boldsymbol{A}^+\boldsymbol{x},
\ \ \boldsymbol{x}\in C^n`.

**Dowód** Twierdzenia 3.

1. :math:`\ ` Niech :math:`\ \boldsymbol{A}^+=\,\boldsymbol{A}.\ ` 
   Wtedy, dla dowolnych :math:`\,\boldsymbol{x},\boldsymbol{y}\in C^n`:
   
   .. math::

      \begin{array}{rll}
      \langle\boldsymbol{x},F^+\boldsymbol{y}\rangle \!\! &
      =\ \ \langle F\boldsymbol{x},\boldsymbol{y}\rangle\ \ =\ \ 
      \langle\boldsymbol{A}\,\boldsymbol{x},\boldsymbol{y}\rangle\ \ =\ \ 
      (\boldsymbol{A}\,\boldsymbol{x})^+\boldsymbol{y}\ \ =
      & \\
      & =\ \ \boldsymbol{x}^+\boldsymbol{A}^+\boldsymbol{y}\ \ =\ \ \ 
      \boldsymbol{x}^+\boldsymbol{A}\,\boldsymbol{y}\ \ \ =\ \ 
      \langle\boldsymbol{x},\boldsymbol{A}\,\boldsymbol{y}\rangle\ \ =
      & \!\! \langle\boldsymbol{x},F\boldsymbol{y}\rangle
      \end{array}

   wobec czego :math:`\ F^+=\ F`.

2. :math:`\ ` Niech :math:`\ \boldsymbol{A}^+\boldsymbol{A}=\boldsymbol{I}_n.\ ` 
   Wtedy, dla dowolnych :math:`\,\boldsymbol{x},\boldsymbol{y}\in C^n`:

   .. math::

      \begin{array}{rll}
      \langle\boldsymbol{x},(F^+F)\,\boldsymbol{y}\rangle \!\! &
      =\ \ \langle\boldsymbol{x},F^+(F\boldsymbol{y})\rangle\ \ =\ \ 
      \langle F\boldsymbol{x}\,,F\boldsymbol{y}\rangle\ \ =\ \ 
      \langle\boldsymbol{A}\,\boldsymbol{x},
      \boldsymbol{A}\,\boldsymbol{y}\rangle\ \ =
      & \\
      & =\ \ (\boldsymbol{A}\boldsymbol{x})^+\,
      (\boldsymbol{A}\boldsymbol{x})\ \ =\ \ 
      \boldsymbol{x}^+\boldsymbol{A}^+
      \boldsymbol{A}\,\boldsymbol{y}\ \ \, = \quad
      \boldsymbol{x}^+\boldsymbol{I}_n\,\boldsymbol{y}\quad\ =
      & \langle\boldsymbol{x},I\,\boldsymbol{y}\rangle
      \end{array}

   wobec czego :math:`\ F^+F=I`.

3. :math:`\ ` Niech :math:`\ \boldsymbol{A}^+\boldsymbol{A}=
   \boldsymbol{A}\boldsymbol{A}^+.\ ` 
   Wykorzystując Lemat :eq:`lemma`, otrzymujemy   


   .. Wtedy, dla dowolnych :math:`\,\boldsymbol{x},\boldsymbol{y}\in C^n`:

   .. math::

      \begin{array}{rl}
      \langle\boldsymbol{x},(F^+F)\,\boldsymbol{y}\rangle \!\! &
      =\ \ \langle\boldsymbol{x},F^+(F\boldsymbol{y})\rangle\ \ =\ \ 
      \langle F\boldsymbol{x}\,,F\boldsymbol{y}\rangle\ \ =\ \ 
      \langle\boldsymbol{A}\,\boldsymbol{x},
      \boldsymbol{A}\,\boldsymbol{y}\rangle\ \ = \\
      & =\ (\boldsymbol{A}\,\boldsymbol{x})^+
      (\boldsymbol{A}\,\boldsymbol{y})\ \ =\ \ 
      \boldsymbol{x}^+(\boldsymbol{A}^+\boldsymbol{A})\,\boldsymbol{y}\ \ =\ \ 
      \boldsymbol{x}^+(\boldsymbol{A}\boldsymbol{A}^+)\,\boldsymbol{y}\ = \\
      & =\ (\boldsymbol{A}^+\boldsymbol{x})^+
      (\boldsymbol{A}^+\boldsymbol{y})\ =\ 
      \langle\boldsymbol{A}^+\boldsymbol{x},
      \boldsymbol{A}^+\boldsymbol{y}\rangle\ =\ 
      \langle F^+\boldsymbol{x},F^+\boldsymbol{y}\rangle\ = \\
      \langle\boldsymbol{x},(FF^+)\,\boldsymbol{y}\rangle
      \end{array}

   dla dowolnych :math:`\,\boldsymbol{x},\boldsymbol{y}\in C^n,\ `
   wobec czego :math:`\ F^+F=FF^+`.


