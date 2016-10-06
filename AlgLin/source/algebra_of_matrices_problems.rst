.. -*- coding: utf-8 -*-

Problems
--------

**Exercise 1.**

Verify by hand calculation the result :math:`\boldsymbol{A}\boldsymbol{B}`
of the computer multiplication.
Add a piece of code that displays the table for the product
:math:`\boldsymbol{B}\boldsymbol{A}\,` and come round 
to the noncommutativity of the matrix multiplication.

Press "Activate" to display matrices and their product;
to change the size of the matrices, write in a new value of n.

.. sagecellserver::

   n = 3
   A = random_matrix(ZZ, n, x=-5, y=6)
   B = random_matrix(ZZ, n, x=-5, y=6)
   table([["  A :","","  B :","","  AB :"],[A,"$\cdot$",B,"=",A*B]])

.. n = 3
   A = random_matrix(ZZ, n, x=-5, y=6)
   B = random_matrix(ZZ, n, x=-5, y=6)
   table([["  A :","","  B :","","  AB :"],[A,"$\cdot$",B,"=",A*B]])
   table([["  A :","","  B :","","  A*B :"],[A,"*",B,"=",A*B]])

**Exercise 2.**

* | Create the matrix A by two other ways.
* | Determine the base ring of the matrix A (apply ``A.base_ring()``).
* | Write the matrix B obtained from A by substition a = -1
  | (apply ``A.subs()``) and determine the ring thereof.
* | Write the matrix C obtained from B by changing the ring to RDF
  | (apply ``B.change_ring()``) and investigate the ring. 

.. sagecellserver::
   
   var('a')
   A = matrix([[a, 2, 3.], [4/3, 5, 6]])
   show(A)

**Exercise 3.**

* Making use of the constructor ``random_matrix()``, create a random 
  :math:`\ 5 \times 4\ ` matrix :math:`\,\boldsymbol{A}\,` 
  over the integer ring.
  
* Using the slicing technique, create the matrix :math:`\,\boldsymbol{B},\,` 
  whose consecutive rows are the last, middle and first row 
  of matrix :math:`\,\boldsymbol{A}.`
  
  *Hint.* Use the template ``[p:q:r]`` with the default value of q :
  ``[p::r]``, and with p = -1, r = -2. What is the actual value of q ?
  
* Write down a selected column of matrix :math:`\,\boldsymbol{A}\,` 
  as a vector :math:`\,\boldsymbol{v}\,` and as a 1-column matrix 
  :math:`\,\boldsymbol{C}.\ ` Verify the type of the obtained objects.

.. sagecellserver::

   A = 
   B = 
   v =
   C =
 
   show ((A, B, v, C))
   print type(v)
   print type(C)     

