
Measuring Time
---------------

A simple way to measure execution time of a program is to use the unix time
program::

    time sort input.txt

The output will give three times labeled, real, system and user.  We are
interested in the real time, since this represents execution time from start to
finish.

Since the goal here is to produce a standard graph, you are going to want to
'time' your program/code with different input sizes.  Breaking up the input to
appropriate sizes is completely application dependent, and largely depends on
the type of input.  Your input might be a million samples, and therefore you
could 'time' program exeuction on 1000, 10000, 25000, 50000, and 100000
samples.  The goal here is to simply see how execution time responds to
different input sizes, so you don't need to scale your samples very high.  But
you do want to get at least 4 points, and have them spaced to create a clear
graph.
