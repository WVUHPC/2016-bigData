
Parallel Code
=======================

::
    library (doParallel)
    cl <- makeCluster (2)

    registerDoParallel (cl)

    foreach ( i=1:3 ) %dopar% sqrt (i)


