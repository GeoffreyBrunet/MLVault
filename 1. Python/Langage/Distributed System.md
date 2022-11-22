**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language

# Definitions
It consist of multiple systems connected together through a network. Each node in the network execute on a part of input / computation and communicates via the network using specially designed software.
Distributed computing softwares / frameworks / modules (like [Hadoop](https://hadoop.apache.org), [Spark](https://spark.apache.org), [[Dask]], [Celery](https://docs.celeryq.dev/en/stable/) and so on) collect the data from multiple nodes and joins (or merges) them together to be viewed at the master / central node.

# Advantages
- Allows computation of huge data which was otherwise not possible to done on single machine.
- Generally distributed systems are designed in such a way that failure of single system / node does not lead to failure of complete network.
- Incrementally increase computation power by simply adding more nodes.
- Improved performance through multitude of nodes and resources avaible for processing.