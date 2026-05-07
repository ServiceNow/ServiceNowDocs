---
title: Working with ERP systems in Zero Copy Connector for ERP
description: A Zero Copy Connector for ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, system, erp system]
breadcrumb: [Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Working with ERP systems in Zero Copy Connector for ERP

A Zero Copy Connector for ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.

## ERP systems organize connections to the system of record

The Zero Copy Connector for ERP system plays a crucial role in data synchronization, sharing, and collaboration, enabling seamless integration and operation between the model and the connected ERP system.

Zero Copy Connector for ERP provides a standard set of models, such as SAP Material Stock and SAP Purchase Document. For a list, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../reference/erp-canvas-standard-extraction-tables.md). For information about building new models, see [Create a model](../task/erpc-add-new-data-model.md). Use Zero Copy Connector for ERP data products, sets of predefined models and process extensions, as examples to help you implement and deploy applications with less manual work. For more information, see [Zero Copy Connector for ERP content packs](erp-canvas-content-packs.md).

## Configuring ERP systems and checking connections

Zero Copy Connector for ERP ERP systems are configured by ServiceNow admins. Zero Copy Connector for ERP supports connecting to multiple systems.

Zero Copy Connector for ERP regularly scans all connected ERP systems for the latest heartbeat, which indicates whether a ping to the ERP system connection is successful.

-   **[View a list of Zero Copy Connector for ERP systems](../task/view-and-monitor-erp-systems-health.md)**  
Check the ERP \(Enterprise Resource Planning\) systems list in Zero Copy Connector for ERP to view the heartbeats and retrieval status of your ERP systems.
-   **[Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md)**  
Configure an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to organize your connections to the system of record.
-   **[Edit and delete ERP systems](../task/edit-and-delete-erp-systems.md)**  
After creating an ERP \(Enterprise Resource Planning\) system, you can edit system details or delete the system at any time.
-   **[View Zero Copy Connector for ERP software information](../task/view-erp-system-information.md)**  
In Zero Copy Connector for ERP \(Enterprise Resource Planning\) , view software information including ERP family, database type, and more.
-   **[View Zero Copy Connector for ERP system heartbeat information](../task/view-erp-system-heartbeat-information.md)**  
In Zero Copy Connector for ERP \(Enterprise Resource Planning\), the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.
-   **[View Zero Copy Connector for ERP partner profile information](../task/view-erp-system-partner-profile-information.md)**  
In Zero Copy Connector for ERP \(Enterprise Resource Planning\), view partner profile information including number and type.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](erp-integration-configuration-overview.md)

