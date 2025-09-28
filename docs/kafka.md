# Apache Kafka

This page is dedicated to questions and answers about Apache Kafka.

## Questions

### What is the role of ZooKeeper in Kafka?

> ZooKeeper was traditionally used to manage the state of a Kafka cluster, including cluster membership and leader elections. However, since Kafka version 4.x, ZooKeeper is no longer required and has been replaced by KRaft mode.

### What is KRaft mode?

> KRaft (Kafka Raft) is the consensus protocol that allows you to run Kafka without ZooKeeper. This new mode, referred to as "KRaft mode", simplifies Kafka's architecture by having Kafka manage its own metadata internally.
> 
> In a KRaft-based cluster, there are two types of nodes:
> * **Controllers**: These nodes are responsible for managing the cluster's metadata, including leadership, membership, and configurations.
> * **Brokers**: These are the usual cluster nodes that handle client traffic and data storage.

### How does Kafka guarantee message order?

> Kafka guarantees message order only within a single partition of a topic. If messages `M1` and `M2` are sent to the same partition `P0`, a consumer `C1` is guaranteed to read `M1` before `M2`. However, Kafka does not guarantee order across different partitions.