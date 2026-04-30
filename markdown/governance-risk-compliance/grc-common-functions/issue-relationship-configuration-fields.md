---
title: Issue Relationship Configuration form
description: Use the Issue Relationship Configuration form in the GRC application to automatically link a destination record with an issue when it’s linked to the source record.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Steps to configure an issue relationship, Configure an issue relationship, Issues in the Workspace, Manage issues, Common GRC features, Governance, Risk, and Compliance]
---

# Issue Relationship Configuration form

Use the Issue Relationship Configuration form in the GRC application to automatically link a destination record with an issue when it’s linked to the source record.

<table id="table_zkd_fkf_rvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source table

</td><td>

Many to Many \(MtoM\) table in which the original record gets created when you link an issue to an object.

 For example, if you linked an issue to a control, the relationship record is created in this table.

</td></tr><tr><td>

Destination table

</td><td>

Target table where the record is created when the issue is linked to the destination object.

 For example, let's say that you selected the issue to link to a control in the **Source table** field. The issue is linked to the control's entity if you selected the issue to link to the entity MtoM in the **Destination table** field.

</td></tr><tr><td>

Source field

</td><td>

Source field that displays the relationship between the source object and the destination object.

</td></tr><tr><td>

Destination field

</td><td>

Destination field that contains the object that is linked to the issue in the **Destination table field.**

 For example, if you selected the issue to link to an entity relationship in the **Destination table** field, then the destination field value is entity.

**Note:** The object types that you select in the source field and destination field should be the same types.

</td></tr></tbody>
</table>**Note:**

-   **Source object**: It’s the original object that is linked to an issue manually.
-   **Destination object**: It’s the object that is automatically linked to the issue due to the issue relationship configuration.

**Parent Topic:**[Configure an issue relationship](../task/enable-or-disable-issue-relationship-configuration.md)

