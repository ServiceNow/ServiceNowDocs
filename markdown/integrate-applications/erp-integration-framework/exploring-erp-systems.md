---
title: Exploring Zero Copy Connector for ERP systems
description: Create an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to connect to an external ERP system.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, erp, system]
breadcrumb: [Explore, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP systems

Create an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to connect to an external ERP system.

In Zero Copy Connector for ERP, an ERP system is a configuration record that represents a connection to a specific section or domain of your external ERP system of record, for example, SAP ECC. The record contains information that tells the ServiceNow AI Platform where to connect and how to communicate with your ERP, using a connection and credential alias.

Each ERP system record organizes the connection to the system of record and points to ERP data rather than copying it. Zero Copy Connector for ERP doesn't replicate data into the ServiceNow AI Platform; it mirrors data that lives in the ERP system of record, where it remains protected.

You can have multiple ERP system records on one instance \(license-dependent\). Once created, each system is regularly pinged to confirm that the connection is healthy.

![Infographic showing steps for configuring connection, creating ERP system, and verifying heartbeat.](../image/erp-explore-systems-infographic.png)

For more information, see [Working with ERP systems in Zero Copy Connector for ERP](erp-canvas-work-with-systems.md).

**Parent Topic:**[Exploring Zero Copy Connector for ERP](exploring-erp-integration.md)

