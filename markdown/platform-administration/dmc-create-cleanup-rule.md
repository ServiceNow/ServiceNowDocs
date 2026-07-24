---
title: Create a cleanup rule
description: Define a rule for deleting records from a primary table on a recurring basis.Define one or more conditions that identify the records to be deleted.Specify which associated records to delete when the cleanup rule runs.View a summary of your cleanup rule and decide whether to activate it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/dmc-create-cleanup-rule.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Deleting older or unwanted records in Data Management Console, Manage data growth in Data Management, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a cleanup rule

Define a rule for deleting records from a primary table on a recurring basis.

## Before you begin

Role required: admin

## About this task

Create a cleanup rule to delete records on a recurring basis. To delete records as a one-time operation, see [Create a one-time delete rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dmc-create-onetime-delete-rule.md).

## Procedure

1.  Access the create rule wizard in the Data Management Console in one of the following ways.

<table id="choicetable_snz_r2m_13c"><thead><tr><th align="left" id="d304140e72">

Option

</th><th align="left" id="d304140e75">

Steps

</th></tr></thead><tbody><tr><td id="d304140e81">

**Overview tab**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; ****.
2.  On the Overview tab, select the table with records that you want to clean up.
3.  Select **Create rule**.


</td></tr><tr><td id="d304140e119">

**Rules tab**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; ****.
2.  On the Tables tab, select the table with records that you want to clean up.
3.  On the table details page, select the Rules tab.
4.  Select **Create rule**.


</td></tr></tbody>
</table>2.  Define the cleanup rule.

    1.  On the Define your rule page, select **Cleanup** as the rule type.

    2.  Enter a name and description for the rule.

        The name is used as the [display value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DisplayValues.md) for references to this rule.

    3.  Select **Save and continue**.


## Define cleanup rule conditions

Define one or more conditions that identify the records to be deleted.

### Before you begin

Role required: admin

### About this task

Use the condition builder to specify filter conditions that define the records to be deleted. For example, you might specify that only records where 'active = false AND state =closed' are deleted.

### Procedure

1.  On the Define conditions page, select the Date/Time field that you want to use for monitoring duration in the **Date field**.

2.  Specify the amount of time that the system must wait before deleting records by entering a duration \(in years, days, and hours\).

3.  Limit the number of records by adding one or more conditions that records must meet.

    1.  Select a field, operator, and field value.

        For example, **\[Active\] \[is\] \[false\]**.

    2.  Use the OR and AND operators to add conditions.

    3.  Select **Add condition set Criteria** to add another set of conditions.

4.  Select **Save and continue**.


## Select associated records to delete

Specify which associated records to delete when the cleanup rule runs.

### Before you begin

Role required: admin

### Procedure

1.  On the Clean up associated records page, select which associated records to delete when the cleanup rule runs.

<table id="choicetable_vlk_yvs_13c"><thead><tr><th align="left" id="d304140e368">

Associated records

</th><th align="left" id="d304140e371">

Description

</th></tr></thead><tbody><tr><td id="d304140e377">

**Attachments**

</td><td>

Selected by default. Associated attachments are always deleted.

</td></tr><tr><td id="d304140e386">

**Journals**

</td><td>

If selected, related records in the Journal Entry \[sys\_journal\_field\] table are also deleted.If cleared, the system deletes records from the target table, but not any related journal records in this table.

</td></tr><tr><td id="d304140e397">

**Audits**

</td><td>

If selected, related records in the following audit tables are also deleted:-   Sys Audit \[sys\_audit\] table
-   Audit Relationship Change \[sys\_audit\_relation\] table
**Note:** Audit records that are created by table cleaner in the Audit Deleted Record \[sys\_audit\_delete\] table are preserved.

If cleared, the system deletes records from the target table, but not any related audit records in these tables.

</td></tr></tbody>
</table>2.  Delete all matching records plus any records referring to them by selecting **Cascade delete**.

    If this option is cleared, the system deletes matching records, but not records referring to them.

3.  Select **Save and continue**.


## View a summary of your cleanup rule and activate it

View a summary of your cleanup rule and decide whether to activate it.

### Before you begin

You must activate the cleanup rule and its corresponding data management policy for the cleanup rule to run.

Role required: admin

### Procedure

1.  On the Rule summary page, review the cleanup rule conditions and settings.

2.  Activate the rule by selecting **Activate the rule upon creation**.


### Result

The table cleanup rule runs automatically and deletes records when they meet the specified record age and any conditions that you set for them.

