.. title: The exponential function (exp)
.. slug: exp-function
.. date: 2020-12-20 16:49:18 UTC+01:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. has_math: true

The exponential function :math:`e^x`, sometimes written as :math:`\mathrm{exp}(x)`, is a famous function with many applications, far more than just exponential growth and decay. It is defined by the power series [#]_

.. math::
   e^x ~=~ \sum_{n=0}^\infty \frac{x^n}{n!} ~=~ 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \frac{x^4}{24} + \frac{x^5}{120}+\cdots
   
with :math:`n!` the faculty of the integer :math:`n` and the number :math:`e\,=\,\sum_{n=0}^\infty \frac{1}{n!}\,\approx\,2.718....` the constant of Euler, after the Swiss mathematician Leonhard Euler (1707 - 1783) [#]_.

.. TEASER_END

In some sense, the exponential function is a generalisation of the sine and the cosine functions, :math:`\mathrm{sin}(x)` and :math:`\mathrm{cos}(x)` respectively, which are defined as [#]_


.. math::
   \begin{array}{lclcl}
   \mathrm{sin}(x)&=&\displaystyle\sum_{n=0}^\infty \frac{(-1)^nx^{2n+1}}{(2n+1)!}&=&\displaystyle x-\frac{x^3}{6}+\frac{x^5}{120}-\cdots \\
   \mathrm{cos}(x)&=&\displaystyle\sum_{n=0}^\infty \frac{(-1)^nx^{2n}}{(2n)!}&=&\displaystyle 1-\frac{x^2}{2}+\frac{x^4}{24}-\cdots
   \end{array}

One may recognize the similarities in the coefficients with the power series of the :math:`\mathrm{exp}(x)` function. More precisely, when we evaluate the :math:`\mathrm{exp}(x)` function for pure imaginary values of :math:`x`, that is :math:`x=i\alpha` with :math:`\alpha\in\mathbb{R}` an arbitrary real number and :math:`i` the imaginary unit [#]_, such that :math:`i^2=-1`, then one can write

.. math::
   e^{i\alpha}~=~\cos(\alpha) + i\sin(\alpha)

which is known as the Euler's formula [#]_. So, by applying the exponential function to *imaginary* numbers the exponential function splits in some sense in two separate functions: the real part being the *cosine* and the imaginary part being the *sine* function. This 'splitting' is thanks to the property of the *imaginary* unit :math:`i` that by squaring :math:`i` it yields a *real* number (:math:`i^2\,=\,-1`), and thus :math:`i^n` is real for even and imaginary for odd values of :math:`n`. Moreover, the alternating signs in the power series of the sine and the cosine functions are due to the fact that :math:`(-1)^n` is :math:`+1` for even and :math:`-1` for odd values of :math:`n`.

Thanks to this splitting in sine and cosine functions, the exponential function applied to imaginary or complex numbers can be used to describe oscillatory behavior in dynamic systems, as well as making rotations, projections and reflections in geometry. To be able to perform this in three rather than two dimensions, the imaginary or complex number may be replaced by a so called *quaternion* [#]_ or an even more general *rotor* or *motor* in the field of geometric algebra [#]_, which may be the topic of another blog post. 

Evaluating Euler's formula at :math:`\alpha=\pi`, with :math:`\pi` the circle constant [#]_, yields the Euler's identity [#]_

.. math::
   e^{i\pi}+1~=~0

that beautifully relates five mathematical constants: :math:`0,\,1,\,i,\,\pi` and :math:`e`.

The inverse of the exponential function is the natural logarithm function :math:`\mathrm{ln}(x)`, such that :math:`\mathrm{ln}(e^x)\,=\,x` and in addition,  provided :math:`x>0`, :math:`e^{\mathrm{ln}(x)}\,=\,x` [#]_.


Solving differential equations
------------------------------

The exponential function appears as a solution or part of a solution of an equation with differentials, better known as a differential equation [#]_, e.g. of the form

.. math::
   \frac{\mathrm{d} y}{\mathrm{d} x}~=~ a y(x).

Here :math:`x` may represent a position in a spatial dimension, e.g. in meters, and the function :math:`y(x)` may represent the spatial distribution of a physical quantity, e.g. units of strain or units of electrical charge. Differential equations also show up in describing dynamical systems, then :math:`x` represents time (usually represented by the symbol :math:`t` rather than :math:`x`), expressed e.g. in units of seconds, and :math:`y(x)` represents the position or velocity of a particle as a function of time. Also note, that the (physical) unit of :math:`a` is the inverse of the unit of :math:`x`, to have proper units on both sides of the differential equation, i.e. units of :math:`y` per units of :math:`x`. Hence, if :math:`x` is measured in :math:`\mathrm{s}` (seconds), than :math:`a` has the unit :math:`1/\mathrm{s}\,=\,\mathrm{s}^{-1}`.

The exponential functions appears in the solution :math:`y(x)` of the differential equation, because the exponential function is equal to its derivative, i.e.

.. math::
   \frac{\mathrm{d}e^x}{\mathrm{d} x}~=~ e^x.

This property can be verified by term for term differentiating the power series expansion of the exponential function given in the first equation of this article. Therefore :math:`e^x` satisfies the differential equation

.. math::
   \frac{\mathrm{d} y}{\mathrm{d} x}~=~ y(x).
  
But, note that there are more functions satisfying this differential equation, all are of the form :math:`y(x)\,=\,ce^x` with :math:`c` some number. This number can be determined uniquely if in addition to the differential equation we add another equation, also known as a *constraint*, *initial condition* or *boundary condition*. For example, when :math:`y(0)=3` it follows that :math:`c=3`, because :math:`e^0\,=\,1`. Also note, that the (physical) unit of :math:`c` is the same as the unit of :math:`y`.

Thanks to the chain rule in calculus [#]_ it can be shown that

.. math::
   \frac{\mathrm{d}e^{ax}}{\mathrm{d}x} ~=~ ae^{ax}

which gives *a* solution to the differential equation depending on :math:`a` given above, and all solutions are of the form :math:`y(x)\,=\,ce^{ax}`, with :math:`c` some number determined by the additional constraint. The parameter :math:`a` of the differential equation, can be seen as a *scaling* parameter of the spatial or temporal dimension :math:`x`. This can be seen by dividing the differential equation by :math:`a`, resulting in

.. math::
   \frac{\mathrm{d} y}{a\mathrm{d} x}~=~ y(x)

which, by introducing the scaled dimension parameter :math:`x'\,=\,ax`, can be rewritten in the *normalized* differential equation

.. math::
   \frac{\mathrm{d} y}{\mathrm{d} x'}~=~ y(x').

Solutions to this differential equation has been shown above as having the form :math:`y(x')=ce^{x'}`, which is only valid over the scaled (or normalized) dimension parameter :math:`x'\,=\,ax`. Rewriting in terms of the *unscaled* dimension parameter :math:`x` yields the form we obtained by applying the chain rule

.. math::
   y(x)~=~ce^{ax}.

As we have seen above, the parameters :math:`c` and :math:`a` are both depending on the units that have been chosen for :math:`y` and :math:`x` respectively. In fact these parameters determine how much we have to scale down :math:`y` by :math:`c` and stretch :math:`x` by :math:`a` to arrive at the exponential function :math:`e^{x'}`. Or stated otherwise, :math:`c` determines how much units the physical quantity :math:`y` represents and the parameter :math:`a` specifies how *fast* :math:`y` is changing as :math:`x` evolves, which is after all just what the differential equation :math:`\mathrm{d}y/\mathrm{d}x\,=\,ay(x)` is saying.

Besides the special case of :math:`a=1` leading to the normalized differential equation, it is illustrative to interprete the differential equation and its solution for :math:`a=0`, :math:`a=-1`, :math:`a\to+\infty` and :math:`a\to-\infty`. Note, that nothing witholds you (and is really rewarding) to study the equations for imaginary values :math:`a=i\alpha` (:math:`\alpha\in\mathbb{R}`) and more general complex values :math:`a=\alpha+i\beta` (:math:`\alpha,\beta\in\mathbb{R}`) as well!

The matrix exponential
----------------------

The above discussion has been performed for :math:`x` and :math:`y` being scalar quantities and the exponential function being a scalar function. However, the exponential function is not limited to scalars, it can be applied on matrix quantities as well. Therefore, let :math:`X` be a *square* matrix, then the matrix exponential function is defined (similarly as above in the scalar case) by [#]_

.. math::
   e^X~=~\sum_{n=0}^\infty \frac{X^n}{n!}~=~I + X + \frac{X^2}{2} + \frac{X^3}{6} + \frac{x^4}{24} + \frac{X^5}{120} + \cdots.

where :math:`I` the identity matrix having the same dimension as :math:`X`. So the matrix exponential :math:`e^X` is a square matrix as well having the same dimension as :math:`X`.

In the following we replace :math:`X` by the quantity :math:`At` where :math:`A` a square matrix, which generalizes the parameter :math:`a` above to the matrix case, and :math:`t` a scalar quantity representing e.g. time or displacement in a fixed direction, similar as the parameter :math:`x` above. Then, the matrix exponential function :math:`e^{At}`
has a beautiful derivative with respect to the scalar quantity :math:`t`, given by

.. math::
   \frac{\mathrm{d}e^{At}}{\mathrm{d}t}~=~Ae^{At},

which can be verified, similar as in the scalar case, by taking term for term the derivative of the power series of the matrix exponential function. Note, we could have written :math:`\mathrm{d}e^{At}/\mathrm{d}t\,=\,e^{At}A` as well, so :math:`A` commutes with :math:`e^{At}`, though matrix products do not commutative in general! 

This result can be applied to solve *coupled* differential equations, that show up in e.g. linear dynamic systems with multiple lumped components, such as mass-spring-damper systems or RLC-networks in the electrical domain. Often, the differential equations can be ordered in such a way that they can be written in the form of the following vector differential equation

.. math::
   \frac{\mathrm{d}y}{\mathrm{d}t}~=~ A y(t)

where now :math:`y(t)` is a (column) vector signal having as many elements as the rows or columns of the square matrix :math:`A`. Note, that to have the units being identical on both sides of this vector differential equation, the unit of :math:`A` should be the inverse of the unit of :math:`t`. For dynamic systems :math:`t` usually has the unit :math:`\mathrm{s}` and thus :math:`A` has the unit :math:`\mathrm{s}^{-1}`.

The solutions to the vector differential equation have the form

.. math::
   y(t)~=~e^{At}c

where :math:`c` a (column) vector having the same dimension and unit as :math:`y`, and can be determined when an additional condition on :math:`y(t)` for some :math:`t` is added, often an initial condition :math:`y(0)=c` because :math:`e^{At}\,=\,I` for :math:`t=0`.

For the scalar case when :math:`A\,=\,a\in\mathbb{R}` or :math:`\mathbb{C}` the evolution of :math:`e^{at}` is as studied above. For the case :math:`A` is a :math:`2\times2` matrix or of higher dimension is more complex. However, the scalar case simply extends to the matrix case when :math:`A` is a *diagonal* matrix, i.e. a matrix with arbitrary values :math:`a_k` on the diagonal and zeros elsewhere. In this case of diagonal :math:`A`, the matrix exponential :math:`e^{At}` is a diagonal matrix as well with diagonal elements :math:`e^{a_kt}`, similar to the scalar case. In fact, when :math:`A` is diagonal the equations in the vector differential equation are not coupled and can be considered as multiple scalar differential equations.

More difficult is the situation when one or more *off-diagonal* elements of :math:`A` are nonzero. In this case the matrix should be made *diagonal* or *triangular* by making certain transformations, based on the eigenvalue decomposition [#]_ or the Jordan normal form [#]_ respectively. The resulting solutions contain :math:`e^{\lambda_k t}` where :math:`\lambda_k` an eigenvalue that replaces the :math:`a` in the scalar case, and can be:

1. real, equivalent to exponential growth or decay;
2. imaginary, harmonic oscillatory behavior;
3. complex, growing or decaying harmonic oscillatory behavior.  

In another blog post, we may go in further detail about this, for now we refer to some youtube-videos of MIT math professor Gilbert Strang on Diagonalizing a Matrix [#]_ and The Matrix Exponential [#]_.

In this article we have only considered *autonomous* systems, i.e. systems without applying external inputs, such as disturbances or controls. Extending to dynamic systems with external inputs will result in the so called State-space representation [#]_, that may also be the topic of another post.

I would like to finish this article on the exponential function with poiting to another inspiring YouTube video by Colin Smith on Physics in Clojure [#]_, 
that ends with a *weird trick* [#]_ obtained by applying the exponential function not on a number but on the *differential operator*, which however is very similar to the called Laplace and Fourier transforms, that are on their turn strongly build on the exponential function as well.

I hope you found this article informative. Please, let me known when you liked it or have some questions or comments.


.. [#] `Wikipedia: Exponential function`_
.. [#] `Wikipedia: Leonhard Euler`_
.. [#] `Wikipedia: Taylor series`_
.. [#] `Wikipedia: Imaginary unit`_
.. [#] `Wikipedia: Euler's formula`_
.. [#] `Wikipedia: Quaternion`_
.. [#] `Wikipedia: Geometric algebra`_
.. [#] `Wikipedia: Pi`_
.. [#] `Wikipedia: Euler's identity`_
.. [#] `Wikipedia: Natural logarithm`_
.. [#] `Wikipedia: Differential equation`_
.. [#] `Wikipedia: Chain rule`_
.. [#] `Wikipedia: Matrix exponential`_
.. [#] `Wikipedia: Eigenvalues and eigenvectors`_
.. [#] `Wikipedia: Jordan normal form`_
.. [#] `Gilbert Strang, Diagonalizing a Matrix (YouTube MIT OpenCourseWare)`_
.. [#] `Gilbert Strang, The Matrix Exponential (YouTube MIT OpenCourseWare)`_
.. [#] `Wikipedia: State-space representation`_
.. [#] `Colin Smith, Physics in Clojure (YouTube Clojure/West)`_
.. [#] `Colin Smith, One weird trick (in\: Physics in Clojure at 38\:15)`_

.. _Wikipedia\: Exponential function: https://en.wikipedia.org/wiki/Exponential_function
.. _Wikipedia\: Leonhard Euler: https://en.wikipedia.org/wiki/Leonhard_Euler
.. _Wikipedia\: Taylor series: https://en.wikipedia.org/wiki/Taylor_series
.. _Wikipedia\: Imaginary unit: https://en.wikipedia.org/wiki/Imaginary_unit
.. _Wikipedia\: Euler's formula: https://en.wikipedia.org/wiki/Euler%27s_formula
.. _Wikipedia\: Quaternion: https://en.wikipedia.org/wiki/Quaternion
.. _Wikipedia\: Geometric algebra: https://en.wikipedia.org/wiki/Geometric_algebra
.. _Wikipedia\: Pi: https://en.wikipedia.org/wiki/Pi
.. _Wikipedia\: Euler's identity: https://en.wikipedia.org/wiki/Euler%27s_identity
.. _Wikipedia\: Natural logarithm: https://en.wikipedia.org/wiki/Natural_logarithm
.. _Wikipedia\: Differential equation: https://en.wikipedia.org/wiki/Differential_equation
.. _Wikipedia\: Chain rule: https://en.wikipedia.org/wiki/Chain_rule
.. _Wikipedia\: Matrix exponential: https://en.wikipedia.org/wiki/Matrix_exponential
.. _Wikipedia\: Eigenvalues and eigenvectors: https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors
.. _Wikipedia\: Jordan normal form: https://en.wikipedia.org/wiki/Jordan_normal_form
.. _Gilbert Strang, Diagonalizing a Matrix (YouTube MIT OpenCourseWare): https://youtu.be/U8R54zOTVLw
.. _Gilbert Strang, The Matrix Exponential (YouTube MIT OpenCourseWare): https://youtu.be/LwSk9M5lJx4
.. _Wikipedia\: State-space representation: https://en.wikipedia.org/wiki/State-space_representation
.. _Colin Smith, Physics in Clojure (YouTube Clojure/West): https://youtu.be/7PoajCqNKpg
.. _Colin Smith, One weird trick (in\: Physics in Clojure at 38\:15): https://youtu.be/7PoajCqNKpg?t=2295
