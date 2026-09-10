---
title: Hermes Messaging Service release notes
description: The ServiceNow Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow instance. Hermes Messaging Service was enhanced and updated in the Australia release.The ServiceNow Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow instance. Hermes Messaging Service was enhanced and updated in the Australia release.The ServiceNow Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow instance. Hermes Messaging Service was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Hermes Messaging Service release notes

The ServiceNow® Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow® instance. Hermes Messaging Service was enhanced and updated in the Australia release.

## About Hermes Messaging Service

-   Create more Hermes topics for specific events or integrations with an expanded topic limit.
-   View granular usage metrics in the Hermes Usage Dashboard.
-   Restrict access to the Hermes cluster based on the client IP address.
-   Manage Hermes configuration properties and background jobs from the Hermes Settings page.
-   Protect message data on broker disks with encryption at rest, with support for customer-supplied keys.

See [Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/hermes-messaging-service.md) for more information.

## Activation and other requirements

-   **Activation information**

    Hermes Messaging Service is a ServiceNow AI Platform feature that is available with activation of the ServiceNow Stream Connect Installer \(com.glide.hub.stream\_connect.installer\) plugin or the installation of the Log Export Service application. For details, see [Activating the Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/hermes-messaging-service-activation.md).


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-capabilities-rn-landing.md)

## July 2026

The ServiceNow® Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow® instance. Hermes Messaging Service was enhanced and updated in the Australia release.

### What's new

-   **[Hermes Settings page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c-hermes-settings.md)**

    Enable maintenance users and administrators to view and modify Hermes configuration properties and manage background jobs directly from the Hermes Settings page.

-   **[Encryption at rest for Hermes topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/encryption-at-rest.md)**

    Protect message data stored on broker disks by enabling encryption at rest on individual Hermes topics. Choose between ServiceNow-managed keys or customer-supplied keys using the Bring Your Own Key \(BYOK\) model.


## Australia

The ServiceNow® Hermes Messaging Service application enables you to integrate your Apache Kafka environment with your ServiceNow® instance. Hermes Messaging Service was enhanced and updated in the Australia release.

### What's new

-   **[Expanded topic limits in Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/exploring-hermes-messaging-service.md)**

    Create more topics in Hermes with an increased topic limit. The total number of partitions across all topics can't exceed 960.

-   **[Hermes Usage Dashboard improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/monitoring-data-usage-hermes.md)**

    View Hermes data usage by source, including the total number of bytes received and bytes sent over time, in the Hermes Usage Dashboard.

-   **[Access restrictions by IP address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/restricting-access-hermes-topics.md)**

    Restrict access to Hermes by enabling IP address access control rules.

-   **[View-only role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/hermes-messaging-service-roles.md)**

    Enable administrators to view topics and namespaces in Hermes by granting the hermes\_viewer role instead of the full admin role.


