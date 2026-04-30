---
title: Hermes Messaging Service release notes
description: The ServiceNow Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow instance. Hermes Messaging Service was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Hermes Messaging Service release notes

The ServiceNow® Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow® instance. Hermes Messaging Service was enhanced and updated in the Xanadu release.

## Hermes Messaging Service highlights for the Xanadu release

-   Publish events from your ServiceNow instance to your Apache Kafka environment and consume high volumes of Apache Kafka events from your external systems with low latency.
-   Effectively process spikes and bursts in message volume from external systems to minimize performance impacts on your instance.
-   Manage the health and performance of message delivery using Hermes diagnostic tools.

See [Hermes Messaging Service](https://www.servicenow.com/docs/access?context=hermes-messaging-service&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Monitor Hermes data usage](https://www.servicenow.com/docs/access?context=monitoring-data-usage-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Monitor data usage by application and track data usage by topic using the Hermes Usage Dashboard.


## Changed in this release

-   **[Monitor topics in multiple cluster sets](https://www.servicenow.com/docs/access?context=view-messages-hermes-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    View messages from multiple cluster sets by selecting a service group in the Hermes Topic Inspector module.

-   **[Test connectivity to multiple cluster sets](https://www.servicenow.com/docs/access?context=run-hermes-messaging-service-diagnostics&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Verify that your instance can send messages to and receive messages from multiple cluster sets by selecting a service group in the Hermes Diagnostics module.


## Activation information

Hermes Messaging Service is a ServiceNow AI Platform feature that is available with activation of the ServiceNow Stream Connect Installer \(com.glide.hub.stream\_connect.installer\) plugin or installation of the Log Export Service application. For details, see [Hermes Messaging Service activation](https://www.servicenow.com/docs/access?context=hermes-messaging-service-activation&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Using Stream Connect for Apache Kafka](https://www.servicenow.com/docs/access?context=stream-connect-apache-kafka&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Produce Apache Kafka messages from your ServiceNow instance using Workflow Studio, and then consume the messages in an external application. You can also produce Apache Kafka messages from an external application and then consume the messages in your ServiceNow instance using a variety of consumers with Stream Connect.

-   **[Log Export Service \(LES\)](https://www.servicenow.com/docs/access?context=les-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Export log data securely to your external data lake for reporting, auditing, or regulatory purposes using Hermes Messaging Service with Log Export Service.

-   **[Instance Data Replication](https://www.servicenow.com/docs/access?context=instance-data-replication&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Improve the performance and processing efficiency of Instance Data Replication by upgrading the replication sets that you created prior to the Washington DC release to use Hermes Messaging Service.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

