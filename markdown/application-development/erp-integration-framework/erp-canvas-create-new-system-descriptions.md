---
title: Zero Copy Connector for ERP new system field descriptions
description: The new system form in Zero Copy Connector for ERP contains information on connection details for the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Zero Copy Connector for ERP field descriptions, Zero Copy Connector for ERP reference, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Zero Copy Connector for ERP new system field descriptions

The new system form in Zero Copy Connector for ERP contains information on connection details for the ERP \(Enterprise Resource Planning\) system.

For process details, see [Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md).

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

Connection

</td><td>

Alias of the connection credential that you configured to connect to the system of record. You can select only from connections in the Zero Copy Connector for ERP scope.For more information, see [Configure the Zero Copy Connector for ERP credentials and connection](../task/set-up-erp-integration-connection.md).

</td></tr><tr><td>

ERP software

</td><td>

The supported ERP software on the system. Select one or more options from the list, for example, ECC 7.5 and SAP S/4HANA 2021. The list contains SAP major versions and does not include patch versions.

</td></tr><tr><td>

Latest alive heartbeat

</td><td>

Date and time that the ServiceNow AI Platform most recently connected to the ERP system.This field isn't editable and has a value only if the ERP system has been successfully saved and contacted.

</td></tr><tr><td>

Extraction tables

</td><td>

Number of ERP extraction tables in the ERP system. This field isn't editable.Link a system to an extraction table by adding the system to the ERP extraction table record in Zero Copy Connector for ERP. For more information, see [Add a new ERP extraction table in Zero Copy Connector for ERP](../task/erp-canvas-add-new-extraction-table.md).

</td></tr><tr><td>

Remote tables

</td><td>

Number of remote tables in the ERP system. This field isn't editable.Link a system to a remote table by adding the system to the ERP remote table record in Zero Copy Connector for ERP. For more information, see [View and edit ERP remote table details with Zero Copy Connector for ERP](../task/erpi-find-tables.md).

</td></tr><tr><td>

Updated

</td><td>

Date and time the ERP system record was most recently saved. This field isn't editable.

</td></tr><tr><td>

KB link \(on heartbeat tabs after system record is first saved\)

</td><td>

If there's an error and a relevant knowledge base article is available, a link to the article is provided.

</td></tr><tr><td>

Status \(on heartbeat tabs after system record is first saved\)

</td><td>

State of the heartbeat: **Started**, **Success**, or **Error**.

</td></tr><tr><td>

Error text \(on heartbeat tabs after system record is first saved\)

</td><td>

Details about any errors that have occurred.

</td></tr><tr><td>

Updated \(on heartbeat tabs after system record is first saved\)

</td><td>

Date and time when the heartbeat was last changed.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

