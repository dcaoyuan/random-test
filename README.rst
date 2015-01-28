astore
======

Avro Data Store based on Akka (TODO persistence)

Core Design
^^^^^^^^^^^

-  Each record is an actor (non-blocking)
-  Akka sharding cluster (easy to scale-out)
-  Locate field/value deeply via
   `avpath <https://github.com/wandoulabs/avpath>`__
-  Scripting triggered by field updating events (JDK 8 JavaScript engine
   -
   `Nashorn <http://docs.oracle.com/javase/8/docs/technotes/guides/scripting/nashorn/>`__)

Run astore
^^^^^^^^^^

.. code:: shell

    $ sbt run

Or

.. code:: shell

    $ sbt clean compile dist
    $ ls target/universal/
    tmp  astore-0.1.1-SNAPSHOT.zip 

Then, copy astore-0.1.1.-SNAPSHOT.zip to somewhere and unzip it

.. code:: shell

    $ cd astore-0.1.1-SNAPSHOT/bin
    $ ./astore

