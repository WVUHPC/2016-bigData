
This manual provides a very concise and practical guide to steps that can be
taken to alleviate limitations created by computing on 'big data'.  We tailored
this documentation specifically for non-computer scientist; despite keeping
this practical advice grounded in sound computing theory.  The focus was to
present clear steps that can be taken to quickly identify which limitations are
present in your own scientific workflows, and which approaches can be taken to
overcome them.  The target audience is academic researchers that have reached
the limits of their workstations, and are moving their research to parallel
methods to make them more practical in the face of growing data set size.
Additionally, we assume that the reader's primary goal is not to develop
sofware, or push thersholds of computing.  Rather, they would like to proceed
with the smallest allowable modifcations to accomplish the needs of their
workflows.  Therefore, we do not present any heavy theoretical work here, nor
do we expect a knowledge of algorithms or computer architecture.  However, we
do assume that the reader has some familiarity with Linux/Unix type systems,
and have knowledge of how to execute commands on the command-line.  More
narrowly, we assume the reader already has a working workflow, either one they
obtained from a third party, or one they wrote, most likely in a higher level
lanague such as R or python.  Consequently, the workflow works fine under
modest data sizes, however when large sets are fed into the workflow, either
the compute time becomes impractical or the memory usage exceeds the bounds of
the computer.  The following manual will guide you to where to go from here.

.. toctree::
   :maxdepth: 2

   intro
   shared/intro
   distributed/intro
   xsede
