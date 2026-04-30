---
title: Zero Copy Connector for ERP ERP model table field descriptions
description: The Entity fields tab for an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP displays the table fields that are included in the ERP model.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, entity]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP ERP model table field descriptions

The **Entity fields** tab for an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP displays the table fields that are included in the ERP model.

For process details, see [Add an entity to a model](../concept/add-an-entity-to-model.md).

Zero Copy Connector for ERP automatically scans the linked ERP system to retrieve the latest entity data. However, you can select the refresh icon to update the data on demand.

<table id="table_m1n_l3v_2yb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Name of the field on the system of record.

</td></tr><tr><td>

Name

</td><td>

Name of the table on the system of record that contains the field.

</td></tr><tr><td>

Field label

</td><td>

Natural language field name for the automatically mapped field on the ServiceNow AI Platform.

</td></tr><tr><td>

Is custom

</td><td>

Option to indicate whether the field on the system of record is standard or customized.

</td></tr><tr><td>

ERP data type

</td><td>

Type of data the field contains. The options are:-   char \(character\)
-   date
-   decimal
-   numc \(number\)
-   time

</td></tr><tr><td>

Is queryable

</td><td>

Option to indicate whether you can retrieve data from the field without querying the source table.Smaller tables, such as a currency table, can have data stored locally and thus don't require a query to retrieve fields.

</td></tr><tr><td>

Updated

</td><td>

Date and time the field was most recently saved.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

