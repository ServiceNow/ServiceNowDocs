---
title: ERP Data Hub ERP model table field descriptions
description: The Entity fields tab for an ERP \(Enterprise Resource Planning\) model in ERP Data Hub displays the table fields that are included in the ERP model.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ERP Data Hub field descriptions, ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub ERP model table field descriptions

The **Entity fields** tab for an ERP \(Enterprise Resource Planning\) model in ERP Data Hub displays the table fields that are included in the ERP model.

ERP Data Hub automatically scans the linked ERP system to retrieve the latest entity data. However, you can select the refresh icon to update the data on demand.

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

Mapped field name

</td><td>

Name of the mapped field.The ServiceNow AI Platform automatically creates this mapped field name in the ERP model after scanning the linked tables on the system of record.

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

</td></tr></tbody>
</table>**Parent Topic:**[ERP Data Hub field descriptions](erp-canvas-field-descriptions.md)

