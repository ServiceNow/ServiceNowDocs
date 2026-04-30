---
title: Configuring Telecommunications Service Operations Management
description: Configure Telecommunications Service Operations Management \(TSOM\) to enable real-time event ingestion, correlation, and automated remediation by integrating with external network monitoring and discovery systems.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Telecommunications Service Operations Management]
---

# Configuring Telecommunications Service Operations Management

Configure Telecommunications Service Operations Management \(TSOM\) to enable real-time event ingestion, correlation, and automated remediation by integrating with external network monitoring and discovery systems.

Set up TSOM to enable end-to-end telecom service operations, including alarm ingestion, CMDB population, discrepancy detection, and service impact visibility. This configuration involves activating Telecommunications API notifications, setting up discovery and service graph connectors, enabling visibility, and configuring audit and reconciliation frameworks.

## Configuration overview

Telecommunications Service Operations Management \(TSOM\) requires configuring multiple components across alarm ingestion, discovery, data normalization, and reconciliation to support end-to-end telecom operations. The configuration flow typically includes:

1.  Activate the following plugins to have TSOM Core in your system
    -   Pattern Designer \(com.snc.pattern.designer\)
    -   ServiceNow IntegrationHub Started Pack Installer \(com.glide.hub.integrations\)
    -   Discovery \(com.snc.discovery\)
    -   CMDB CI Class Models \(sn\_cmdb\_ci\_class\) 1.69.0
    -   Visibility Content \(sn\_pattern\_design\) 6.23.0
    -   Integration Commons for CMDB \(sn\_cmdb\_int\_util\) 2.19.0
2.  Enable alarm ingestion: Activate the Telecommunications API notifications and set up topic subscriptions to receive alarms from external systems. For more information, see [Configuring Telecommunications API notifications](configuring-telecommunications-api-notifications.md).
3.  Set up visibility: Configure Telecom Visibility to view service-to-infrastructure mappings and monitor network health. For more information, see [Set up Telecom Visibility](../task/configuring-tsom-visibility.md)
    1.  Populate the telecom-aware CMDB:
        -   Install and configure Horizontal Discovery. For more information, see [Install Horizontal Discovery and set up Discovery Patterns](../task/install-horizontal-telecommunication-discoverypatterns.md).
        -   Set up Telecom Discovery Builder \(TDB\) ETL flows in connectors. For more information, see [Configuring the Telecom Discovery Builder framework ETL in a connector](configuring-the-telco-generic-schema-etl.md).
        -   Use service graph connectors \(e.g., Nokia Altiplano\) to import topology and configuration data. For more information, see [Configure Nokia Altiplano service graph connector](configuring-service-graph-connector-nokia-altiplano.md).
    2.  Enable discrepancy detection:
        -   Activate Telecom Discrepancy Identification and Reconciliation. For more information, see [Activate Telecom Discrepancy Identification and Reconciliation](../task/configure-telecom-reconciliation.md).
        -   Define filters for telecom audits and configure attribute value discrepancy checks in CMDB 360.

Each step is modular and can be configured based on your environment and available integrations.

