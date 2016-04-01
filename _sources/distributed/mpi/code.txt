
MPI code
==================

Parallel distributed computing is always done through the Message Passing
Interface (MPI).  `MPI <http://www.mcs.anl.gov/research/projects/mpi/>`_ is the 
parallel computing standard.  As such, almost all distributed computing
applications rely on MPI.

If your application requires the use of MPI, we strongly encourage that you
should use C or fortran as an implementation.  However, we recognize that this
requires a large learning curve associated with learning a lower level langauge
like C.  Our thoughts are generally that if you require this amount of
performance, other factors beside simply message passing is often required to
make the application tenable.  

MPI using R
^^^^^^^^^^^^

However, some smaller applications can get away with using R for MPI.  The
`pbdMPI <https://cran.r-project.org/web/packages/pbdMPI/index.html>`_ package is
currently the best MPI implementation in R.  However, the package is some what
poorly documentated.  In that they expect some familiarity with the MPI
standard to understand what their functions do.

C/fortran MPI implementations
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

There are several implementations of the MPI standard for C and fortran.  They
all offer mostly the same functionality, however, there are some 
differences.  Largely, for most programmers they are interchangable. 

* `openMPI <https://www.open-mpi.org/>`_
* `MPICH <http://www.mpich.org/>`_
* `MVAPICH <http://mvapich.cse.ohio-state.edu/>`_


