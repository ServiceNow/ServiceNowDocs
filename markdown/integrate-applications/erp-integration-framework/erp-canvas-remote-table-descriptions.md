---
title: Zero Copy Connector for ERP remote table form field descriptions
description: The Remote table form in Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to create and edit remote tables in the ERP model.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, remote, table]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP remote table form field descriptions

The Remote table form in Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to create and edit remote tables in the ERP model.

For process details, see [View and edit ERP remote table details with Zero Copy Connector for ERP](../task/erpi-find-tables.md).

<table id="table_ep5_44s_wxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the remote table on the ServiceNow AI Platform.

</td></tr><tr><td>

Application

</td><td>

Application scope: global or per application.

</td></tr><tr><td>

ERP module

</td><td>

ERP module in the system of record, for example, sales orders or inventory. Select a module from the list. If the module you need isn't listed, contact [ServiceNow Technical Support](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547260).

 ERP modules represent a distinct set of features and functionalities tailored to address business processes or activities.

</td></tr><tr><td>

ERP model

</td><td>

ERP model connected to the remote table. The ERP model controls the available fields on the remote table.**Note:** Changing the ERP model removes any previously configured table fields that aren't available on the new model.

To change the model for an ERP remote table, you must select the **Unlock ERP model field** button and then select the **Unlock model change** button on the confirmation dialog.

</td></tr><tr><td>

Attachment setting

</td><td>

The remote table attachment is the cached response from the ERP system.

 If this field is set to **Use attachment**, Zero Copy Connector for ERP doesn't call the ERP system when someone fetches data from the remote table.

 If this field is set to **None**, Zero Copy Connector for ERP does call the ERP system.

</td></tr><tr><td>

ERP system

</td><td>

ERP system that the remote table is linked to. The connected system represents the ERP instance that is linked to the model, enabling data flow and interaction between the model and the connected ERP system. For more information, see [Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md).

</td></tr><tr><td>

Remote table link

</td><td>

Name of and link to the remote table on the ServiceNow AI Platform.Selecting the remote table link opens a new browser tab, where you can explore, query, and manage the remote table.

</td></tr><tr><td>

Page size

</td><td>

Amount of data to read from the ERP system at a time. The default is 1000. Increasing the size may impact MID Server memory space.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the remote table.

</td></tr><tr><td>

Long text

</td><td>

A longer description or information about the remote table.

</td></tr><tr><td>

Requires queryable field

</td><td>

Indicates whether you can retrieve data from the remote table without querying the source table.Smaller tables, such as a currency table, can have data stored locally and thus don't require a query to retrieve fields.

</td></tr><tr><td>

Enable schedule

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

