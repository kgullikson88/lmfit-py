.. lmfit documentation master file,

Non-Linear Least-Square Minimization and Curve-Fitting for Python
===========================================================================

.. _Levenberg-Marquardt:     http://en.wikipedia.org/wiki/Levenberg-Marquardt_algorithm
.. _MINPACK-1:               http://en.wikipedia.org/wiki/MINPACK


Lmfit provides a high-level interface to non-linear optimization and
curve fitting problems for Python. Lmfit builds on
`Levenberg-Marquardt`_ algorithm of :func:`scipy.optimize.leastsq`, but
also supports most of the optimization methods from :mod:`scipy.optimize`.
It has a number of useful enhancements, including:

  * Using :class:`Parameter` objects instead of plain floats as variables.
    A :class:`Parameter` has a value that can be varied in the fit, fixed,
    have upper and/or lower bounds.  It can even have a value that is
    constrained by an algebraic expression of other Parameter values.

  * Ease of changing fitting algorithms.  Once a fitting model is set up,
    one can change the fitting algorithm without changing the objective
    function.

  * Improved estimation of confidence intervals.  While
    :func:`scipy.optimize.leastsq` will automatically calculate
    uncertainties and correlations from the covariance matrix, lmfit also
    has functions to explicitly explore parameter space to determine
    confidence levels even for the most difficult cases.

  * Improved curve-fitting with the :class:`Model` class.  This which
    extends the capabilities of :func:`scipy.optimize.curve_fit`, allowing
    you to turn a function that models for your data into a python class
    that helps you parametrize and fit data with that model.

  * Many :ref:`pre-built models <builtin_models_chapter>` for common
    lineshapes are included and ready to use.

.. _lmfit github repository:   http://github.com/lmfit/lmfit-py

The lmfit package is Free software, using an MIT license.  The software and
this document are works in progress.  If you are interested in
participating in this effort please use the `lmfit github repository`_.


.. toctree::
   :maxdepth: 2

   intro
   installation
   parameters
   fitting
   model
   builtin_models
   confidence
   bounds
   constraints



