
Measuring Memory
----------------

The de facto standard for measuring memory is using the linux tool `valgrind
<http://valgrind.org/>`_.  Valgrind comes with many different options and tools
that are useful to coders.  But for memory usage discovery, we want to use the
'`massif <http://valgrind.org/docs/manual/ms-manual.html>`_' tool::

    valgrind --tool=massif sort input.txt

Valgrind will take snapshots of memory usage of your program/code.  When the
execution of the program is finished, a file in the format of
'massif.out.99999' will be in the directory valgrind was started from.  You can
control the output filename using the '--massif-out-file' option::

    valgrind --tool=massif --massif-out-file=1000-samples sort input.txt

One convienant approach is the name the outfiles with the input size.  This way
you can easily identify which files goes with which problem size.  To read the
files, you use the 'ms_print' tool, which is bundled with valgrind::

    ms_print 1000-samples

ms_print will output a lot of text.  The most useful part of the file, is the
'Detailed snapshots' line, which occurs usually within the first 25 lines of
output::

    ms_print massif.out.34625 | less

Here is some sections of the output::

    Detailed snapshots: [1 (peak), 6, 9, 19, 22, 29, 32, 43]

    --------------------------------------------------------------------------------
    n        time(i)         total(B)   useful-heap(B) extra-heap(B) stacks(B)
    --------------------------------------------------------------------------------
     0              0                0                0             0 0
     1 10,916,110,628       51,389,792       51,385,123         4,669 0
       

One of the snapshots will be labeled with '(peak)'.  In this case
snapshot 1 is the peak snapshot.  Scroll down the the file and find the table
that has the information for snapshot 1.  I see that the program used
51,389,792 total bytes (B).  Which is about 49 MB of RAM.  Accuracy is not
important, so you could just call this 51 MB of RAM (using 1000 as a conversion
instead of the proper 1024).  The goal is to observe the general trend in
memory usage, not obtain exact measurements.

.. warning:: Do not run valgrind and time in the same command.  valgrind seriously slows down a programs execution time, and will therefore skew the data.


