---
title: Hermes Messaging Service release notes
description: The ServiceNow Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow instance. Hermes Messaging Service was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Hermes Messaging Service release notes

The ServiceNow® Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow® instance. Hermes Messaging Service was enhanced and updated in the Australia release.

## Hermes Messaging Service highlights for the Australia release

-   Create more Hermes topics for specific events or integrations with an expanded topic limit.
-   View granular usage metrics in the Hermes Usage Dashboard.
-   Restrict access to the Hermes cluster based on the client IP address.

See Hermes Messaging Service for more information.

## New in the Australia release

-   **Expanded topic limits in Hermes**

    Create more topics in Hermes with an increased topic limit. The total number of partitions across all topics can't exceed 960.

-   **Hermes Usage Dashboard improvements**

    View Hermes data usage by source, including the total number of bytes received and bytes sent over time, in the Hermes Usage Dashboard.

-   **Access restrictions by IP address**

    Restrict access to Hermes by enabling IP address access control rules.

-   **View-only role**

    Enable administrators to view topics and namespaces in Hermes by granting the hermes\_viewer role instead of the full admin role.


## Activation information

Hermes Messaging Service is a ServiceNow AI Platform feature that is available with activation of the ServiceNow Stream Connect Installer \(com.glide.hub.stream\_connect.installer\) plugin or the installation of the Log Export Service application. For details, see Activating the Hermes Messaging Service.

## Related ServiceNow applications and features

-   **Using Stream Connect for Apache Kafka**

    Produce Apache Kafka messages from your ServiceNow instance using Workflow Studio and then consume the messages in an external application. You can also produce Apache Kafka messages from an external application and then consume the messages in your ServiceNow instance using a variety of consumers with Stream Connect.

-   **Exploring Log Export Service \(LES\)**

    Export log data securely to your external data lake for reporting, auditing, or regulatory purposes using Hermes Messaging Service with the Log Export Service.

-   **Instance Data Replication**

    Improve the performance and processing efficiency of Instance Data Replication by upgrading the replication sets that you created before the Washington DC release to use Hermes Messaging Service.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

