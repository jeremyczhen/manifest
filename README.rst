How to build FDBus Development Kit (FDK)
=========================================
Prepare run-time for buildCentral
===================================
1) Install python from `Python <https://www.python.org/downloads/>`_
2) > sudo pip install python-magic
3) > sudo pip install networkx
4) > sudo pip install simplejson

Download FDK
===============
1) > repo init -u https://github.com/jeremyczhen/manifest.git
2) > repo sync
3) > cd buildCentral

Build FDK
==========
For more details please refer to `buildCentral <https://github.com/jeremyczhen/buildCentral>`_

Build 1: host - Ubuntu; target - Ubuntu
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
1) > ./mk -thost
2) Binaries and headers are installed at output/stage/host/

Build 2: host - Ubuntu; target - ARM Linux
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
1) > ./mk -tarm-linux
2) Binaries and headers are installed at output/stage/arm-linux/

Build 3: host - Windows; target - Windows
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
1) > make sure Microsoft Visual Studio is installed
2) > mk -thost -g vs16
3) All visual Studio solutions are located at output\build\default\
4) Open the solutions and build in the following order:
 protobuf/ -> fdbus/ -> protobus/

