# nounoup
Python adapter for the JVM-based nounou package for neurophysiology


## Which JVM => Python library to use?

We considered the following libraries

+  ___[Pyjnius](https://pyjnius.readthedocs.org/en/latest/)___... seems to be current (as of 11.2015) and usable, with reasonable overhead. Supported by many current blog entries for this use.
+  [Py4J](https://www.py4j.org/index.html)... seems to have much larger overhead due to RPC socket use
