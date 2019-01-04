Part seven: Set up java, go and node environment.
========================================================
================
download file
================
`Java`__

.. __: https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html
**Note** choose accept like following.

.. image:: /source/image/java.png

Go download gox.xx.linux-amd64.tar.gz	

`Go`__

.. __: https://golang.org/dl/

`Go download for Chinese`__

.. __: https://studygolang.com/dl

`Node`__

.. __: https://nodejs.org/en/download/


=======================
Unzip file downloaded
=======================
Open a nautilus with ``sudo nautilus``, then unzip our downloaded file.
Go move its child folder named **go**,
Java rename it java,
Node rename it node.
then copy above folder into **/usr/local** folder.


=======================
Edit profile
=======================
``sudo gedit /etc/profile``, then we need to add to some text in the profile opened like following.

.. code-block:: shell

    export GOROOT=/usr/local/go
    export GOARCH=amd64
    export GOOS=linux
    export GOPATH=/home/username/gopath
    export GOBIN=$GOROOT/bin
    export PATH=$GOPATH/bin:$GOROOT/bin:$PATH

**You need to change username**

.. code-block:: shell

    export JAVA_HOME=/usr/local/java
    export JRE_HOME=/usr/local/java/jre
    export CLASSPATH=.:$JAVA_HOME/lib:$JRE_HOME/lib:$CLASSPATH
    export PATH=$JAVA_HOME/bin:$JRE_HOME/bin:$PATH

**Node need command, do not add following into profile.** 
``sudo ln -s /usr/local/node/bin /usr/local/share/bin``

``sudo ln -s /usr/local/node/npm /usr/local/share/bin``


====================
Make profile work
====================
``source /etc/profile``


=======================
Check environment
=======================
**Java:**
``java version``

**Go:**
``go env``

**node:**
``node -v``