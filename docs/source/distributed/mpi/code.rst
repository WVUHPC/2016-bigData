
MPI code examples
==================

A simple pbdMPI code example::

    library ( pbdMPI )

    init ()
    .comm.size <- comm.size ()
    .comm.rank <- comm.rank ()

    N <- 5
    x <- (1:N) + N * .comm.rank

    if ( .comm.rank == 0 ) {
        send ( x )
    } else if ( .comm.rank == 1 ) {
        y <- recv ( x )
    }

    comm.print ( y, rank.print = 1 )

    finalize ()

Explanation of this code set.

Another MPI code example in R::

    suppressMessages ( library ( pbdMPI, quietly = T ) )

    init ()
    .comm.size <- comm.size ()
    .comm.rank <- comm.rank ()

    x <- sample ( 1:1000, 50, replace = T )

    x_global <- reduce ( y, op = "sum" )

    comm.print ( x_global, rank.print == 0 )

    finalize ()

And this should be finished.
