
R Tabular Data
===============

.. image:: ../../../images/diagrams/tabular/tabularRcode.png


Algorithm Efficiency
====================

Using linux core utilities. ::

    cut -b 69 | awk '{ if ( $1=="F" ) s = s + 1 } END { print s, NR-s }'


This code took 5.679 seconds to run.  Giving exactly the same answer.
