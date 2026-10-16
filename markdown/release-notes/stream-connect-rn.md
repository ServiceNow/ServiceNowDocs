---
title: Stream Connect release notes
description: The ServiceNow Stream Connect application links your Apache Kafka environment to your ServiceNow instance, enabling you to stream data between your instance and your external systems. See the following sections for release notes by version.The Brazil release adds Stream Producer to automatically stream changes from Stream Connect tables to Kafka topics, and enables OAUTHBEARER authentication for message replication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/stream-connect-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Stream Connect release notes

The ServiceNow® Stream Connect application links your Apache Kafka environment to your ServiceNow instance, enabling you to stream data between your instance and your external systems. See the following sections for release notes by version.

## About Stream Connect

-   Publish and process Kafka events at scale. Publish events to your Kafka environment from your ServiceNow instance and consume Kafka events from your external systems at a high volume with low latency.
-   Build flows that produce and consume Kafka events. Stream Connect is integrated with Workflow Studio, providing a low-code way to publish and process Kafka messages.
-   Import and process data from your Kafka environment using your own scripts or your existing Robust Transform Engine \(RTE\) or transform map configurations.
-   Monitor consumer and producer performance with detailed reporting of statistics and performance metrics.
-   Integrate your ServiceNow instance directly with your local Kafka environment with Direct Kafka.

See [Using Stream Connect for Apache Kafka](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/stream-connect-apache-kafka.md) for more information.

## Activation and other requirements

-   **Activation information**

    Stream Connect requires a Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html). The Stream Connect Dashboard is available from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/build-automate-rn-landing.md)

## Brazil Early Availability

The Brazil release adds Stream Producer to automatically stream changes from Stream Connect tables to Kafka topics, and enables OAUTHBEARER authentication for message replication.

### What's new

-   **[Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/stream-producer.md)**

    Automatically stream changes from ServiceNow tables to Kafka topics with Stream Producer. Stream Producer uses change data capture \(CDC\) technology to capture inserts, updates, and deletes on selected tables. The captured changes are formatted as messages and sent to a Kafka topic, enabling real-time data synchronization with external applications.

-   **[Stream Producer schemas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/schema-management.md)**

    Stream Producer supports the Avro serialization format for message payloads. When using an Avro format, Stream Producer uses the selected table's auto-generated schema to convert CDC payloads to Avro before sending them to Kafka.

-   **[OAUTHBEARER authentication for Stream Connect message replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-data-input-kafka-credentials.md)**

    Authenticate using OAUTHBEARER as part of the SASL credential framework for Stream Connect message replication. OAUTHBEARER authentication lets Stream Connect administrators meet customer requirements, improve security, and align with existing OAuth capabilities on the platform, enabling seamless integration with Kafka environments that require advanced authentication.

-   **[Stream Connect Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/stream-connect-dashboard.md)**

    Use the Stream Connect Dashboard to view data for Stream Producers, including the number of messages and bytes produced, the rate of production, and the number of messages still pending. Monitor and analyze Stream Producer performance with the Stream Producer CDC Statistics section on each Stream Producer's page. The Stream Connect Dashboard is available from the ServiceNow Store.


### Plugin information

-   **New plugins**

    ServiceNow Stream Producer \(`com.glide.hub.stream_connect.stream_producer`\): Adds Stream Producer capabilities.


