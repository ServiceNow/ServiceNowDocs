---
title: Create an archive rule
description: Define the criteria for archiving records by creating an archive rule.Preview the records that you want to archive, and then activate an archive rule.Delete archived records and related records after a specified amount of time.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Archiving records, Manage data growth, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an archive rule

Define the criteria for archiving records by creating an archive rule.

## Before you begin

Because you can define multiple archive rules for a table, verify any existing archive rules to avoid potential conflicts. For example, if there's a rule for archiving records older than six months, creating another rule to archive records older than three months could cause a conflict. In such cases, either rule could potentially run, each archiving records under different conditions.

Role required: admin

## Procedure

1.  Access the archive rule form in one of the following ways.

<table id="choicetable_bxv_hjk_1bc"><thead><tr><th align="left" id="d152225e64">

Option

</th><th align="left" id="d152225e67">

Steps

</th></tr></thead><tbody><tr><td id="d152225e73">

**Using a data management policy**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.
2.  Select the data management policy for the table with records that you want to archive.
3.  In the Archive Rules related list, select **New**.


</td></tr><tr><td id="d152225e109">

**Using the Archive Rules module**

</td><td>

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.
2.  Select **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_ub4_f4s_x4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that identifies the rule. Used as the [display value](../../field-administration/concept/c_DisplayValues.md) for references to this archive rule.

</td></tr><tr><td>

Table

</td><td>

The table with records that you want to archive. -   You can't change the table in an existing archive rule. To archive records in a different table, create a new archive rule.
-   You can't select a table in a different application scope.
-   You can't create an archive rule for a table where **update\_synch** is set to true in the dictionary entry for the table.
-   You can't create archive rules for some internal system tables or peripheral tables. For example:
    -   Sys Audit \[sys\_audit\]
    -   Audit Deleted Record \[sys\_audit\_delete\]
    -   Audit Relationship Change \[sys\_audit\_relation\]
    -   Attachment \[sys\_attachment\]
    -   Journal Entry \[sys\_journal\_field\]


</td></tr><tr><td>

Retain references

</td><td>

Option to keep the sys\_id for a reference field instead of storing the display name as a string in the archive table. **Important:** The **Retain references** check box becomes read only after you select it and save the archive rule.

When you enable this option on a table with archived records, the system automatically reprocesses all existing archive records and enables references. This process can take time to complete for larger archive tables. You can track the status by viewing the Archive Rule Reference Migrations \[sys\_archive\_ref\_migration\] table.

For details on manually retaining references, see [Migrating non-reference fields to reference fields](../reference/archive-reference-migration.md).

</td></tr><tr><td>

Description

</td><td>

Description of the archive rule.

</td></tr><tr><td>

Conditions

</td><td>

Condition builder for specifying filter conditions that define the records to be archived. For example, you might archive inactive records older than a certain date.

 Make sure that the correct records are selected by testing the conditions in a list view before you activate the archive rule. For example,

-   To archive records closed more than two years ago from today, use the relative operator in a condition like **\[Closed\] \[relative\] \[before\] \[2\] \[Years\] \[ago\]**.
-   To archive records for the current year and the prior year, and not two years ago from today's date, use a condition like **\[Closed\] \[before\] \[Last 2 years\]**.


</td></tr><tr><td>

Auto Rearchive

</td><td>

Option that enables a restored record to be automatically rearchived after a set time period.

</td></tr><tr><td>

Auto Rearchive Duration

</td><td>

The time interval before the restored record is automatically archived.

</td></tr></tbody>
</table>3.  Estimate the number of records to archive by selecting the **Recalculate Archive Estimate** related link.

    The estimate only includes primary records and excludes any related records added to the archive rule. The estimate helps you determine if the archive rule affects the number of records you expect it to. If the estimate is too high or low, change the archive rule conditions accordingly.

    The updated count appears in the **Record estimate** field.

4.  Select **Submit**.


**Parent Topic:**[Archiving records](../../managing-data/concept/archiving-older-records.md)

## Activate an archive rule

Preview the records that you want to archive, and then activate an archive rule.

### Before you begin

Role required: admin

### About this task

You must activate the archive rule and its corresponding data management policy for the archive rule to run.

The sample archive rules are inactive by default.

### Procedure

1.  Access the archive rule that you want to activate in one of the following ways.

<table id="choicetable_cxh_nkk_1bc"><thead><tr><th align="left" id="d152225e421">

Option

</th><th align="left" id="d152225e424">

Steps

</th></tr></thead><tbody><tr><td id="d152225e430">

**Using a data management policy**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.
2.  Select the data management policy for the table with records that you want to archive.
3.  In the Archive Rules related list, select the archive rule that you want to activate.


</td></tr><tr><td id="d152225e463">

**Using the Archive Rules module**

</td><td>

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.
2.  Select the archive rule that you want to activate.


</td></tr></tbody>
</table>2.  Estimate the number of archive records by selecting the **Recalculate Archive Estimate** related link.

    The estimate only includes primary records and excludes any related records added to the archive rule. The estimate helps you determine if the archive rule affects the number of records that you expect. If the estimate is too high or low, change the archive rule conditions accordingly.

    The updated count appears in the **Record estimate** field.

3.  Activate the archive rule by selecting the **Active** check box.

4.  Archive records immediately by selecting the **Run Archive Now** related link.

    The **Run Archive Now** related link is only available if the corresponding data management policy is activated.


### Result

Records that meet the archive rule criteria are archived during the next archive run.

### What to do next

View the archived records by navigating to **All** &gt; **System Archiving** &gt; **Archive Tables** and selecting the module for the archived table, for example, **Archive Incidents**.

## Create a destroy rule

Delete archived records and related records after a specified amount of time.

### Before you begin

Role required: admin

### About this task

You can associate a destroy rule with any archive rule in a data management policy.

If you need to amend the destroy rule properties running against your archived data, see [System properties](../reference/r_SetArchiveRuleProcessingBehavior.md).

### Procedure

1.  On the archive rule form, select **Create Destroy Rule**.

2.  In the Destroy Rule tab, fill out the fields.

<table id="table_ugn_bg5_cv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to activate the destroy rule.

</td></tr><tr><td>

Destroy Related Records

</td><td>

Option to automatically destroy related records associated with the archived records.**Note:** Peripheral records, which include records in the Journal Entry \[sys\_journal\_field\], Attachment \[sys\_attachment\], and Sys Audit \[sys\_audit\] tables are deleted automatically, even if you decide to preserve related records.

</td></tr><tr><td>

Archive Duration

</td><td>

Specify the amount of time that records stay in the archive table before the system deletes them.

</td></tr></tbody>
</table>3.  Estimate the number of archived records marked for deletion by selecting the **Recalculate Destroy Estimate** related link.

4.  Select **Submit**.


### Result

Records that have been archived longer than the archive duration value are destroyed when the scheduled job runs. You can verify the progress by checking the archive destroy log.

