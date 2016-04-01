
Parallel CLI
===================================================

If you are using an existing third party application to process your data, you
might already have parallel computing available to you.  You would have to
specify it on the command-line.  The most common forms of the '-p', '-np', or
'--parallel' options.  These options are almost always followed by a number
indicating a processor count::

    sort --parallel 8 ...

Another example might be::

    bowtie2 -p 4 ...

Some applications, however, allows parallel computing but does not require
specification of processors on the command-line.  They are controlled by an
environment variable 'OMP_NUM_THREADS'.  These applications are utilizing the
openMP library - and it is a very common paradigm to add parallel computing to
applications::

    export OMP_NUM_THREADS=8

Gromacs, a popular molecular dynamic program, is controlled this way.

.. tip:: Check the documenation of your application, specifically looking for
    sections outlining parallel computing.  It's important to be able to
    recognize what type of parallel computing your application offers.  If your
    program uses OMP_NUM_THREADS, or uses -p, -np, etc... to specify processor
    number - then it almost certainly uses shared parallel computing.  And
    therefore, it will not be adequate to alleviate memory usage limitations.
