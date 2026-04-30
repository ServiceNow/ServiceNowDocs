---
title: Automatically initiate a pulse survey from Listening Posts
description: Send automated surveys to measure employee satisfaction with a recent experience, like closing an HR task initiated from a life cycle event, by applying auto trigger conditions.
locale: en-US
release: yokohama
product: Listening Posts
classification: listening-posts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a pulse survey in Listening Posts, Creating and delivering pulse surveys, Listening Posts, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Automatically initiate a pulse survey from Listening Posts

Send automated surveys to measure employee satisfaction with a recent experience, like closing an HR task initiated from a life cycle event, by applying auto trigger conditions.

## Before you begin

Role required: sn\_lp.creator

## Procedure

1.  Navigate to **Listening Posts** &gt; **Pulse Survey**.

2.  Select a survey.

3.  Enable the **Auto-initiate conditions** option to set up conditions for initiating feedback surveys on completion of a task.

    **Note:** The **Auto-initiate conditions** option appears only if the survey is associated to a theme of type **Employee lifecycle**.

4.  In the **Feedback Initiators** related list, click **New**.

    **Note:** Feedback Initiators work only for the HR tasks of Listening Posts V3 or a later version.

<table id="table_bxz_kp3_qqb"><thead><tr><th>

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

Table to run the trigger condition on. You can select only tables in the current application scope. For example, to send a survey whenever an HR task closes, select the HR task \[sn\_hr\_core\_task\] table.

</td></tr><tr><td>

User field

</td><td>

Field that stores users to whom you want to send the survey. You can select any field, on the selected table or on a referenced table that references the User \[sys\_user\] table. Use the tree picker to select a field.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether this trigger condition is active \(selected\).

</td></tr><tr><td>

Trigger randomly

</td><td>

Check box that determines whether to send the survey to the appropriate user every time the condition is met \(cleared\) or only a percentage of the time \(selected\).

</td></tr><tr><td>

Probability \(%\)

</td><td>

Approximate probability that the survey is sent each time the condition is met. For example, if the probability is set to 50, the system sends the survey approximately 50% of the time the conditions are met. There are no repeat interval restrictions is assumed. This field is visible and required only when Trigger randomly is selected.

</td></tr><tr><td>

Description

</td><td>

Summary information to identify the trigger condition.**Note:** For a triggered record, the table title is used for the survey description.

</td></tr><tr><td>

Condition

</td><td>

Condition builder that defines the criteria that must be true to send the survey. For example, to send a survey whenever an HR task closes, create the condition \[State\] \[is\] \[Closed\].

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Create a pulse survey in Listening Posts](create-pulse-survey.md)

