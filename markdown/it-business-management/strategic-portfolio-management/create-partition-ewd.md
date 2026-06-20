---
title: Create and configure a partition
description: Create a partition to control record visibility for users within a specific function, such as a department or business unit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-portfolio-management/create-partition-ewd.html
release: zurich
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: task
last_updated: "2026-06-20"
reading_time_minutes: 3
breadcrumb: [Configure, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Create and configure a partition

Create a partition to control record visibility for users within a specific function, such as a department or business unit.

## Before you begin

-   Identify the reference field, such as Department or Business Unit, to use as the partition criteria for each supported table. The reference field can be different for each table within the same partition.
-   Create a dedicated role for this partition to control record visibility for its users. For details, see .

Role required: sn\_spm\_ewd.ewd\_admin

## About this task

Partitions are created per function — such as a department, business unit, or investment type — based on your organization's needs. Each partition requires a unique label and a dedicated role. After a partition is created, the partition criteria field selected for a partitioned table is set to read-only and can't be changed. Plan your partition structure before creating partitions. Changing the partition criteria field to a different function type — for example, from department to business unit — after data has been populated requires deleting and recreating the affected partitions.

## Procedure

1.  Navigate to **All** &gt; **Enterprise-Wide Deployment** &gt; **Partitions**.

    A list of partitions appears.

2.  Select **New**.

3.  Fill in the fields on the partition form.

    |Field|Description|
    |-----|-----------|
    |Label|Display name of the partition. For example, enter `IT Ops` for the IT Operations department partition.|
    |Name|Name of the partition stored in the system. This field is automatically set to the label value, with underscores replacing spaces.|
    |Partition role|Role assigned to this partition. Determines which users can access records associated with this partition.|

4.  From the Additional actions \(\[Omitted image "context-menu-icon.png"\] Alt text: Additional actions icon.\), select **Save**.

    Partitioned table records for Project \[pm\_project\], Demand \[dmn\_demand\], Program \[pm\_program\], and Portfolio \[pm\_portfolio\] are automatically generated without partition criteria.

5.  Configure partition criteria for the required tables.

    1.  From the Partitioned tables list, select a table.

        For example, select Program \[pm\_program\]. The partitioned table record opens.

    2.  Fill in the fields on the partitioned table form.

<table id="table_gr3_xd3_fjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Partition

</td><td>

Name of the partition associated with this partitioned table.

</td></tr><tr><td>

Active

</td><td>

When selected, the partitioned table is active on this partition.

</td></tr><tr><td>

Table

</td><td>

Name of the table associated with this partitioned table record.

</td></tr><tr><td>

Partition criteria

</td><td>

Condition that determines which records belong to this partition. Use the **Field**, **Operator**, and **Value** fields to build the condition. Select a reference field such as **Department**, **Portfolio**, or **Investment Type** as the field, then select a partition value. The following example shows the Field set to Department and the Value set to IT Ops. All programs with the Department field set to IT Ops belong to this partition. \[Omitted image "partition-criteria-condition.png"\] Alt text: Partition criteria condition builder showing Field set to Department and Value set to IT Ops.

 **Note:** After you save the partition criteria record for a table, the criteria field is locked for that table. All subsequent partitions on the same table must use the same criteria field. This maintains consistency across all partitions for the same table.

</td></tr></tbody>
</table>    3.  Select **Update**.

    4.  Repeat steps a through c for Demand \[dmn\_demand\], Project \[pm\_project\], and Portfolio \[pm\_portfolio\] as needed.

    Partition criteria is configured for each supported table for this partition.


## What to do next

Assign the partition role to the relevant users or groups so they can access records within this partition. For details, see [Assign partition role for access to the partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/assign-partition-role-ewd.md).

**Note:** If your instance has existing records to associate with the new partition, run the partition backfill job. For details, see [Update partition details for existing records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/update-partition-details-for-existing-records.md).

