---
title: Trigger Condition form for surveys
description: Description of the field values for the Trigger Condition form for surveys.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Trigger Condition form for surveys

Description of the field values for the Trigger Condition form for surveys.

<table id="table_TriggerConditionFields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment

</td><td>

Survey to send.

</td></tr><tr><td>

Table

</td><td>

Table to run the trigger condition on. You can select only tables in the current application scope. For example, to send a survey whenever an incident closes, select the Incident \[incident\] table.

</td></tr><tr><td>

User field

</td><td>

Field that stores the users you want to send the survey. You can select any field, on the selected table or on a referenced table, that references the User \[sys\_user\] table. Use the tree picker to select a field.**Note:** To avoid requiring users to log in to take a survey with a trigger condition, set the survey to **Public**.

</td></tr><tr><td>

Repeat interval

</td><td>

Minimum period that must pass before the trigger condition can resend the survey to the same user. For example, assume the repeat interval is set to 30 days. Even if the same user qualifies for multiple surveys from this trigger condition, the system can send only one survey every 30 days. **Note:**

-   Ensure that the Schedule period of the selected survey definition is set to **No Limit**. If the schedule period is set to a different value, it prevents the trigger condition from sending surveys as expected.
-   Trigger condition creates a survey instance irrespective of the repeat interval if the survey is set as anonymous.

</td></tr><tr><td>

Application

</td><td>

\[Admin only\] Application is set to Core.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether this trigger condition is active \(selected\).

</td></tr><tr><td>

Business rule

</td><td>

\[Admin only\] Business rule the system creates to monitor the selected table. When the condition is met, the business rule sends the survey to the correct user. No configuration is necessary for this business rule.

</td></tr><tr><td>

Trigger randomly

</td><td>

Check box that determines whether to send the survey to the appropriate user every time the condition is met \(cleared\) or only a percentage of the time \(selected\).

</td></tr><tr><td>

Probability \(%\)

</td><td>

Approximate probability that the survey is sent each time the condition is met. For example, if the probability is set to 50, the system sends the survey approximately 50% of the time the conditions are met. There are no repeat interval restrictions is assumed. This field is visible and required only when Trigger randomly is selected.

</td></tr><tr><td>

Related Field 1- 4

</td><td>

Field that contains a value you want to store for reporting purposes. You can pick any reference field on the selected table. When the trigger condition generates a survey instance, the system stores the value from the triggering record. Specify up to four fields. For example, select the Incident table, **Assigned to** and **Problem** as related fields. The system stores the assigned user and problem associated with the incident as Related record 1 and Related record 2 in the survey instance record. To view the fields, configure the form for any survey instance.

 **Note:** You cannot use a related field for the ticket number because you cannot select the Number column. You can, however, use the trigger\_id column of the table.

</td></tr><tr><td>

Description

</td><td>

Summary information to identify the trigger condition. **Note:** For a triggered record, the table title is used for the survey description.

</td></tr><tr><td>

Condition

</td><td>

Condition builder that defines the criteria that must be true to send the survey. For example, to send a survey whenever an incident closes, create the condition **\[State\] \[is\] \[Closed\]**.**Note:**

-   When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Survey triggers will not function as expected when you use dot-walk conditions in the **Condition** field.

</td></tr></tbody>
</table>**Parent Topic:**[Surveys reference](survey-reference.md)

**Related topics**  


[Configure a trigger condition for a survey](../task/t_CreateATriggerCondition.md)

