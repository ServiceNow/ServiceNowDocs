---
title: ERP Data Hub new system field descriptions
description: The Create new system form in ERP Data Hub contains information on connection details for the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ERP Data Hub field descriptions, ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub new system field descriptions

The Create new system form in ERP Data Hub contains information on connection details for the ERP \(Enterprise Resource Planning\) system.

<table id="table_obh_qgd_5xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP system

</td><td>

Name of the ERP system to help identify the business area.

</td></tr><tr><td>

Short description

</td><td>

Brief description of what the ERP system is for, such as sales orders.

</td></tr><tr><td>

Connection \(HTTP connection available starting in Xanadu Store Release 2\)

</td><td>

Alias of the connection credential that you configured to connect to the system of record. You can select only from connections in the ERP Data Hub scope.For more information, see [Configure the ERP Data Hub credentials and connection](../task/set-up-erp-integration-connection.md).

</td></tr><tr><td>

Latest alive heartbeat \(HTTP heartbeat available starting in Xanadu Store Release 2\)

</td><td>

Date and time that the ServiceNow AI Platform most recently connected to the ERP system.This field isn't editable and has a value only if the ERP system has been successfully saved and contacted.

</td></tr><tr><td>

ETL data sources/Extraction tables

</td><td>

Number of ERP extraction tables in the ERP system.Link a system to an extraction table by adding the system to the ERP extraction table record in ERP Data Hub. For more information, see [Add a new ERP extraction table in ERP Data Hub](../task/erp-canvas-add-new-extraction-table.md).

</td></tr><tr><td>

Remote tables

</td><td>

Number of remote tables in the ERP system.Link a system to a remote table by adding the system to the ERP remote table record in ERP Data Hub. For more information, see [View and edit ERP remote table details with ERP Data Hub](../task/erpi-find-tables.md).

</td></tr><tr><td>

Updated

</td><td>

Date and time the ERP system record was most recently saved.

</td></tr><tr><td>

KB link \(on heartbeat tabs\)

</td><td>

If there's an error and a relevant knowledge base article is available, a link to the article is provided.

</td></tr><tr><td>

Status \(on heartbeat tabs\)

</td><td>

State of the heartbeat: **Started**, **Success**, or **Error**.

</td></tr><tr><td>

Error text \(on heartbeat tabs\)

</td><td>

Details about the error.

</td></tr><tr><td>

Updated \(on heartbeat tabs\)

</td><td>

Date and time when the heartbeat was last changed.

</td></tr></tbody>
</table>**Parent Topic:**[ERP Data Hub field descriptions](erp-canvas-field-descriptions.md)

