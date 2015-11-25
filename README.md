# nounoup
Python adapter for the JVM-based nounou package for neurophysiology


## Which JVM => Python library to use?

We considered the following libraries

+  ___[Pyjnius](https://pyjnius.readthedocs.org/en/latest/)___... seems to be current (as of 11.2015) and usable, with reasonable overhead. Supported by many current blog entries for this use.
+  [Py4J](https://www.py4j.org/index.html)... seems to have much larger overhead due to RPC socket use
+  Other libraries such as [jep](https://pypi.python.org/pypi/jep) are available for accessing Python from Java (other direction)

Because of problems during the installation with ___[Pyjnius](https://pyjnius.readthedocs.org/en/latest/)___ ( pip and setup.py doesn't work), we tried [Py4J](https://www.py4j.org/index.html). After successfull installation we weren't able to run the JVM.

+ [javabridge] (https://pypi.python.org/pypi/javabridge) .. is the only working library so far.
