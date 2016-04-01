
Infrastructure
========================

MPI requires a "low-latency" infrastructure for top performance.

.. image:: images/connection.png
    :align: center

The figure shows an MPI application running on two different systems.  One
system uses a 'fibre' interconnect, which are fiber optics cables that run at
56GB/s.  While the second system uses standard ethernet interconnect (which
runs at 10GB/s).  As you can see, the ethernet system starts to get hit with
significant performance penalties due to the slow network.

So we would not recommend simply plugging a bunch of workstatons together in
the lab using ethernet cables and trying to scale an application up.  You
should run these applications on high performance computing platforms.  Most
universities have HPC centers available to their researchers.  If not, the next
page will introduce you to XSEDE.  Which is the organization that includes many
nationally funded computing systems specifically catered to serve STEM
disciplines.
