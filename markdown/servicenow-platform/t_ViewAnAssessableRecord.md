---
title: View an assessable record
description: View the Assessable Record form to edit preferences and perform various actions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Assessable records, Metric types and assessable records, Create an assessment metric for a category, Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View an assessable record

View the Assessable Record form to edit preferences and perform various actions.

## Before you begin

Role required: assessment\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Assessable Records**.

2.  Open a record from the list.

    By default, the list displays only assessable records with **Active** metric types.

3.  On the Assessable Record form, edit fields and perform other actions as necessary \(see table\).

<table id="table_lz1_whs_jp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

\[Read-Only\] Assessable record name based on the [Select a field as the table display value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_SelectTheDisplayValue.md) of the source record. The name appears on assessment questionnaires.

</td></tr><tr><td>

Source

</td><td>

\[Read-Only\] Source record the assessable record is linked to. The **Source** reflects the table name and source record display value. For example, if the **Name** field is the display value for the Company table, the assessable record for a company record named **Amazon** has the **Source** value **Company: Amazon**.

</td></tr><tr><td>

Live feed

</td><td>

Check box that, when selected, creates a Live Feed group for the assessable record, which appears on the scorecard. If you clear the check box after a Live Feed group has been created, the system deletes the Live Feed group and all its messages.

</td></tr><tr><td>

Type

</td><td>

\[Read-Only\] Metric type from which the assessable record was generated.

</td></tr><tr><td>

Decision matrix

</td><td>

Check box that, when selected, enables this assessable record's results data to appear on decision matrixes of the same metric type. Decision matrixes are graphs that plot the assessment results for multiple assessable records. If you clear the check box, the assessable record still appears on the default decision matrixes if you click the **View Matrix** related link on the assessable record's scorecard.

</td></tr><tr><td>

Live feed group

</td><td>

\[Read-Only\] Live feed group for this assessable record. When you select the **Live feed** check box and save the record, the system populates this field.

</td></tr><tr><td class="sub-head" colspan="2">

Related Links

</td></tr><tr><td>

View Scorecard

</td><td>

Opens the scorecard for the assessable record.

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

Category

</td><td>

All metric categories associated with the assessable record. An assessable record must be associated to a category to be evaluated. Click **Edit** to add or remove category associations. Note that it is often more efficient to [associate assessable records](../reference/r_ManageAssessablRecordAssociation.md) to categories using the Metric Category form.

</td></tr><tr><td>

Category users

</td><td>

All stakeholders who can take assessment questionnaires about this assessable record. Click **Edit** to create and delete stakeholders. For more information about this and other methods of creating stakeholders, see [Stakeholders](../reference/r_CategoryUsersAndStakeholders.md). This related list is available only when the associated metric type has the **Scheduled** schedule type.

</td></tr></tbody>
</table>
**Parent Topic:**[Assessable records](../concept/c_assessable-records.md)

**Parent Topic:**[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

**Related topics**  


[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

