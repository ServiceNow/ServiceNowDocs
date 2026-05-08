---
title: Telecom Discovery via Cisco Meraki SD-WAN
description: The Service Graph Connector \(SGC\) for Cisco Meraki provides a cloud-based management platform that provides a visual representation of network traffic flow between services and applications, enabling centralized configuration, monitoring, and management. Network administrators can easily discover and map services, enforce security policies, and troubleshoot issues in real time.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Indirect Discovery with SGCs, Telecom Discovery, Explore, Telecommunications Service Operations Management]
---

# Telecom Discovery via Cisco Meraki SD-WAN

The Service Graph Connector \(SGC\) for Cisco Meraki provides a cloud-based management platform that provides a visual representation of network traffic flow between services and applications, enabling centralized configuration, monitoring, and management. Network administrators can easily discover and map services, enforce security policies, and troubleshoot issues in real time.

The Cisco Meraki SGC provides visibility, control, and synchronization of physical and logical network infrastructure for service providers and telecom enterprises. It leverages REST APIs and a MID Server to deliver a unified, telecom-model-aligned view.

## Key benefits

-   Automated Device Discovery: Periodically, as determined by import schedules, scans the Cisco Meraki dashboard to import all Configuration Item \(CI\) data.
-   Real-time synchronization: Ensures the Configuration Management Database \(CMDB\) is up to date with the latest CI information.
-   Visualization: Provides a graphical representation of Cisco Meraki networks, device relationships, and dependencies through the Integration Hub ETL.

**Note:** For a general overview of Service Graph Connector technology, see Getting started with Service Graph Connectors.

## Cisco Meraki SGC Architecture

The Cisco Meraki architecture consists of the following key components:

-   Setup: A guided multi-step process that establishes connection alliances, configures credentials, and sets up REST API endpoints to integrate with the Meraki dashboard.
-   Data sources: Scripts that fetch information related to various components such as organizations, networks, devices, and uplinks from Meraki APIs.
-   Import schedules: Determines when data sources are executed to facilitate the discovery and updating of CIs.
-   Connection and credential aliases: Details of the protocols used for API requests to extract data.
-   Connections: Contains the necessary connection details for accessing the Meraki environment during the discovery process.
-   Credentials: Provides the necessary authorization information to obtain data from the Meraki environment.
-   Properties: System properties that contribute to configuring Cisco Meraki SGC and can be referenced within data sources.

## CMDB Integrations Dashboard

The Integration Commons for CMDB application provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors. The dashboard displays metrics for all integration runs. You can filter the view to a specific integration, time duration, or integration run. For more details about monitoring integrations in the CMDB Integrations Dashboard, see Integration Commons for CMDB.

**Related topics**  


[Configure Cisco Meraki Service Graph Connector](configuring-cisco-meraki-service-graph-connector.md)

[Run and verify an import schedule for Cisco Meraki SGC](../task/run-and-verify-import-for-cisco-meraki-sd-wan-service-graph-connector.md)

