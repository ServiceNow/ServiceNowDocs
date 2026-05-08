---
title: Define trigger conditions for a coaching opportunity
description: Use the Coaching Opportunity form to define a critical moment in a process on which a user can be coached. A coaching opportunity consists of the relationship between a process that can be improved, and coaches and trainees.
locale: en-US
release: australia
product: Coaching
classification: coaching
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Coaching, IT Service Management]
---

# Define trigger conditions for a coaching opportunity

Use the Coaching Opportunity form to define a critical moment in a process on which a user can be coached. A coaching opportunity consists of the relationship between a process that can be improved, and coaches and trainees.

## Before you begin

Role required: sn\_coaching.admin

## About this task

When the triggered conditions defined in a coaching opportunity are met, an assessment for that trainee is generated. The coaching assessment is then assigned to a coach for training, or is completed using automated virtual learning content.

## Procedure

1.  Create a coaching opportunity using the guided setup or by using the application navigator.

<table id="choicetable_wfs_345_4lb"><thead><tr><th align="left" id="d402250e68">

To create using

</th><th align="left" id="d402250e71">

Do this

</th></tr></thead><tbody><tr><td id="d402250e77">

**Guided setup**

</td><td>

1.  Navigate to **Continual Improvement** &gt; **Administration** &gt; **Guided Setup**.
2.  Go to the **Add a Coaching Opportunity** section and select **Configure**.


</td></tr><tr><td id="d402250e113">

**The Application navigator**

</td><td>

Navigate to **Coaching** &gt; **Coaching Opportunities**.

</td></tr></tbody>
</table>2.  Select **New**.

3.  Fill in the fields on the Coaching Opportunity form.

    1.  Select the table that contains the field for coaching in the **Table** field.

    2.  Select the **Trainee field** from the source table.

    3.  To limit the trainees for which a coaching assessment is generated, select a specific **Trainee group**.

    4.  Select a coach or a group of coaches to assess and provide feedback to trainee assessments generated from this coaching opportunity.

        -   To select a coach group, from the **Coach group** field, select the group of coaches.
        -   To select the assignment group manager as the coach for the selected task record, enable the **Specify coach user** check box and select the coach user from the selected table.
    5.  Add the condition for the critical moment in the **Trigger** fields.

        See [Common ITSM assessment triggers](../concept/cf-coaching-overview.md#section_b5h_3cd_gfb) for examples.

4.  Fill in the fields in the **Snapshot Settings** tab.

    1.  Select the **Snapshot fields** that contain the values to capture in the coaching assessment when an assessment is triggered.

    2.  To use an advanced script, select the **Advanced** check box and add your script.

        See Scripts for more information on scripting.

5.  Fill in the fields in the **Frequency** tab.

    1.  To limit the number of coaching assessments generated, set the **Random sample \(%\)** to a percentage of the total number.

        If you reduce the random sample size, you can avoid certain trainees from being excluded by specifying **Users who should be coached on every opportunity**. For example, you may want new employees to be coached every time.

    2.  Specify the **Assessment duration** after which the coaching assessment is set to **Closed Complete** state.

        You can disable automatic closure behavior by deactivating the **Close assessments after expiration** scheduled job.

    3.  To **Prevent duplicate assessments** from being created for a trainee for the same coaching opportunity within a certain time period, select the check box.

        Specify the **Time period** within which duplicate assessments are not created.

6.  Fill in the fields in the **Surveys** tab.

    1.  To select feedback surveys taken by trainees and coaches when the coaching assessment is in **Resolved** state, select a **Survey taken by Coach** and a **Survey taken by Trainee**.

7.  Fill in the fields in the **Related KPIs** tab.

    1.  Select the primary KPI improved by the coaching opportunity in the **Improvement KPI** field.

    2.  Select the **Strategic objective** affected by the coaching opportunity in the **Strategic objective** field.

        **Note:** You can set strategic objectives by navigating to **Continual Improvement** &gt; **Strategy Objectives**.

        You can add [assigned trainings and virtual coach](cf-identify-learning-content.md) items to the related lists, if applicable, to complete the coaching opportunity.


## Coaching admin defines a trigger condition

|Field|Value|
|-----|-----|
|Number|COP0000109|
|Name|Incident Process: Coaching on Incident Reassignment|
|Description|Coach a user on the reassignment process of an incident, including adding comments, CI, and category.|
|Table|Incident \[incident\]|
|Trainee|Assigned to|
|Trainee group|Trainee group|
|Coach group|Coach Group|
|Active|Selected|
|Trigger|Option: Assigned to|
|Operator: changes|

|Field|Value|
|-----|-----|
|Frequency|
|Random sample \(%\)|100|
|Assessment duration|5 days|
|Surveys|
|Survey taken by Coach|Trainee Assessment Survey \(provided by coach\)|
|Survey taken by Trainee|Coach Effectiveness Survey \(provided by trainee\)|
|Related KPIs|
|Improvement KPI|Number of reassigned open incidents|
|Strategic objective|Retrofit Staffing to include more global logistics|
|Snapshot Settings|
|Snapshot fields|Resolution code, Resolution notes, Work notes|

**Parent Topic:**[Configuring Coaching](../concept/cf-configuring-coaching.md)

**Related topics**  


[Coaching field descriptions](../reference/cf-coaching-field-descriptions.md)

