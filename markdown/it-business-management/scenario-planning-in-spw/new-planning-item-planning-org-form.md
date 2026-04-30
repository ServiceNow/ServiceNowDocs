---
title: Planning item type form
description: Learn about the fields of the new table form that are required to add a new planning item type in Strategic Planning.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Form field information for Strategic Planning, Reference, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Planning item type form

Learn about the fields of the new table form that are required to add a new planning item type in Strategic Planning.

<table id="table_bnt_zb3_gqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label for the table.

</td></tr><tr><td>

Name

</td><td>

This field is auto generated from your input in the **Label field**.

</td></tr><tr><td>

Application

</td><td>

This field is automatically set to **Portfolio Planning** based on your scope.

 If this field shows a different value, then ensure that your ServiceNow instance is in **Portfolio Planning** scope.

</td></tr><tr><td>

Extends table

</td><td>

If this new table is a type of planning item, select **Planning Item**.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|User role|Set this field to **sn\_align\_core.apw\_user** so that you grant access to the Strategic Planning user to this table.|

|Application Access|
|------------------|
|Enable the **Can read**, **Can create**, **Can update**, and **Can delete** fields.|

**Parent Topic:**[Form field information for Strategic Planning](form-field-information-for-strategic-planning.md)

**Related topics**  


[Define a new planning item type in Strategic Planning](../task/create-planning-organization-and-planning-item-type.md)

