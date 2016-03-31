
What is "big Data"
==================

"big Data" has numerous definitions - and it's variation of application is
always tied to context.  There are added difficulties for just producing large
data sets - specifially what techniques you will use.  Additionally,
statistical tests and method applications often need to be modified when
working with big Data.  However, these difficulties are research field
dependent, and frankly, often researchers do not have difficulty figuring out
which methods need to be used given their problem size.  This is almost always
covered in their research training.  So none of these issues will be discussed
in this manual.

Here, we use a more practical approach to defining big Data.  Any data set that
exceeds practical computing time and/or memory limits of existing hardware is
big Data.  And the threshold limits of these parameters ( time and memory ), is
also contextual.  If your existing workstation has only 8GB of RAM, any data
set that uses more than 8GB will create difficulties for you to compute on it.
Additionally, time is contextual as well.  A workflow might take 45 days to
compute.  But if you are doing this only once, you might easily be able to deal
wih this time constraint (work on another project in the meantime for
instance).  However, if you need to run this same workflow 2000 times, now 45
days per instance will create an extreme burden to you.  If your wondering, it
would take over 246 years if you did not adjust that compute time to run 2000
instances back to back.

Therefore, our practical definition of big Data is any data set that produces a
need to either reduce compute time, reduce memory usage, or both.  And
depending on which needs you have, an appropriate solution emerges.

.. csv-table:: Solution Set
    :header: "Limitation", "Solution"
    
    time only, parallel computing
    memory only, distributed computing
    time and memory, distributed computing

