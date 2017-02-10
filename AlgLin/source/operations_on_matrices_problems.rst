Exercises and Problems
----------------------

Solution of a linear system by the Gauss-Jordan elimination
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Exercise.**

The coefficient matrix :math:`\boldsymbol{A}\,` and the vector of constants
:math:`\,\boldsymbol{b}\,` determine a linear system of four equations 
in four variables with a unique solution over the rational field.

1. | :math:`\,` Construct the augmented matrix :math:`\,\boldsymbol{B}\,`
     and solve the system 
   | :math:`\,` by transforming :math:`\,\boldsymbol{B}\,`
     into the reduced row echelon form.

2. | :math:`\,` To confirm the result ascertain that 
     the product of the matrix :math:`\boldsymbol{A}\,` 
   | :math:`\,` by the solution column 
     :math:`\,\boldsymbol{x}\,` equals the column of constants
     :math:`\,\boldsymbol{b}`.

.. | :math:`\,` Confirm the result by verifying that the product of the matrix 
     :math:`\boldsymbol{A}\,` 
   | :math:`\,` and the solution column 
     :math:`\,\boldsymbol{x}\,` equals the column of constants
     :math:`\,\boldsymbol{b}`.

**Hint.** The solution column :math:`\,\boldsymbol{x}\,` 
is the last column of the augmented matrix in the reduced row echelon form 
(it may be detached by slicing). 
The method ``column()`` may be used to convert a vector 
into the one-column matrix.

.. sagecellserver::

   A = matrix(QQ,[[1, 2, 3,-2],
                  [2,-1,-2,-3],
                  [3, 2,-1, 2],
                  [2,-3, 2, 1]])
               
   b = vector([6,8,4,-8])

Elementary operations on matrices by the Sage commands
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Exercise 1.** :math:`\\`
Uncomment one of the three hashed lines to demonstrate that the corresponding
command operates directly upon the original matrix:

The row version:

.. sagecellserver::
   
   A = matrix([[2, 5, 3, 0],
               [2, 0,-2,-1],
               [0, 0, 4, 5]])
            
   # A.swap_rows(1,2)
   # A.rescale_row(2,-3)
   # A. add_multiple_of_row(0,1,3)
   A

The column version:

.. sagecellserver::

   A = matrix([[2, 5, 3, 0],
               [2, 0,-2,-1],
               [0, 0, 4, 5]])
            
   # A.swap_columns(1,2)
   # A.rescale_col(2,-3)
   # A. add_multiple_of_column(0,1,3)
   A

**Exercise 2.** :math:`\\`
Uncomment one of the three hashed lines to demonstrate that the corresponding
command returns a transformed matrix while leaving the original one unchanged:

The row version:

.. sagecellserver::
   
   A = matrix([[2, 5, 3, 0],
               [2, 0,-2,-1],
               [0, 0, 4, 5]])

   # B = A.with_swapped_rows(1,2)
   # B = A.with_rescaled_row(2,-3)
   # B = A.with_added_multiple_of_row(0,1,3)
   A,B

The column version:

.. sagecellserver::
   
   A = matrix([[2, 5, 3, 0],
               [2, 0,-2,-1],
               [0, 0, 4, 5]])
            
   # B = A.with_swapped_columns(1,2)
   # B = A.with_rescaled_col(2,-3)
   # B = A.with_added_multiple_of_column(0,1,3)
   A,B

**Exercise 3.** :math:`\\`
Note that whereas ``echelonize()`` acts directly on the original matrix,
``echelon_form()`` and ``rref()`` return the modified matrix without 
changing the original: :math:`\\`

.. sagecellserver::

   A = matrix([[2, 5, 3, 0],
               [2, 0,-2,-1],
               [0, 0, 4, 5]])
            
   A.echelonize(); A

.. sagecellserver::

   A = matrix([[2, 5, 3, 0],
               [2, 0,-2,-1],
               [0, 0, 4, 5]])
            
   B = A.echelon_form()
   C = A.rref()
   A, B, C

Matrix Inversion by the Elimination Method
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The inverse of a given matrix :math:`\,\boldsymbol{A}\in M_n(K)\,` can be 
obtained by appropriate elementary row operations on the 2-block
composed of :math:`\,\boldsymbol{A}\,` and the identity matrix
:math:`\,\boldsymbol{I}_n.\ `

In a previous section a 2-block has been built by the method ``augment()``, 
and the matrix :math:`\,\boldsymbol{A}^{-1}\,` was selected 
by slicing. In the present alternative way the framework of block matrices 
is applied. The association of matrices :math:`\,\boldsymbol{A}\,` and 
:math:`\,\boldsymbol{I}_n\ ` is performed by the method ``block_matrix()``, 
whereas the resulting inverse matrix :math:`\,\boldsymbol{A}^{-1}\,`
is isolated using the method ``subdivision()``. [5]_
In both cases the row-reducing is executed by ``rref()``.

The following program generates an invertible matrix :math:`\,\boldsymbol{A}\,` 
of a given order :math:`\,n\,` over the rational field :math:`\,Q,\ `
and calculates its inverse by means of the above-mentioned 
procedures. 

.. :math:`\ `

.. **Exercise.** :math:`\,`

.. admonition:: Experiment with Sage! 
 
   For :math:`\,n = 2,\,3\ ` perform by hand elementary operations which 
   transform a matrix :math:`\ [\,\boldsymbol{A}\,|\,\boldsymbol{I}\,]\ ` 
   to the form :math:`\ [\,\boldsymbol{I}\,|\,\boldsymbol{A}^{-1}\,].\ ` 
   Compare your result with that given by the program.

   Experiment with greater :math:`\,n\,` and compare the result of the present 
   elimination method with that given by the standard method ``inverse()`` 
   of matrix inversion. 

:math:`\ `

.. sagecellserver::

   n = 4

   A = random_matrix(QQ, n, algorithm = 'echelonizable',
                     rank = n, upper_bound = 10)

   show(table([["Calculate the inverse of the matrix", 'A', '=', A]]))
  
   B = block_matrix([[A,identity_matrix(n)]])  # augment the matrix A
   R = B.rref()                # reduced row echelon form of B
   A_1 = R.subdivision(0,1)    # matrix A^(-1) selected from R
   
   @interact
   
   def _(h=('Step:',["2-block (A,I)","2-block (I,A^(-1))","Verify"])):
    
       if h=="2-block (A,I)": show(table([
           ["", "", "$\qquad\ $ B = (A,I)$\:$ is extension of A:"],
           ["B", '=', B]]))
                    
       elif h=="2-block (I,A^(-1))": show(table([
           ["", "", "$\quad\ \ \ $ Reduced row echelon form of B:"],
           ["B.rref()", '=', R]]))
                    
       elif h=="Verify": show(table([
           ["$A\ :$", "", "$A^{-1}\ :$", "", "$A\ *\ A^{-1}\ :$"],
           [A, '*', A_1, '=', A*A_1]]))

Permutation Matrices
~~~~~~~~~~~~~~~~~~~~

**Problem.**

Pre-multiplying a column vector :math:`\,\boldsymbol{x}\,=\,[x_i]_m\in K^m\ `
by a permutation matrix :math:`\,\boldsymbol{P}_\sigma\in M_m(K)\ ` 
rearranges the entries of :math:`\,\boldsymbol{x}\ ` according 
to the permutation :math:`\,\sigma:`

.. math::
   
   \boldsymbol{P}_\sigma\ \boldsymbol{x}\ =\ 
   \left[\begin{array}{c}
   \boldsymbol{e}_{\sigma(1)} \\
   \boldsymbol{e}_{\sigma(2)} \\ 
   \dots                      \\
   \boldsymbol{e}_{\sigma(m)}
   \end{array}\right]
   \left[\begin{array}{c}
   x_1 \\ x_2 \\ \dots \\ x_m
   \end{array}\right]\ =\ 
   \left[\begin{array}{c}
   x_{\sigma(1)} \\ x_{\sigma(2)} \\ \dots \\ x_{\sigma(m)}
   \end{array}\right]\,.

(here :math:`\,\boldsymbol{e}_i\ ` is a :math:`\,` *row* :math:`\,` 
vector with unity in the :math:`\,i`-th position, zeroes elsewhere, 
:math:`\ i=1,2,\dots,m.`).

Validate the result of action of :math:`\,\boldsymbol{P}_\sigma\ ` 
upon the :math:`\,` *column* vector :math:`\,\boldsymbol{e}_k^T :`

.. math::
   
   \boldsymbol{P}_\sigma\ \boldsymbol{e}_k^T\ =\ 
   \boldsymbol{e}^T_{\sigma^{-1}(k)}\,,\quad
   k=1,2,\dots,m.

.. :math:`\ `

.. **Exercise.**

.. Given a number :math:`\,n=2,3,...,\ ` the program constructs the permutation 
   group :math:`\,S_n\,`  and displays a randomly selected permutation 
   :math:`\,\sigma\in S_n\,` together with its matrix 
   :math:`\,\boldsymbol{P}_\sigma.`

.. admonition:: Experiment with Sage!
   
   Set an integer :math:`\,n=2,3,...,\ ` and display a randomly selected 
   permutation :math:`\,\sigma\in S_n\,` together with its matrix 
   :math:`\,\boldsymbol{P}_\sigma.`   
   
.. sagecellserver::

   n = 4   
   G = SymmetricGroup(n)
   g = G.random_element()
   (g, g.matrix())

Column Version of Permutation Matrices
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this approach a permutation refers to columns 
rather than to rows of a matrix.

Namely, for a rectangular matrix
:math:`\ \boldsymbol{A}\,=\,[a_{ij}]_{m\times n}\in M_{m\times n}(K)\ `
given in the column form

.. math::
   
   \boldsymbol{A}\ =\ 
   [\,\boldsymbol{A}_1\,|\,\boldsymbol{A}_2\,|\,\dots\,|\,\boldsymbol{A}_n\,]\,,
   \quad\text{where}\quad
   \boldsymbol{A}_j\ =\ 
   \left[\begin{array}{c}
   a_{1j} \\ a_{2j} \\ \dots \\ a_{mj}
   \end{array}
   \right]\,,\quad j=1,2,\ldots,n,

and a permutation :math:`\ \sigma\in S_n\,,\ ` the operation 
:math:`\,O^t_\sigma\,` is defined by

.. math::
   
   O^t_\sigma\,\boldsymbol{A}\ \ :\,=\ \ 
   [\;\boldsymbol{A}_{\sigma(1)}\,|\;\boldsymbol{A}_{\sigma(2)}\,|\;\dots\,|\,
   \boldsymbol{A}_{\sigma(n)}\,]

(the superscript 't' distinguishes the column operation 
from its row counterpart).

By analogy with the row case, the permutation matrix 
:math:`\ \boldsymbol{Q}_\sigma\ ` is defined as :math:`\\` the result 
of application of :math:`\,O^t_\sigma\,` to the identity matrix 
:math:`\ \boldsymbol{I}_n =
[\;\boldsymbol{e}_1\,|\;\boldsymbol{e}_2\,|\;\dots\,|\,\boldsymbol{e}_n\,]\,:`

.. math::
   
   \boldsymbol{Q}_\sigma\ :\,=\ O^t_\sigma\ \boldsymbol{I}_n\ =\ 
   [\;\boldsymbol{e}_{\sigma(1)}\,|\;\boldsymbol{e}_{\sigma(2)}\,|\;\dots\,|\,
   \boldsymbol{e}_{\sigma(n)}]

.. (:math:`\boldsymbol{e}_j\ ` is a column vector with the unity 
   in the :math:`\,j`-th position, zeroes elsewhere, :math:`\ j=1,2,..,n.`).

.. :math:`\,`

**Problem 1.** :math:`\,`
Prove that:

1. | :math:`\,` A permutation of columns of a product 
     :math:`\boldsymbol{A}\boldsymbol{B}\ ` 
     of two matrices can be achieved 
   | :math:`\,` by the same permutation of columns 
     of the *second* factor :math:`\boldsymbol{B}\ ` only.

2. | :math:`\,` A permutation of columns of a rectangular matrix 
     :math:`\boldsymbol{A}\ ` is equivalent 
   | :math:`\,` to *post*-multiplying :math:`\boldsymbol{A}\ ` 
     by the matrix of that permutation.

This may be written down in detail as

.. admonition: Theorem.
   
   Let :math:`\,\boldsymbol{A}\in M_{m\times p}(K),\ 
   \boldsymbol{B}\in M_{p\times n}(K),\ \ 
   \sigma\in S_n\,.\ ` Then 

   1. :math:`\ O_\sigma\,(\boldsymbol{A}\boldsymbol{B})\ =\ 
      \boldsymbol{A}\,(O_\sigma\boldsymbol{B})\,;`

   2. :math:`\ O_\sigma\,\boldsymbol{A}\ =\ 
      \boldsymbol{A}\,\boldsymbol{P}_\sigma\,,\qquad\text{where}\quad
      \boldsymbol{P}_\sigma = O_\sigma\,\boldsymbol{I}_n\in M_n(K)\,.`

.. admonition:: Theorem.

   Given a permutation :math:`\ \sigma\in S_n\,,\ `
   the following statements hold true:

   1. :math:`\,` If :math:`\,\boldsymbol{A}\in M_{m\times p}(K),\ 
      \boldsymbol{B}\in M_{p\times n}(K),\ `
      then
      :math:`\ O^t_\sigma\,(\boldsymbol{A}\boldsymbol{B})\ =\ 
      \boldsymbol{A}\,(O^t_\sigma\boldsymbol{B})\,.`

   2. :math:`\,` If :math:`\,\boldsymbol{A}\in M_{m\times n}(K),\ `
      then
      :math:`\ O^t_\sigma\,\boldsymbol{A}\ =\ 
      \boldsymbol{A}\,\boldsymbol{Q}_\sigma\,,\ \ \text{where}\ \ 
      \boldsymbol{Q}_\sigma = O^t_\sigma\,\boldsymbol{I}_n\in M_n(K)\,.`

**Hints.**
 
1. :math:`\,` Apply the Column Rule of Matrix Multiplication.

2. :math:`\,` Note that
   :math:`\ \boldsymbol{A} = \boldsymbol{A}\,\boldsymbol{I}_n\ `
   and take advantage of statement 1.

**Problem 2.** :math:`\,`

Prove that a product of two permutation matrices is also a permutation matrix:

.. math::
   :label: QQ_col
   
   \boldsymbol{Q}_\rho\ \boldsymbol{Q}_\sigma\ =\ \,
   \boldsymbol{Q}_{\rho\:\circ\:\sigma}\,,
   \qquad\rho,\sigma\in S_n\,.

**Hint.** :math:`\,` 

Recall the multiplication rule for the row permutation matrices:

.. math::
   :label: PP_row

   \quad\boldsymbol{P}_\rho\ \boldsymbol{P}_\sigma\ =
   \ \boldsymbol{P}_{\sigma\,\circ\,\rho}\,,\quad\rho,\sigma\in S_m

and remark that the row and column matrices of a permutation
are interrelated by transpose:

.. math::
   
   \boldsymbol{Q}_\sigma = \,\boldsymbol{P}_\sigma^{\,T}\,,\quad 
   \boldsymbol{P}_\sigma = \,\boldsymbol{Q}^{\,T}_\sigma\,,\qquad
   \sigma\in S_n.

.. note:: :math:`\ `
   
   Observe that the Rule :eq:`QQ_col` preserves the order of permutations    
   (whereas in :eq:`PP_row` the order is reversed). This means that the map
   
   .. math::
      
      S_n\ni\,\sigma\quad\rightarrow\quad Q_\sigma \in\,M_n(K)

   is a *representation* of the group :math:`\,S_n\ `
   on the vector space :math:`\ K^n.` 
   
   

.. [5] http://doc.sagemath.org/html/en/reference/matrices/sage/matrix/matrix2.html










