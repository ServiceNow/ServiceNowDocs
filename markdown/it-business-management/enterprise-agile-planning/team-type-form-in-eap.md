---
title: Team type form
description: Learn about the fields of the new table form that are required to add a new team type in Enterprise Agile Planning.
locale: en-US
release: yokohama
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Team type form

Learn about the fields of the new table form that are required to add a new team type in Enterprise Agile Planning.

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

This field is auto-generated from your input in the **Label field**.

</td></tr><tr><td>

Application

</td><td>

This field is automatically set to **Portfolio Planning Core** based on your scope.

 If this field shows a different value, then set the scope of your ServiceNow instance to **Portfolio Planning Core**.

</td></tr><tr><td>

Extends table

</td><td>

Select **Enterprise agile team**.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|User role|Set this field to **sn\_apw\_advanced.eap\_user** so that you grant access to the EAP user to this table.|

|Application Access|
|------------------|
|Enable the **Can read**, **Can create**, **Can update**, and **Can delete** fields.|

**Parent Topic:**[Enterprise Agile Planning reference](eap-reference.md)

**Related topics**  


[Create a custom team type in EAP](../task/create-custom-team-type-in-eap.md)

