---
title: Enable Apache Kafka health monitoring
description: Set configurations in the Apache HTTP server application to enable the Agent Client Collector to perform Apache Kafka HTTP server monitoring.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Enable Apache Kafka health monitoring

Set configurations in the Apache HTTP server application to enable the Agent Client Collector to perform Apache Kafka HTTP server monitoring.

## Before you begin

-   Enable Java Management Extensions \(JMX\) for Kafka metric collection by running the following command:

    ```
    Environment=”JMX_PORT=9999”
    ```

-   Role required: agent\_client\_collector\_admin

## Procedure

1.  Enable collecting Apache Kafka performance metrics using Java Management Extensions \(JMX\) by running the following command:

    ```
    JMX_PORT=9999 bin/kafka-server-start.sh config/server.properties
    ```

2.  Configure the admin server port by modifying the port number of the admin.serverPort property in the zookeeper.properties file.

    The default port is 8080.


**Parent Topic:**[Agent Client Collector deployment - shared between servers and endpoints](../concept/acc-shared-deployment.md)

