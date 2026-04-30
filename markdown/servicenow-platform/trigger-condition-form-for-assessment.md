---
title: Trigger Condition form for assessments
description: Description of the field values for the Trigger Condition form for assessments.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Assessments reference, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Trigger Condition form for assessments

Description of the field values for the Trigger Condition form for assessments.

<table id="table_ynv_khz_x4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment

</td><td>

\[Required\] Metric type to generate assessment instances for. Triggered assessments only work if the metric type is set to the **On demand** schedule type.

</td></tr><tr><td>

Table

</td><td>

\[Required\] Table to run the trigger condition on. You can select only tables in the current application scope. The table must have a connection to the assessable records for the selected **Assessment**. For example, you might want to send a vendor assessment when incidents close that are related to vendors you assess. In this case, select the Incident \[incident\] table. After you select a table, ensure there is at least one option for the **Assessable Record Field**. If there is not, select a different table.

</td></tr><tr><td>

User field

</td><td>

\[Required\] Field that stores the users you want to send the assessment. You can select any field, on the selected **Table** or on a related table, that references the User \[sys\_user\] table. Use the tree picker to select a field.![Tree picker](../images/SelectUserField.png)

</td></tr><tr><td>

Repeat Interval

</td><td>

Minimum period that must pass before the trigger condition can resend the assessment to the same user. For example, assume the repeat interval is set to 30 days. Even if the same user is eligible for multiple assessments from this trigger condition, the system can only send the user one assessment every 30 days.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether this trigger condition is active \(selected\).

</td></tr><tr><td>

Business rule

</td><td>

\[Admin only\] Business rule the system creates to monitor the selected table. When the condition is met, the business rule sends the assessment to the correct user. No configuration is necessary for this business rule.

</td></tr><tr><td>

Trigger randomly

</td><td>

Check box that determines whether to send the assessment to the appropriate user every time the condition is met \(cleared\) or only a percentage of the time \(selected\), as specified in the **Probability \(%\)** field.

</td></tr><tr><td>

Probability \(%\)

</td><td>

Probability out of 100 that the assessment will be sent each time the condition is met. For example, if the probability is set to 50, the system sends the assessment approximately 50% of the time the conditions are met, assuming there are no repeat interval restrictions. This field is visible and required only when the **Trigger randomly** check box is selected.

</td></tr><tr><td>

Assessable Record Field

</td><td>

\[Required\] Field on the selected **Table** that determines which assessable record will be the subject of the assessment. Only appropriate reference fields on the selected **Table** are available to select. If there are no **Assessable Record Field** options available, you must select a different **Table**.

 If the selected **Assessment** evaluates records on the Company `[core_company]` table and the selected **Table** is Incident, the only **Assessable Record Field** options are fields on the Incident table that reference the Company table. For example, **Company** or, if vendor ticketing is enabled, **Vendor**. If you select **Vendor**, the trigger condition sends an assessment about the **Vendor** for the incident, assuming there is an assessable record for the associated company. The assessment contains questions from all metric categories associated with the assessable record.

**Note:** This field is not available if the selected **Assessment** is a metric type used for surveys. See [Survey trigger conditions](../../survey-administration/concept/c_TriggerConditions.md).

</td></tr><tr><td>

Related Field 1 – Related Field 4

</td><td>

Field that contains a value you want to store for reporting purposes. You can pick any reference field on the selected **Table**. When the trigger condition generates an assessment instance, the system stores the value from the triggering record. Select up to four fields.

 For example, if you select the Incident table, you might select **Caller** and **Vendor** as related fields. That stores the caller and vendor associated with the incident as **Related record 1** and **Related record 2** in the assessment instance record. To view these fields, configure the Assessment Instance form.

</td></tr><tr><td>

Description

</td><td>

Summary information to identify the trigger condition.

</td></tr><tr><td>

Condition

</td><td>

\[Required\] Condition builder that defines the criteria that must be true to send the assessment. For example, if you want to send an assessment whenever an incident closes, create the condition \[State\] \[is\] \[Closed\].

</td></tr></tbody>
</table>**Parent Topic:**[Assessments reference](assessment-reference.md)

**Related topics**  


[Configure a trigger condition for a survey](../../survey-administration/task/t_CreateATriggerCondition.md)

