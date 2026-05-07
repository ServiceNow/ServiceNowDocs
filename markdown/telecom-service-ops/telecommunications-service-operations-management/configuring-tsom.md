---
title: Configuring Telecommunications Service Operations Management
description: Configure Telecommunications Service Operations Management \(TSOM\) to enable real-time event ingestion, correlation, and automated remediation by integrating with external network monitoring and discovery systems.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Telecommunications Service Operations Management]
---

# Configuring Telecommunications Service Operations Management

Configure Telecommunications Service Operations Management \(TSOM\) to enable real-time event ingestion, correlation, and automated remediation by integrating with external network monitoring and discovery systems.

Set up TSOM to enable end-to-end telecom service operations, including alarm ingestion, CMDB population, discrepancy detection, and service impact visibility. This configuration involves activating Telecommunications API notifications, setting up discovery and service graph connectors, enabling visibility, and configuring audit and reconciliation frameworks.

## Configuration overview

Telecommunications Service Operations Management \(TSOM\) requires configuring multiple components across alarm ingestion, discovery, data normalization, and reconciliation to support end-to-end telecom operations. The configuration flow typically includes the next plugins \(The plugin dependency will be automatically resolved during the installation\).

1.  Install the following plugins:

    |Name|ID|Product/Service|
    |----|---|---------------|
    |TSOM Event Management Connectors|sn\_tsom\_em\_connectors|Telecom Assurance|
    |Service Graph Connector for Fortinet|sn\_tsom\_fortinet\_connector|Telecom Visibility|
    |Service Graph Connector for Meraki|sn\_tsom\_meraki\_connector|Telecom Visibility|
    |Service Graph Connector for VeloCloud|sn\_tsom\_vcloud\_connector|Telecom Visibility|

2.  Enable alarm ingestion: Activate the Telecommunications API notifications and set up topic subscriptions to receive alarms from external systems. For more information, see [Configuring Telecommunications API notifications](configuring-telecommunications-api-notifications.md).
3.  Set up visibility or Event Management by following the appropriate setup wizards. See [Configure Telecom Visibility](../task/configuring-tsom-visibility.md) and [Fault Management: Events and alerts](fault-management-events-and-alerts.md).

Each step is modular and can be configured based on your environment and available integrations.

