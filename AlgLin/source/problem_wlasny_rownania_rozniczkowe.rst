
Liniowe układy równań różniczkowych
-----------------------------------

Zajmiemy się liniowym układem równań różniczkowych 1. rzędu 
o stałych współczynnikach:

.. math::
   :label: set_diff
   
   \begin{array}{l}
   \dot{x}_1\ =\ a_{11}\,x_1\,+\,a_{12}\,x_2\,+\,\ldots\,+\,a_{1n}\,x_n \\
   \dot{x}_2\ =\ a_{21}\,x_1\,+\,a_{22}\,x_2\,+\,\ldots\,+\,a_{2n}\,x_n \\
   \ \ldots\qquad\ldots\qquad\ \ \ldots\qquad\ldots\qquad\ldots\qquad   \\
   \dot{x}_n\ =\ a_{n1}\,x_1\,+\,a_{n2}\,x_2\,+\,\ldots\,+\,a_{nn}\,x_n \\ 
   \end{array}

gdzie :math:`\ \ x_i=x_i(t)\,,\ \ \dot{x}_i\,=\,\frac{d}{dt}\ x_i(t)\,,\ \ 
a_{ij}\in R\,,\ \ i,j=1,2,\ldots,n.\ `
Wprowadzając oznaczenia

.. math::
   
   \boldsymbol{A}\ =\ 
   \left[\begin{array}{cccc} 
      a_{11} & a_{12} & \dots & a_{1n} \\
      a_{21} & a_{22} & \dots & a_{2n} \\
      \dots & \dots & \dots & \dots    \\
      a_{n1} & a_{n2} & \dots & a_{nn} \\
   \end{array}\right]\,,\qquad
   \boldsymbol{x}\ =\ 
   \left[\begin{array}{c} 
      x_1 \\ x_2 \\ \ldots \\ x_n \end{array}\right]\,,\qquad
      \dot{\boldsymbol{x}}\ =\ 
   \left[\begin{array}{c} 
      \dot{x}_1 \\ \dot{x}_2 \\ \ldots \\ \dot{x}_n 
   \end{array}\right]\,,


można układ :eq:`set_diff` zapisać w zwartej postaci macierzowej:
 
.. math::
   :label: mat_eqn
   
   \dot{\boldsymbol{x}}\ =\ \boldsymbol{A}\,\boldsymbol{x}\,.

.. Poprzedni zapis \boldsymbol{\dot{x}}
   stawiał w wersji .html kropkę nad 'x' przesuniętą w górę
   (w wersji .pdf wynik był poprawny)

Szukamy rozwiązań postaci 

.. math::
   :label: exp_soln
   
   \boldsymbol{x}(t)\,=\,\boldsymbol{v}\,e^{\,\lambda\,t}\,,\qquad
   \lambda\in C\,,\quad\boldsymbol{v}=[\,\beta_i\,]_n\in C^n\,.

Wtedy 
:math:`\ \,\dot{\boldsymbol{x}}(t)=\lambda\,\boldsymbol{v}\,e^{\,\lambda\,t}\ `
i podstawienie do :eq:`mat_eqn` daje

.. math::
   
   \lambda\,\boldsymbol{v}\,e^{\,\lambda\,t}\ =\ 
   \boldsymbol{A}\,\boldsymbol{v}\,e^{\,\lambda\,t}\,,

skąd, po podzieleniu przez :math:`\ e^{\,\lambda\,t}\neq 0\,,\ ` otrzymujemy

.. math::
   :label: eigen_eqn
   
   \boldsymbol{A}\,\boldsymbol{v}\ =\ \lambda\,\boldsymbol{v}\,.

Równanie :eq:`eigen_eqn` jest problemem własnym macierzy 
:math:`\,\boldsymbol{A}\ ` potraktowanej jako operator liniowy w przestrzeni 
:math:`\,C^n\ ` (działanie tego operatora na wektor 
:math:`\,\boldsymbol{x}\in C^n\,` polega na mnożeniu go z lewej strony przez 
:math:`\boldsymbol{A}`).

.. (działając na wektor :math:`\,\boldsymbol{x}\in C^n\,` operator 
   mnoży go z lewej strony przez :math:`\boldsymbol{A}`).

Tak więc funkcja :eq:`exp_soln` jest rozwiązaniem równania :eq:`mat_eqn` 
wtedy i tylko wtedy, :math:`\,` gdy :math:`\\` :math:`\lambda\ ` jest wartością 
własną macierzy :math:`\,\boldsymbol{A}\,,\ ` a :math:`\ \,\boldsymbol{v}\ ` - 
:math:`\,` wektorem własnym należącym do tej wartości.

Wartości własne :math:`\ \lambda\ ` wyliczamy z równania charakterystycznego

.. math::
   :label: char_eqn
   
   \det\,(\boldsymbol{A}-\lambda\,\boldsymbol{I}_n)\ \ =\ \ 
   \left|
   \begin{array}{cccc}
   \alpha_{11}-\lambda & \alpha_{12} & \dots & \alpha_{1n} \\
   \alpha_{21} & \alpha_{22}-\lambda & \dots & \alpha_{2n} \\
   \dots & \dots & \dots & \dots \\
   \alpha_{n1} & \alpha_{n2} & \dots & \alpha_{nn}-\lambda 
   \end{array}
   \right|\ \ =\ \ 0\,.

a odpowiednie wektory własne :math:`\,` - :math:`\,` rozwiązując 
problem liniowy :eq:`eigen_eqn` dla danej wartości :math:`\,\lambda:`

.. .. math::
      :label: hom_set
      
      (a_{11}-\lambda)\ \beta_1\,+\,a_{12}\ \beta_2\,+\,\ldots
      \,+\,a_{1n}\ \beta_n\ =\ 0
   
      a_{21}\ \beta_1\,+\,(a_{22}-\lambda)\ \beta_2\,+\,\ldots
      \,+\,a_{2n}\ \beta_n\ =\ 0
   
      \quad\ldots\qquad\ldots\qquad\ldots\qquad\ldots\qquad\ldots

      a_{n1}\ \beta_1\,+\,a_{n2}\ \beta_2\,+\,\ldots
      \,+\,(a_{nn}-\lambda)\ \beta_n\ =\ 0

.. math::
   :label: hom_set
   
   \begin{array}{l}
   (a_{11}-\lambda)\ \beta_1\,+\,a_{12}\ \beta_2\,+\,\ldots
   \,+\,a_{1n}\ \beta_n\ =\ 0 \\
   a_{21}\ \beta_1\,+\,(a_{22}-\lambda)\ \beta_2\,+\,\ldots
   \,+\,a_{2n}\ \beta_n\ =\ 0 \\
   \ \ \ldots\qquad\ldots\qquad\ldots\qquad\ldots\qquad\ldots \\
   a_{n1}\ \beta_1\,+\,a_{n2}\ \beta_2\,+\,\ldots
   \,+\,(a_{nn}-\lambda)\ \beta_n\ =\ 0
   \end{array}

Ze względu na jednorodność układu :eq:`set_diff`, a także odpowiadającego mu 
równania macierzowego :eq:`mat_eqn`, każda kombinacja liniowa rozwiązań jest 
również jego rozwiązaniem.



