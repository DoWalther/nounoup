# nounoup
Python adapter for the JVM-based nounou package for neurophysiology


## Which JVM => Python library to use?

We considered the following libraries

+  ___[Pyjnius](https://pyjnius.readthedocs.org/en/latest/)___... seems to be current (as of 11.2015) and usable, with reasonable overhead. Supported by many current blog entries for this use.
+  [Py4J](https://www.py4j.org/index.html)... seems to have much larger overhead due to RPC socket use
+  Other libraries such as [jep](https://pypi.python.org/pypi/jep) are available for accessing Python from Java (other direction)

Because of problems with importing the ___[Pyjnius](https://pyjnius.readthedocs.org/en/latest/)___ library(ImportError: DLL load failed, we tried [Py4J](https://www.py4j.org/index.html). It is possible to import py4j, but we can't run the JVM. 

+ [javabridge] (https://pypi.python.org/pypi/javabridge) .. is the only working library so far.

## Dependencies
+ [numpy](https://pypi.python.org/pypi/numpy/1.10.1)
+ [nose] (https://pypi.python.org/pypi/nose/1.3.7)
+ [JDK 64Bit] (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
+ 32Bit Python for example [Anaconda](https://www.continuum.io/downloads)

## Getting started
Before you run the setup.py file you need to install Java SE Development Kit 8u66(64Bit).

###### Setting JAVA_HOME environment variable

1. Find out where Java is installed. If you didn't change the path during installation, it will be something like this:        
  *C:\Program Files (x86)\Java\jdk1.8.0_66*
2. In Windows 7 right click **My Computer** and select **Properties** > **Advanced**.
3. Click the **Environment Variables** button.
4. Under **System Variables**, click **New**.
5. In the **Variable Name** field, enter:                                                                                      
  *JAVA_HOME*
6. In the **Variable Value** field, enter your JDK installation path.

## Installation

+ Change the directory to the javabridge folder.
+ You are now able to run the setup.py file.  *python setup.py install*.
+ After successful installation you should do the unit test. *python setup.py develop* and *python setup.py nosetests*
+ The result should be something like this:  Ran 159 tests in 0.771s                                                                                                        OK
