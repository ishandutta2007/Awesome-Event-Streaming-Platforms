# Awesome-Event-Streaming-Platforms

# Top Event Streaming Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Distributed Logs, Pub/Sub Messaging & Self-Hosted Streaming Infrastructure*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Event Streaming Platforms**. These systems provide durable, ordered, replayable logs for high-throughput event ingestion, real-time data pipelines, and event-driven microservices—forming the backbone of modern data architectures.

**Examples** include Confluent Cloud, Amazon MSK, Redpanda Cloud, Azure Event Hubs, Google Cloud Pub/Sub, IBM MQ, Solace PubSub+, HiveMQ, and Apache Kafka (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, protocol compatibility, and transparent streaming infrastructure—ideal for teams that need data sovereignty, avoid per-message SaaS fees, and require auditable event pipelines. The open-source landscape is anchored by **Apache Kafka** (the distributed log standard with 30,000+ GitHub stars), **Redpanda** (Kafka-compatible without JVM or ZooKeeper), and **Apache Pulsar** (separated compute/storage with multi-tenancy), with specialized brokers like **HiveMQ** for MQTT/IoT ingestion.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Confluent Cloud](https://www.confluent.io/confluent-cloud/)**  
  Fully managed Kafka service from the company founded by Kafka's creators. Offers Schema Registry, ksqlDB, and Connectors as managed add-ons. The reference platform for teams that want Kafka without operational burden. Note: IBM completed its acquisition of Confluent in March 2026 .

- **[Amazon MSK](https://aws.amazon.com/msk/)**  
  AWS's managed Kafka service with IAM, mTLS, and SASL/SCRAM authentication. Integrates with CloudWatch for metrics and S3/CloudWatch/Firehose for log delivery. Best for AWS-native architectures requiring managed Kafka.

- **[Redpanda Cloud](https://redpanda.com/cloud)**  
  Kafka-compatible streaming platform with Serverless, Dedicated, and BYOC deployment options. Serverless tier bills by ingress, egress, partitions, and retained data. Provides native Kafka protocol support, so existing clients connect without code changes .

- **[Azure Event Hubs](https://azure.microsoft.com/en-us/products/event-hubs/)**  
  Azure's native event streaming platform with built-in Apache Kafka compatibility. Standard tier supports 1MB max event size and 7-day retention; Premium extends to 90-day retention and 100 consumer groups. Best for Azure-native workloads wanting Kafka compatibility.

- **[Google Cloud Pub/Sub](https://cloud.google.com/pubsub)**  
  Google's globally distributed messaging service. Not natively Kafka-compatible—migration requires client changes. Supports message ordering via ordering keys, dead-letter topics, and up to 31 days retention. Best for GCP-native architectures that don't require Kafka protocol.

- **[IBM MQ](https://www.ibm.com/products/mq)**  
  Enterprise messaging middleware with deep mainframe and IBM ecosystem integration. Reliable, secure, and scalable for mission-critical integration. Proprietary and typically enterprise-priced.

- **[Solace PubSub+](https://solace.com/)**  
  Event streaming and management platform supporting multiple protocols (AMQP, MQTT, JMS, REST) with a unified broker. Strong for hybrid cloud and IoT use cases.

- **[CloudKarafka](https://www.cloudkarafka.com/)**  
  Hosted Apache Kafka service. **Note**: CloudKarafka has been discontinued and is in brownout mode . The official FAQ page title confirms "Service Discontinued" . Not recommended for new deployments.

- **[HiveMQ Cloud](https://www.hivemq.com/)**  
  Managed MQTT broker for IoT and event-driven architectures. The open-source HiveMQ Community Edition can be self-hosted; the cloud tier adds managed infrastructure and enterprise features.

## Open-Source GitHub Projects

- **[Apache Kafka](https://github.com/apache/kafka)**  
  The distributed event streaming platform standard. High-throughput, fault-tolerant, durable log storage with the deepest ecosystem: Kafka Connect, Kafka Streams, ksqlDB, and hundreds of maintained connectors . Apache 2.0 licensed with 30,000+ GitHub stars . Requires JVM and (historically) ZooKeeper, though KRaft mode eliminates ZooKeeper in newer versions. Best for organizations that need the full Kafka ecosystem and can manage operational complexity.

- **[Redpanda](https://github.com/redpanda-data/redpanda)**  
  Kafka API-compatible streaming platform built in C++ with no JVM or ZooKeeper. Provides **native Kafka protocol support**, meaning existing Kafka clients work without code changes—unlike translation-layer approaches . Lower operational overhead and lower latency than standard Kafka, with 220+ connectors via Redpanda Connect . Source-available under BSL with a free Community Edition. Best for latency-sensitive or cost-sensitive workloads that want Kafka compatibility without Kafka's operational weight.

- **[Apache Pulsar](https://github.com/apache/pulsar)**  
  Distributed pub-sub messaging system with **separated compute and storage layers**, enabling independent scaling and stronger native multi-tenancy than Kafka . Supports tiered storage, geo-replication, and durable subscriptions. Kafka compatibility runs through a separate protocol handler rather than native wire protocol, so migration requires testing and may lag on newer Kafka features . Best for organizations that need multi-tenant event streaming with independent scaling of serving and storage.

- **[HiveMQ Community Edition](https://github.com/hivemq/hivemq-community-edition)**  
  Java-based open-source MQTT broker fully supporting MQTT 3.x and MQTT 5. Apache 2.0 licensed . The technical core of HiveMQ's enterprise platform. Best for IoT ingestion pipelines requiring MQTT protocol support and a plugin-based architecture.

- **[Apache RocketMQ](https://github.com/apache/rocketmq)**  
  Cloud-native messaging and streaming platform with low latency and high throughput. Java-based, Apache 2.0 licensed. Popular in Chinese enterprise environments. Best for teams that need a Kafka alternative with different tradeoffs in transactional messaging and Kubernetes-native operation.

- **[Apache ActiveMQ](https://github.com/apache/activemq)**  
  High-performance multi-protocol message broker supporting JMS, AMQP, MQTT, and STOMP. Apache 2.0 licensed, Apache top-level project. Best for JMS-centric enterprise environments and legacy Java integration.

- **[RabbitMQ](https://github.com/rabbitmq/rabbitmq-server)**  
  Mature, widely-deployed open-source message broker supporting AMQP, MQTT, and STOMP. Flexible routing via exchanges and queues. Best for traditional message queue workloads and microservices communication requiring complex routing logic.

- **[Eclipse Mosquitto](https://github.com/eclipse/mosquitto)**  
  Lightweight open-source MQTT broker written in C. Fully supports MQTT 3.1 and 3.1.1. Small footprint makes it suitable for constrained devices and edge deployments. Best for resource-constrained IoT gateways.

- **[Eclipse Zenoh](https://github.com/eclipse-zenoh/zenoh)**  
  Next-generation pub-sub/overlay protocol with native bridges to MQTT, Kafka, and WebSocket. Dual-licensed EPL-2.0/Apache-2.0. Best for robotic, edge, and WAN-spanning deployments where traditional brokers become bottlenecks.

### Additional Strong Open-Source Options

- **Numaflow** — Kubernetes-native, language-agnostic platform for scalable event-driven applications .
- **AutoMQ** — Serverless Kafka alternative built on S3, claiming 10x cost savings with full Kafka compatibility. Apache-2.0 licensed with 10,000+ stars .
- **Timeplus** — Lightweight stream processing platform deployed as a single binary, optimized for real-time analytics .
- **Apache Qpid** — AMQP-compliant messaging tools with multi-language support. Best for AMQP-centric enterprise integration.
- **Frameworks for building custom systems**: Pair **Apache Kafka** as the durable event backbone with **HiveMQ** for MQTT/IoT ingestion. Use **Redpanda** when Kafka compatibility is required but operational simplicity matters. Choose **Pulsar** when multi-tenancy and independent storage scaling are priorities. For edge deployments, **Mosquitto** provides lightweight MQTT brokering.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Event streaming platforms vary significantly in throughput characteristics, operational complexity, and protocol support; benchmark against your workload before committing.
- "Kafka-compatible" services may not implement every Kafka feature; verify protocol compatibility (transactions, exactly-once semantics, Schema Registry) before migrating production workloads .
- Self-hosted streaming infrastructure requires proper cluster sizing, replication configuration, monitoring, and disaster recovery planning.
- CloudKarafka has been discontinued and should not be selected for new projects .

---

**Made for data engineers, platform teams, IoT architects, and developers building real-time event-driven systems.**  
Let's make event streaming more open, compatible, and accessible.
