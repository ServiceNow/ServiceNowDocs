---
title: Zero Copy Connector for ERP system list field descriptions
description: The systems list in Zero Copy Connector for ERP \(Enterprise Resource Planning\) shows the connection and metadata retrieval status of each ERP system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-system-list-descriptions.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, create, new, system, connection]
breadcrumb: [Field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP system list field descriptions

The systems list in Zero Copy Connector for ERP \(Enterprise Resource Planning\) shows the connection and metadata retrieval status of each ERP system.

For process details, see [View a list of Zero Copy Connector for ERP systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/view-and-monitor-erp-systems-health.md).

<table id="table_xn1_4kd_5xb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP system

</td><td>

Name of the ERP system.

</td></tr><tr><td>

ERP heartbeat

</td><td>

Latest status of the SAP system connection, either **Success** or **Error**. The connection is checked every 5 minutes automatically.

</td></tr><tr><td>

Retrieval status

</td><td>

Status of the metadata retrieval that runs when the system first connects to the SAP system.-   BAPI/RFC: For BAPI, a list of the functions available to call on the system is collected. For RFC, the system checks which tables are available on the database.
-   Table: The tables from the database are retrieved.
-   OData: The models are retrieved.

</td></tr></tbody>
</table>