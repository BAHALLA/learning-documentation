# Apache Kafka

> **Apache Kafka** is a distributed event-streaming platform used for high-performance data pipelines, streaming analytics, and event-driven applications.

---

## ZooKeeper’s Role (Legacy)

!!! info "Overview"
    ZooKeeper was traditionally used to manage the **state of a Kafka cluster**, including:
    
    * Cluster membership  
    * Leader elections  

!!! warning "Since Kafka 4.x"
    Kafka **no longer requires ZooKeeper**.  
    The **KRaft (Kafka Raft)** mode fully replaces it.

---

## KRaft Mode

!!! success "Definition"
    **KRaft (Kafka Raft)** is Kafka’s built-in consensus protocol that lets Kafka manage its **own metadata** without ZooKeeper.

| Node Type      | Responsibilities                                   |
|-----------------|----------------------------------------------------|
| **Controller** | Maintains cluster metadata, leader election, configs |
| **Broker**     | Handles client traffic and persists topic data       |

---

## Message Ordering

!!! quote "Guarantee"
    Kafka **guarantees message order only within a single partition**.

For example, if messages `M1` and `M2` are sent to **partition `P0`**,  
a consumer `C1` will always read **`M1` before `M2`**.

!!! warning "Important"
    Kafka **does not guarantee order across different partitions**.


