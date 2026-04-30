---
title: Create a pulse survey in Listening Posts
description: Create a pulse survey under a theme. Publish the survey to enable users to receive and complete the survey.
locale: en-US
release: yokohama
product: Listening Posts
classification: listening-posts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Creating and delivering pulse surveys, Listening Posts, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Create a pulse survey in Listening Posts

Create a pulse survey under a theme. Publish the survey to enable users to receive and complete the survey.

## Before you begin

Role required: sn\_lp.creator

## Procedure

1.  Navigate to **Listening Posts** &gt; **Pulse Survey**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_pgp_pnd_knb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the pulse survey.

</td></tr><tr><td>

Theme

</td><td>

Theme to which you want to associate the pulse survey.

</td></tr><tr><td>

Add Audience

</td><td>

Option to add users who receive the pulse survey instances.**Note:** This field appears only when the Content Delivery plugin is installed.

</td></tr><tr><td>

Audience

</td><td>

Users with whom you want to share the pulse survey instances.**Note:**

-   This field appears only when you enable the **Add Audience** check box.
-   You can add audience for a survey using the **Audience** field or the **Survey Recipients List** related list. When you add users in both the **Audience** field and **Survey recipients List**, a union of those users receive pulse survey instances.


</td></tr><tr><td>

Send notifications

</td><td>

Option to notify users when a survey is assigned to them.

</td></tr><tr><td>

Send Mobile notifications

</td><td>

Option to send notifications on a mobile application.

</td></tr><tr><td>

Virtual Agent notifications

</td><td>

Option to send actionable notifications via Virtual Agent.

</td></tr><tr><td>

Description

</td><td>

Additional information about the pulse survey.

</td></tr><tr><td>

Active

</td><td>

Option for indicating that the pulse survey is active and available for use.

</td></tr><tr><td>

State

</td><td>

Current state of the pulse survey.-   **Draft**: State of the pulse survey when created.
-   **Ready**: State of the pulse survey before instances are created by the scheduled job.
-   **Published**: State after the survey instance is available to the audience.
-   **Closed**: State after the end date of the pulse survey. The survey is automatically set to closed state after its end date.


</td></tr><tr><td>

Auto-initiate conditions

</td><td>

Option to set up conditions to trigger feedback surveys.**Note:** This option appears only for a pulse survey that is associated to a theme of type **Employee lifecycle**.

</td></tr><tr><td>

Start date

</td><td>

Date starting which the pulse survey instances are sent to users.

</td></tr><tr><td>

End date

</td><td>

Date until which the pulse survey instances are available for users to respond.

</td></tr><tr><td>

Anonymity level

</td><td>

Level of anonymity that you want to set for an auto-initiated pulse survey.-   **Non-Anonymous**: Name and demographic details of users are captured along with their survey responses.
-   **Anonymous**: Only survey responses of the users are captured.
-   **Employee Choice**: User is given an option to make a choice while taking the survey on Employee Center: Keep their identity anonymous or non-anonymous.


</td></tr></tbody>
</table>4.  Click **Submit**.

5.  In the **Questions** related list:

    -   To add a question to the content, click **New**. For more information, see [Create a pulse question in Listening Posts](create-pulseq.md).
    -   To add a question from the Question Bank, click **From Question Bank**.
    **Note:** You cannot add or update questions once a survey is published.

6.  To create another copy of the survey, click **Copy**.

7.  Click **Schedule Publish**.

    **Note:** Clicking **Schedule Publish** ensures that the instances are created when the LP create group pulse instance scheduled job runs. This option is applicable when the start date is in the future.

8.  To publish survey instances immediately without waiting for a scheduled job run, click **Publish Immediately**.

    **Note:** The **Publish Immediately** option appears only for a survey that is associated to a theme of type Group pulse. The start date must be today or in the past, and there must be at least a day difference between the start date and the end date.

9.  To cancel a published survey, click **Cancel**.

    The pulse survey is closed; all the pulse survey instances which are yet to be taken are canceled, and completed instances remain unaffected.


## What to do next

-   In the **Pulse Users** related list, view the final lists of users to whom the pulse survey instances are sent. This related list is displayed only after a pulse survey is published and instances are available to users.
-   In the **Survey Recipients List** related list, add recipients to whom you want to send the survey instances.
-   In the **Feedback initiators** related list, click **New** to initiate feedback surveys based on trigger conditions. See [Automatically initiate a pulse survey from Listening Posts](auto-initiate-cnd.md).

-   **[Automatically initiate a pulse survey from Listening Posts](auto-initiate-cnd.md)**  
Send automated surveys to measure employee satisfaction with a recent experience, like closing an HR task initiated from a life cycle event, by applying auto trigger conditions.

**Parent Topic:**[Creating and delivering pulse surveys](../concept/create-deliver-surveys.md)

**Related topics**  


[Create a pulse question in Listening Posts](create-pulseq.md)

[Create a pulse theme in Listening Posts](create-pulse-theme.md)

[Create a pulse survey as content in Listening Posts](create-survey-content.md)

[Delivering pulse surveys in Listening Posts](../concept/delivery-pulse-content2.md#)

