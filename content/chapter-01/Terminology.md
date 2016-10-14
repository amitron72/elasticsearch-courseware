# Terminology #

* Elasticsearch is a near real time search platform - not ACID (Atomicity, Consistency, Isolation, Durability) compliant
* Cluster is a collection of one or more nodes storing, indexing, and searching data
* Node is a single server in a cluster, nodes discover each other with unicast and by cluster name defined in /etc/elasticsearch/elasticsearch.yml
* Node can be configured as master-eligible, data, client, tribe, or left default: master-eligible and data node
* Index is a collection of documents and equivalent of Rdbms (Relational Database Management System) database or schema
* Type is a collection of documents of a specific type inside index, a loose equivalent of table in Rdbms
* Document is a basic unit of operation for indexing, replications, and searching. An approximate equivalent of a row/record in Rdbms. Document can be searched for in an index, but when being indexed must be assigned to a type
* Shards is a unit of storage and operation assigned to a node to distribute index across nodes in a cluster - to allow horizontal scalability
*  Replication supports high availability as in case of a node failure and improves scalability by allowing search operations on replicas