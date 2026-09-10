---
title: Exploring Zero Copy Connector for ERP systems
description: Create an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to connect to an external ERP system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/exploring-erp-systems.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, system]
breadcrumb: [Exploring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP systems

Create an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to connect to an external ERP system.

In Zero Copy Connector for ERP, an ERP system is a configuration record that represents a connection to a specific section or domain of your external ERP system. The record contains information that tells the ServiceNow AI Platform where to connect and how to communicate with your ERP, using a connection and credential alias.

Zero Copy Connector for ERP supports the following ERP systems:

-   SAP ECC
-   SAP S/4HANA
-   SAP S/4HANA Cloud
-   SuccessFactors
-   Workday
-   Oracle E-Business Suite \(EBS\)

Each ERP system record organizes the connection to the ERP system and points to ERP data rather than copying it. Zero Copy Connector for ERP doesn't replicate data into the ServiceNow AI Platform; it mirrors data that lives in the ERP system, where it remains protected.

\[Omitted image "erp-canvas-explore-systems.png"\] Alt text: System recording showing information including system, connections, and ERP software.

You can have multiple ERP system records on one instance \(license-dependent\). After creation, Zero Copy Connector for ERP regularly pings each system to confirm that the connection is healthy.

For more information, see [Working with ERP systems in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.md).

