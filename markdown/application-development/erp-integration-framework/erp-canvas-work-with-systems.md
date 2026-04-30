---
title: Working with ERP systems in Zero Copy Connector for ERP
description: An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Zero Copy Connector for ERP, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Working with ERP systems in Zero Copy Connector for ERP

An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.

## ERP systems organize connections to the system of record

The system plays a crucial role in data synchronization, sharing, and collaboration, enabling seamless integration and operation between the ERP model and the connected ERP system.

Zero Copy Connector for ERP provides a standard set of ERP models, such as SAP Material Stock and SAP Purchase Document. You can also build new models. For a list of standard ERP models, which you must clone to modify, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../reference/erp-canvas-standard-extraction-tables.md).

## Configuring ERP systems and checking connections

ERP systems are configured by ServiceNow admins. The ERP system is set on the extraction table or remote table. Zero Copy Connector for ERP supports connecting to multiple systems.

Zero Copy Connector for ERP regularly scans all connected ERP systems for the latest heartbeat, which indicates whether a ping to the ERP system connection is currently successful.

-   **[Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md)**  
Configure an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to organize your connections to the system of record.
-   **[View a list of Zero Copy Connector for ERP systems](../task/view-and-monitor-erp-systems-health.md)**  
Check the ERP \(Enterprise Resource Planning\) systems list in Zero Copy Connector for ERP to view the heartbeats and retrieval status of your ERP systems.
-   **[View Zero Copy Connector for ERP system heartbeat information](../task/view-erp-system-heartbeat-information.md)**  
In Zero Copy Connector for ERP, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.
-   **[View Zero Copy Connector for ERP software information](../task/view-erp-system-information.md)**  
In Zero Copy Connector for ERP, view software information including machine type, node name, supported database, and more.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](erp-integration-configuration-overview.md)

