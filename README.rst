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


