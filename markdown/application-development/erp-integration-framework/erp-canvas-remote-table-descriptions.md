---
title: Zero Copy Connector for ERP remote table form field descriptions
description: The Remote table form in Zero Copy Connector for ERP enables you to create and edit remote tables in the ERP \(Enterprise Resource Planning\) model.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Zero Copy Connector for ERP field descriptions, Zero Copy Connector for ERP reference, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Zero Copy Connector for ERP remote table form field descriptions

The Remote table form in Zero Copy Connector for ERP enables you to create and edit remote tables in the ERP \(Enterprise Resource Planning\) model.

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

Remote table link

</td><td>

Name of and link to the remote table on the ServiceNow AI Platform.Selecting the remote table link opens a new browser tab, where you can explore, query, and manage the remote table.

</td></tr><tr><td>

ERP model

</td><td>

ERP model connected to the remote table. The ERP model controls the available fields on the remote table.**Note:** Changing the ERP model removes any previously configured table fields that aren't available on the new model.

To change the model for an ERP remote table, you must select the **Unlock ERP model field** button and then select the **Unlock model change** button on the confirmation dialog.

</td></tr><tr><td>

ERP system

</td><td>

ERP system that the remote table is linked to. The connected system represents the ERP instance that is linked to the model, enabling data flow and interaction between the model and the connected ERP system. For more information, see [Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md).

</td></tr><tr><td>

Requires queryable field

</td><td>

Indicates whether you can retrieve data from the remote table without querying the source table.Smaller tables, such as a currency table, can have data stored locally and thus don't require a query to retrieve fields.

</td></tr><tr><td>

Updated

</td><td>

Date and time the remote table record was last saved.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

