---
title: Create an archive rule in Data Management Console
description: Define a rule for archiving records.Define one or more conditions that identify the records to be archived.Delete archived records after a specified amount of time by configuring optional destroy rule conditions.Archive, clear, or delete related records when an archive rule runs.View a summary of your archive rule and decide whether to activate it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/dmc-create-archive-rule.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Archiving records in Data Management Console, Manage data growth in Data Management, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an archive rule in Data Management Console

Define a rule for archiving records.

## Before you begin

Role required: admin

## About this task

Because you can define multiple archive rules for a table, verify any existing archive rules to avoid potential conflicts. For example, if there's a rule for archiving records older than six months, creating another rule to archive records older than three months could cause a conflict. In such cases, either rule could potentially run, each archiving records under different conditions.

## Procedure

1.  Access the create rule wizard in the Data Management Console in one of the following ways.

<table id="choicetable_snz_r2m_13c"><thead><tr><th align="left" id="d281335e67">

Option

</th><th align="left" id="d281335e70">

Steps

</th></tr></thead><tbody><tr><td id="d281335e76">

**Overview tab**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; ****.
2.  On the Overview tab, select the table with records that you want to archive.
3.  Select **Create rule**.


</td></tr><tr><td id="d281335e114">

**Rules tab**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; ****.
2.  On the Tables tab, select the table with records that you want to archive.
3.  On the table details page, select the Rules tab.
4.  Select **Create rule**.


</td></tr></tbody>
</table>2.  Define the archive rule.

    1.  On the Define your rule page, select **Archive** as the rule type.

    2.  Enter a name and description for the rule.

        The name is used as the [display value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DisplayValues.md) for references to this rule.

    3.  Select **Save and continue**.


## Define archive rule conditions

Define one or more conditions that identify the records to be archived.

### Before you begin

Role required: admin

### About this task

Use the condition builder to specify filter conditions that define the records to be archived. For example, you might archive inactive records older than a certain date.

Make sure that the correct records are selected by testing the conditions in a list view before you activate the archive rule. For example,

-   To archive records closed more than two years ago from today, use the relative operator in a condition like **\[Closed\] \[relative\] \[before\] \[2\] \[Years\] \[ago\]**.
-   To archive records for the current year and the prior year, and not two years ago from today's date, use a condition like **\[Closed\] \[on\] \[Last 2 years\]**.

### Procedure

1.  On the Define conditions page, limit the number of records by adding one or more conditions that records must meet.

    1.  Select a field, operator, and field value.

        For example, **\[Category\] \[is\] \[Software\]**.

    2.  Use the OR and AND operators to add conditions.

    3.  Select **Add condition set Criteria** to add another set of conditions.

2.  Estimate the number of records to archive by selecting **Calculate archive estimate**.

    The estimate only includes primary records and excludes any related records added to the archive rule. The estimate helps you determine if the archive rule affects the number of records you expect it to. If the estimate is too high or low, change the archive rule conditions accordingly.

3.  Automatically send restored records back to the archive after a set time period.

    1.  Select **Auto-rearchive**.

    2.  Enter the time interval in years, days, and hours before the restored record is automatically archived.

4.  Select **Save and continue**.


## Define destroy rule conditions

Delete archived records after a specified amount of time by configuring optional destroy rule conditions.

### Before you begin

Role required: admin

### About this task

Optionally, use the condition builder to specify filter conditions that define the archive records to be destroyed. For example, you might delete archive records older than five years.

Skip this page and advance to the next one if you don't want to configure a destroy rule now.

### Procedure

1.  On the Destroy archived records page, select **Destroy archived records**.

2.  Specify the amount of time that records stay in the archive table before the system deletes them by entering a value for the archive duration in years, days, and hours.

    The default archive duration is one year.

    **Important:** Archive records are destroyed immediately if all **Archive Duration** fields are empty or set to 0.

3.  Automatically destroy related records associated with the archived records by selecting **Destroy related records**.

    **Note:** Associated records, which include records in the Journal Entry \[sys\_journal\_field\], Attachment \[sys\_attachment\], and Sys Audit \[sys\_audit\] tables are deleted automatically, even if you decide to preserve related records.

4.  Estimate the number of archived records marked for deletion by selecting **Recalculate Destroy Estimate**.

5.  Activate the destroy rule by selecting **Activate archive destroy rule**.

6.  Select **Save and continue**.


### Result

After the archive destroy rule is activated, records that have been archived longer than the archive duration value are destroyed when the scheduled job runs. You can verify the progress by checking the archive destroy log.

## Manage related records

Archive, clear, or delete related records when an archive rule runs.

### Before you begin

Role required: admin

### Procedure

1.  On the Manage related records page, select **+ Add records**.

2.  Select which action to take on related records in the **Action** list.

    |Action|Description|
    |------|-----------|
    |**Archive**|Archive records that reference the archived record.|
    |**Clear**|Remove the reference to the archived record. The record no longer references the archived record and doesn't appear as a related record in future archives.|
    |**Cleanup**|Delete records that reference the archived record.|

3.  Select the related records that you want to archive, clear, or delete by selecting a relationship in the **Reference** list.

    The **Reference** list contains all the relationships that exist to the archived table. There are two types of relationships in the list.

    -   **Reference fields**

        The list contains reference fields in other tables that refer to the archived table.

        For example, you create an archive rule on the Problem \[problem\] table. You can include related incident records by selecting the **Problem in Incident** field reference field on the Incident \[incident\] table.

        -   The **Archive** action archives any incident record that references an archived problem.
        -   The **Clear** action updates any incident record with a reference to the archived problem record by clearing the reference. If the reference is a [many-to-many relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_ManyToManyTaskRelations.md), the related record rule deletes the reference instead of clearing the reference.
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
4.  Apply an archive rule to the related records that you're archiving by selecting a rule in the **Reference table rule** list.

    For example, if you already have an archive rule for the Incident \[incident\] table, select the existing incident archive rule when archiving records related to incidents records.

    **Note:** You control the cascade depth by specifying an archive rule in the **Reference table rule** field. Related records without a specified archive rule aren't cascaded.

    -   Prior to the Washington DC release, if an archive rule was defined in the system for a related record's table, the system would automatically cascade and process that archive rule and the related records associated with it.
    -   Beginning in the Washington DC release, even if an archive rule exists for a related record's table, you must declare that rule in the **Reference table rule** field to achieve that cascading behavior. If you have multiple related records on multiple tables, you can decide which of those records you want to include in the cascade by specifying the reference table rule.
5.  Select **Add**.

6.  Add or delete more related records entries as needed.

7.  Select **Save and continue**.


## View a summary of your archive rule and activate it

View a summary of your archive rule and decide whether to activate it.

### Before you begin

You must activate the archive rule and its corresponding data management policy for the archive rule to run.

Role required: admin

### Procedure

1.  On the Rule summary page, review the archive rule conditions and settings.

2.  Activate the rule by selecting **Activate the rule upon creation**.


### Result

Records that meet the archive rule criteria are archived during the next archive run.

