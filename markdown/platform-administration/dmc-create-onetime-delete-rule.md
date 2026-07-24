---
title: Create a one-time delete rule
description: Define a rule for deleting records now or at a later date.Define one or more conditions that identify the records to be deleted.Specify which associated records to delete when the one-time delete rule runs.Schedule a date and time to execute a one-time delete rule or execute it after you finish creating it.View a summary of your one-time delete rule and acknowledge the deletion.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/dmc-create-onetime-delete-rule.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Previewing and deleting records in Data Management Console, Manage data growth in Data Management, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a one-time delete rule

Define a rule for deleting records now or at a later date.

## Before you begin

Role required: admin

## About this task

Create a one-time delete rule to delete records once. To delete records on a recurring basis, see [Create a cleanup rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dmc-create-cleanup-rule.md).

## Procedure

1.  Access the create rule wizard in the Data Management Console in one of the following ways.

<table id="choicetable_snz_r2m_13c"><thead><tr><th align="left" id="d132367e72">

Option

</th><th align="left" id="d132367e75">

Steps

</th></tr></thead><tbody><tr><td id="d132367e81">

**Overview tab**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; ****.
2.  On the Overview tab, select the table with records that you want to delete.
3.  Select **Create rule**.


</td></tr><tr><td id="d132367e119">

**Rules tab**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; ****.
2.  On the Tables tab, select the table with records that you want to delete.
3.  On the table details page, select the Rules tab.
4.  Select **Create rule**.


</td></tr></tbody>
</table>2.  Define the one-time delete rule.

    1.  On the Define your rule page, select **One-time delete** as the rule type.

    2.  Enter a name and description for the rule.

        The name is used as the [display value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DisplayValues.md) for references to this rule.

    3.  Select **Save and continue**.


## Define one-time delete rule conditions

Define one or more conditions that identify the records to be deleted.

### Before you begin

Role required: admin

### About this task

Use the condition builder to specify filter conditions that define the records to be deleted.

**Important:** Deleting records can cause unexpected cascade deletion. Preview the number of records that will be affected before activating the rule and change the conditions as needed.

### Procedure

1.  On the Define conditions page, limit the number of records by adding one or more conditions that records must meet.

    1.  Select a field, operator, and field value.

        For example, **\[Category\] \[is\] \[Software\]**.

    2.  Use the OR and AND operators to add conditions.

    3.  Select **Add condition set Criteria** to add another set of conditions.

    **Note:** Limiting the number of records that are added to the one-time delete job can help prevent the table from being locked when the job is executed.

2.  View the records that match the conditions by selecting **Preview affected records**.

    The list of records appears in a new browser tab.

3.  On the Define conditions page, select **Save and continue**.


## Select associated records to delete

Specify which associated records to delete when the one-time delete rule runs.

### Before you begin

Role required: admin

### About this task

Deleting records in a table also deletes records from tables that extend or reference the source table. Preview the affected records before you execute a delete job and learn about other tables that are impacted.

Up to three levels of cascaded records are deleted when the job is executed. For example, if the preview identifies incidents that match the conditions, it will also delete any problems that reference those incidents, defects that reference those problems, and test records that reference the defects. If sys\_attachment and sys\_attachment\_docs table records are associated with the incidents, those records might not appear in the preview but they are deleted as well.

### Procedure

1.  On the Delete associated records page, view the count of records from the source table that match the conditions in the one-time delete rule by selecting **Preview cascade**.

    The **Preview cascade delete records** dialog displays the estimate. Counts for records in other tables that reference those source records are listed as well, although those counts are only close estimates.

2.  Review the count of affected records by table to ensure that the records are safe to delete.

3.  Note that a rollback context is created by default.

    **Important:** If you need to restore records deleted by accident, you have up to fourteen days to execute the rollback job.

4.  Run predefined business rules after records are deleted by selecting **Run business rules and engines**.

5.  Select **Save and continue**.


## Schedule or execute a one-time delete rule

Schedule a date and time to execute a one-time delete rule or execute it after you finish creating it.

### Before you begin

Role required: admin

### About this task

Consider scheduling the one-time delete rule to run during non-business hours to minimize the potential performance impact on your users. Deleting all records in a table temporarily locks the table, which prevents inserts and updates. If you want to delete all records from a table, use a cleanup rule instead. For more information, see [Deleting older or unwanted records in Data Management Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/deleting-records.md).

### Procedure

1.  On the Set up schedule page, schedule the one-time delete rule to run now or at a later date.

<table id="choicetable_orr_f3t_13c"><thead><tr><th align="left" id="d132367e499">

Option

</th><th align="left" id="d132367e502">

Description

</th></tr></thead><tbody><tr><td id="d132367e508">

**Schedule later**

</td><td>

Set up a schedule at a later time.

</td></tr><tr><td id="d132367e517">

**Execute upon creation**

</td><td>

Run the one-time delete rule immediately after you finish creating it.

</td></tr><tr><td id="d132367e526">

**Run at**

</td><td>

Select a date and time to run the one-time delete rule.**Note:** Scheduling at a later date and time might affect a different number of records.

</td></tr></tbody>
</table>2.  Select **Save and continue**.


## View a summary of your one-time delete rule

View a summary of your one-time delete rule and acknowledge the deletion.

### Before you begin

You must activate the one-time delete rule and its corresponding data management policy for it to run.

Role required: admin

### Procedure

1.  On the Rule summary page, review the one-time delete rule conditions and settings.

2.  Read and verify the deletion by selecting the acknowledgment statement.


### Result

The one-time delete rule runs based on the chosen schedule and deletes records when they meet the conditions that you set for them.

