---
title: Create a resource value record
description: Create a resource value record for each software model for which you want to calculate licensing requirements.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create a resource value record

Create a resource value record for each software model for which you want to calculate licensing requirements.

## Before you begin

Role required: sam\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Resource Value**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_uky_rp3_t1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the resource value.

</td></tr><tr><td>

Software model

</td><td>

Software model of the software product that the resource value is associated with.

</td></tr><tr><td>

Company

</td><td>

Company of the associated resource value record.

</td></tr><tr><td>

Location

</td><td>

Physical location of the associated resource value record.

</td></tr><tr><td>

Units consumed

</td><td>

Total number of resource value units of the associated software product that you’re currently consuming. For example, if you’re protecting 50 terabytes of data using a data protection software product, set the **Units consumed** field to `50`.For the Java SE software model with the Employee license metric, the **Units consumed** field must be set to the number of employees consuming the licenses.

</td></tr><tr><td>

Department

</td><td>

Department that the resource value record is assigned to.

</td></tr><tr><td>

Cost Center

</td><td>

Cost center that is financially responsible for the resource value.

</td></tr></tbody>
</table>4.  Select **Save**.

    **Note:** You can create multiple resource value records for the same software model and give them unique names. All the resource value records with the same software model are taken into consideration before reconciliation is run.


## Result

The resource value record that you created appears in the Resource Value list view.

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

