---
title: ERP Data Hub system list field descriptions
description: The Create new system form in ERP Data Hub contains information on connection details for the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ERP Data Hub field descriptions, ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub system list field descriptions

The Create new system form in ERP Data Hub contains information on connection details for the ERP \(Enterprise Resource Planning\) system.

<table id="table_xn1_4kd_5xb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP system

</td><td>

Name of the ERP system.

</td></tr><tr><td>

ERP heartbeat \(HTTP connection available starting in Xanadu Store Release 2\)

</td><td>

Latest status of the SAP system connection, either **Success** or **Error**. The connection is checked every 5 minutes automatically.

</td></tr><tr><td>

Retrieval status \(OData available starting in Xanadu Store Release 2\)

</td><td>

When the system is first set up and connects to the SAP system, metadata is retrieved.-   BAPI/RFC: For BAPI, a list of functions available to call on the system are collected. For RFC, a check is done to determine the tables available on the database.
-   Table: The tables from the database are retrieved.
-   Odata: The models available on the HTTP protocol are retrieved.

</td></tr></tbody>
</table>**Parent Topic:**[ERP Data Hub field descriptions](erp-canvas-field-descriptions.md)

