---
title: Archive related records in Core UI
description: Archive, clear, or delete related records from an archive rule.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Archiving records in Core UI, Manage data growth in Core UI, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Archive related records in Core UI

Archive, clear, or delete related records from an archive rule.

## Before you begin

Role required: admin.

## Procedure

1.  Access the archive rule that you want to configure in one of the following ways.

<table id="choicetable_cxh_nkk_1bc"><thead><tr><th align="left" id="d120397e59">

Option

</th><th align="left" id="d120397e62">

Steps

</th></tr></thead><tbody><tr><td id="d120397e68">

**Using a data management policy**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.
2.  Select the data management policy that contains the archive rule.
3.  In the Archive Rules related list, select the archive rule that you want to configure.
4.  In the **Archive Related Records** related list, select **New**.


</td></tr><tr><td id="d120397e110">

**Using the Archive Rules module**

</td><td>

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.
2.  Select the archive rule that you want to configure.
3.  In the **Archive Related Records** related list, select **New**.


</td></tr></tbody>
</table>2.  Select which action to take on related records in the **Action** field.

    |Action|Description|
    |------|-----------|
    |**Archive**|Archive records that reference the archived record.|
    |**Clear**|Remove the reference to the archived record. The record no longer references the archived record and doesn't appear as a related record in future archives.|
    |**Delete**|Delete records that reference the archived record.|

3.  Select the related records that you want to archive, clear, or delete by selecting a relationship in the **Reference** field.

    The **Reference** field lists all the relationships that exist to the archived table. There are two types of relationships in the list.

    -   **Reference fields**

        The list contains reference fields in other tables that refer to the archived table.

        For example, you create an archive rule on the Problem \[problem\] table. You can include related incident records by selecting the **Problem in Incident** field reference field on the Incident \[incident\] table.

        -   The **Archive** action archives any incident record that references an archived problem.
        -   The **Clear** action updates any incident record with a reference to the archived problem record by clearing the reference. If the reference is a [many-to-many relationship](../../task-table/concept/c_ManyToManyTaskRelations.md), the related record rule deletes the reference instead of clearing the reference.
        -   The **Delete** action deletes any incident record that references the archived problem record.
    -   **Document ID fields**

        The list contains document ID fields in other tables that point to the archived table. Document ID relationships display an asterisk \(\*\) character at the end of the selection name.

        For example, you create an archive rule on the Problem \[problem\] table. You can include related attachment records by selecting the **Table sys ID Attachment\(sys\_attachment\)\*** reference.

        -   The **Archive** action updates the attachment record to change the **Document ID** to refer to the archived table record.
        -   The **Clear** action removes the **Document ID** reference to the archived record. The record no longer references the archived record and doesn't appear as a related record in future archives.
        -   The **Delete** action deletes any attachment record that references the archived primary record.
    **Note:** You can't select references from some internal system tables or from peripheral tables. For example:

    -   Sys Audit \[sys\_audit\]
    -   Audit Deleted Record \[sys\_audit\_delete\]
    -   Audit Relationship Change \[sys\_audit\_relation\]
    -   Attachment \[sys\_attachment\]
    -   Journal Entry \[sys\_journal\_field\]
4.  Apply an archive rule to the related records that you're archiving by selecting a rule in the **Reference table rule** field.

    For example, if you already have an archive rule for the Incident \[incident\] table, select the existing incident archive rule when archiving records related to incidents records.

    **Note:** You control the cascade depth by specifying an archive rule in the **Reference table rule** field. Related records without a specified archive rule aren't cascaded.

    -   Prior to the Washington DC release, if an archive rule was defined in the system for a related record's table, the system would automatically cascade and process that archive rule and the related records associated with it.
    -   Beginning in the Washington DC release, even if an archive rule exists for a related record's table, you must declare that rule in the **Reference table rule** field to achieve that cascading behavior. If you have multiple related records on multiple tables, you can decide which of those records you want to include in the cascade by specifying the reference table rule.
5.  Select **Submit**.


**Parent Topic:**[Archiving records in Core UI](../../managing-data/concept/archiving-older-records.md)

