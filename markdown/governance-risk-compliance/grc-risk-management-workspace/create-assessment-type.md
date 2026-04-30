---
title: Create an assessment type
description: The risk manager can create a set of questions for each risk assessment.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Assess risks, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create an assessment type

The risk manager can create a set of questions for each risk assessment.

## Before you begin

Role required: sn\_risk.asmt\_creator or sn\_risk.manager or sn\_risk.administrator

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Administration** &gt; **Assessment Types**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the assessment type.

</td></tr><tr><td>

Assessment duration

</td><td>

Number of time assessors have to complete their assigned questionnaires, starting from the time the assessment is generated.

</td></tr><tr><td>

Table

</td><td>

Table that contains the records you want to evaluate. The system creates assessable records for records on this table that meet the conditions you specify, if any. The number of matching records appears as a link by the **Condition** field. If you change the table selection, the link dynamically updates. Select the link to open the list of matching records in a new tab or window.**Note:** More roles are required to view the records on certain tables. If you select a table that you don’t have access to, a warning message appears by the Condition field where the number of matching records would be. You can’t generate assessable records for tables you don’t have sufficient roles for.

</td></tr><tr><td>

Scale factor

</td><td>

Number to represent the best possible score for assessment results. All results for assessments of this type are scaled to this number. 10 is generally a good scale factor.**Note:** This field becomes read-only when it contains a value and you save the metric type. Choose a scale factor that you’re satisfied with before you save the metric type.

</td></tr><tr><td>

Condition

</td><td>

Condition builder that defines specific records to assess from the selected table. If you don’t specify any conditions, the system creates assessable records for all records on the selected table. Select the refresh icon to update the adjacent record count.**Note:** If you change the table or conditions, you must select **Generate Assessable Records** to create new assessable records.

</td></tr><tr><td>

Description

</td><td>

Helpful information about this type. Enter a clear description of the type and its purpose.

</td></tr><tr><td>

State

</td><td>

Status of the assessment: **Draft** or **Published**.

</td></tr><tr><td>

Enforce condition

</td><td>

Option that determines what happens to assessable records when you change the selected table or conditions.

</td></tr><tr><td>

Roles

</td><td>

Additional user roles that can view the results and access records associated with this type. Users with the specified roles have read access to this type record and to the associated categories, metrics, assessable records and scorecards, category users, stakeholders, and decision matrixes.

**Note:** Users with these roles don’t have access to Assessments modules unless they’re assessment administrators. Users with these roles can navigate to the records by other means, such as from reference fields on assessment instances. This field provides the option to grant user access to specific assessment data in special cases. For example, the Vendor metric type provides access to users with the vendor\_manager role to view results and compare assessable records when they open scorecards or decision matrixes in the Vendor Performance application.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Assess risks](../concept/assess-risk-old-way.md)

