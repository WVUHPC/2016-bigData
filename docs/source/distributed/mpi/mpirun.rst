
MPIRUN
===========================

MPIRUN is the command used to initiate distributed parallel computing
applications.  Applications that utilize distributed computing are executed
using something similar to::

    mpirun -np 120 -hostfile $PBS_NODEFILE xhpl

Each system is different, depending on how the mpi libraries where compiled and
configured.  Some systems us 'aprun', 'mpiexec', or something similar.  You
will have to consult your system documentation.  
