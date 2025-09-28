# Apache Kafka

This page is dedicated to questions and answers about Apache Kafka.

## Questions

### What is the role of ZooKeeper in Kafka?

> ZooKeeper manages the Kafka cluster state, including membership and leadership. Since version 4.x, ZooKeeper is no longer used and has been replaced by KRaft mode.

### How does Kafka guarantee message order?

> Kafka guarantees message order within a topic's partition. For example, if messages `M1` and `M2` are sent to the same partition `P0`, a consumer `C1` is guaranteed to read `M1` before `M2`.


### What is the difference between a topic and a partition?

*Answer goes here*
