---
title: Zero Copy Connector for ERP system list field descriptions
description: The Create new system form in Zero Copy Connector for ERP contains information on connection details for the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, create, new, system, connection]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP system list field descriptions

The Create new system form in Zero Copy Connector for ERP contains information on connection details for the ERP \(Enterprise Resource Planning\) system.

For process details, see [View a list of Zero Copy Connector for ERP systems](../task/view-and-monitor-erp-systems-health.md).

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

When the system is first set up and connects to the SAP system, metadata is retrieved.-   BAPI/RFC: For BAPI, a list of functions available to call on the system are collected. For RFC, a check is done to determine the tables available on the database.
-   Table: The tables from the database are retrieved.
-   Odata: The models available on the HTTP protocol are retrieved.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

