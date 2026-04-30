---
title: Working with ERP systems in ERP Data Hub
description: An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Data Hub, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Working with ERP systems in ERP Data Hub

An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.

## ERP systems organize connections to the system of record

The system plays a crucial role in data synchronization, sharing, and collaboration, enabling seamless integration and operation between the ERP model and the connected ERP system.

ERP Data Hub provides a standard set of ERP models, such as SAP Material Stock and SAP Purchase Document. You can also build new models. For a list of standard ERP models, which you must clone to modify, see [Standard ERP models and extraction tables for ERP Data Hub](../reference/erp-canvas-standard-extraction-tables.md).

## Configuring ERP systems and checking connections

ERP systems are configured by ServiceNow admins. The ERP system is set on the extraction table or remote table. ERP Data Hub supports connecting to multiple systems.

ERP Data Hub regularly scans all connected ERP systems for the latest heartbeat, which indicates whether a ping to the ERP system connection is currently successful.

-   **[Create an ERP system in ERP Data Hub](../task/create-an-erp-system.md)**  
Configure an ERP \(Enterprise Resource Planning\) system in ERP Data Hub to organize your connections to the system of record.
-   **[View a list of ERP Data Hub systems](../task/view-and-monitor-erp-systems-health.md)**  
Check the ERP \(Enterprise Resource Planning\) systems list in ERP Data Hub to view the heartbeats and retrieval status of your ERP systems.
-   **[View ERP Data Hub system heartbeat information](../task/view-erp-system-heartbeat-information.md)**  
In ERP Data Hub, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.

**Parent Topic:**[Configuring ERP Data Hub](erp-integration-configuration-overview.md)

