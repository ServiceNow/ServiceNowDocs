---
title: Working with ERP systems in ERP Canvas
description: An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erp-canvas-work-with-systems.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Canvas, ERP Canvas, Building low-code applications, Developing your application, Building applications]
---

# Working with ERP systems in ERP Canvas

An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.

## ERP systems organize connections to the system of record

The system plays a crucial role in data synchronization, sharing, and collaboration, enabling seamless integration and operation between the ERP model and the connected ERP system.

ERP Canvas provides a standard set of ERP models, such as SAP Material Stock and SAP Purchase Document. You can also build new models. For a list of standard ERP models, which you must clone to modify, see [Standard ERP models and extraction tables for ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-standard-extraction-tables.md).

## Configuring ERP systems and checking connections

ERP systems are configured by ServiceNow admins. The ERP system is set on the extraction table or remote table. ERP Canvas supports connecting to multiple systems.

ERP Canvas regularly scans all connected ERP systems for the latest heartbeat, which indicates whether a ping to the ERP system connection is currently successful.

-   **[Create an ERP system in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/create-an-erp-system.md)**  
Configure an ERP \(Enterprise Resource Planning\) system in ERP Canvas to organize your connections to the system of record.
-   **[View a list of ERP Canvas systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/view-and-monitor-erp-systems-health.md)**  
Check the ERP \(Enterprise Resource Planning\) systems list in ERP Canvas to view the heartbeats and retrieval status of your ERP systems.
-   **[View ERP Canvas system heartbeat information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/view-erp-system-heartbeat-information.md)**  
In ERP Canvas, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.
-   **[View ERP Canvas software information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/view-erp-system-information.md)**  
In ERP Canvas, view software information including machine type, node name, supported database, and more.

**Parent Topic:**[Configuring ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-integration-configuration-overview.md)

