
Parallel Code
=======================

When applying parallel computing to your own code.  The easiest method is to
use packages available for your language of choice.  Most languages have
packages that practically automate parallel computing, especially around for
loops.  An example::

    library (doParallel)
    cl <- makeCluster (2)

    registerDoParallel (cl)

    foreach ( i=1:3 ) %dopar% sqrt (i)

This is in the R language, and uses the doParallel package, which is an
extension of the parallel package which comes shipped with R.  R has built-in
functions that can parallelize any of the apply functions and foreach loops,
which are large sources of time limits.

    - `Getting started with doParallel
      <https://cran.r-project.org/web/packages/doParallel/vignettes/gettingstartedParallel.pdf>`_
    - `Parallel package
      <http://stat.ethz.ch/R-manual/R-devel/library/parallel/doc/parallel.pdf>`_

.. warning:: The parallel package should not be used for distributed computing.
    While some examples exist where you can put processors on different
    servers, the package does not employ a true SSMD (single source multiple
    data) paradigm.  Which means the parallel package will not provide
    solutions to memory limitations.

Python modules
^^^^^^^^^^^^^^

Python has some built-in ability to perform parallel computing using the
`multiprocessing <https://docs.python.org/3/library/multiprocessing.html>`_
module.  However, due to a 'Global lock interpreter' python's parallel
computing capacity is limited.  Nonetheless, multiprocessing module can provide
parallel computing surrounding simple parallel tasks (for loops, for instance).

C/Fortran
^^^^^^^^^^

C and Fortran users should use `openMP <http://openmp.org/wp/>`_ which has
greatly simplified the interface for parallel programming.  Tutorials are
offered on their `resource <http://openmp.org/wp/resources/#Tutorials>`_ page.
