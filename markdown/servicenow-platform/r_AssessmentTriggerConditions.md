---
title: Assessment trigger conditions
description: A trigger condition tells the system who to send a designated assessment to and when, based on specific conditions.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure trigger conditions for an assessment, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment trigger conditions

A trigger condition tells the system who to send a designated assessment to and when, based on specific conditions.

With trigger conditions, assessment administrators can configure the system to generate assessments each time a specific action occurs, such as when an incident or change request closes. The trigger condition sends the assessment to specified users who are related to the triggering record, such as incident callers or change request assignees. You can choose to send the assessment every time the condition is met, or set a probability for the system to send the assessment at random when the condition is met.

For a description of the field values in Trigger Condition form, see [Trigger Condition form for assessments](trigger-condition-form-for-assessment.md).

<table id="table_znx_kb2_5s"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Assessment

</td><td>

Vendor

</td></tr><tr><td>

Table

</td><td>

Incident `[incident]`

</td></tr><tr><td>

User field

</td><td>

Assigned to

</td></tr><tr><td>

Repeat Interval

</td><td>

30 days

</td></tr><tr><td>

Active

</td><td>

true

</td></tr><tr><td>

Trigger randomly

</td><td>

false

</td></tr><tr><td>

Assessable Record Field

</td><td>

VendorThis is a field in the table that is selected from the **Table** field. The reference record selected in the field specified must have an assessable record.

 **Note:** The values in this field must have assessable records of the selected metric type. If this condition is met, then only the assessment is triggered.

</td></tr><tr><td>

Related Field 1

</td><td>

Caller

</td></tr><tr><td>

Related Field 2

</td><td>

Vendor

</td></tr><tr><td>

Condition

</td><td>

\[State\] \[is\] \[Closed\] and \[Vendor\] \[is not empty\]

</td></tr></tbody>
</table>## Trigger condition example

Modesto Scroggie is the caller on an incident that is assigned to Boris Catino, a service desk technician. Boris contacts a vendor to resolve Modesto's issue and sets the **Vendor** field to **Microsoft**. When the incident closes, the system creates an assessment instance assigned to Boris so Boris can evaluate Microsoft as a vendor.

Because two related fields were selected as part of the trigger condition, the assessment instance stores the following information from the incident:

-   **Related record 1:** User: Modesto Scroggie
-   **Related record 2:** Company: Microsoft

**Note:** Even though the trigger condition is set to be triggered every time the conditions are met, the **Repeat Interval** setting ensures that Boris does not receive another assessment if another vendor incident assigned to him closes within 30 days of the first one.

**Parent Topic:**[Configure trigger conditions for an assessment](../task/t_CreateTriggerAssessment.md)

