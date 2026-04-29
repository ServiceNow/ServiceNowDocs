---
title: Notification example: notify an assignment group of updates to Priority 1 Incidents
description: Notify users by email when there are updates to high priority incidents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Notification example: notify an assignment group of updates to Priority 1 Incidents

Notify users by email when there are updates to high priority incidents.

## Before you begin

Role required: admin

## About this task

Send emails to an assignment group whenever there are updates to an incident in which the **Priority** is **1 - Critical**. Include information that is of interest to the recipients, such as the incident number, category, assignees, and any comments that were added to the incident.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**, and then click **New**.

2.  On the email notification form, enter the following values:

<table id="table_gbc_bxz_x4"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Priority 1 Incident Updated

</td></tr><tr><td>

Table

</td><td>

Incident \[incident\]

</td></tr><tr><td>

Active

</td><td>

Selected

</td></tr><tr><td>

Category

</td><td>

Incident Alert

</td></tr><tr><td>

Send when

</td><td>

Record inserted or updated

</td></tr><tr><td>

Inserted

</td><td>

Selected

</td></tr><tr><td>

Updated

</td><td>

Selected

</td></tr><tr><td>

Conditions

</td><td>

\[Priority\]\[is\]\[1 - Critical\] AND \[Updated\]\[changes\]

</td></tr><tr><td>

Users/Groups in fields

</td><td>

Assignment group

</td></tr><tr><td>

Subject

</td><td>

```
Priority ${priority} Incident updated
```

 **Note:** In this notification, the variable $\{priority\} returns the value **1 - Critical**.

</td></tr></tbody>
</table>3.  In the **Message HTML** field, enter the following message and script:

    ```
    Short Description: ${short_description}
    Click here to view incident: ${URI}
    Incident number: ${number}
    Category: ${category}
    Assigned to: ${assigned_to}
    Assignment group: ${assignment_group}
    <hr/>
    Comments:
    ${comments}
    ```

4.  From the form context menu, click **Save**.

5.  Preview the email notification to ensure it includes all the needed information.

    1.  On the notifications form, click **Preview Notification**.

    2.  Note that the email includes the following information:

        -   Short description
        -   A link to the incident record
        -   Incident number
        -   Category
        -   The name of the user to whom the incident is assigned
        -   The group assigned to the incident
        -   Comments from the incident record
6.  Test that the email notification sends to an assignment group when its Priority 1 Incident is updated.

    1.  [Create a user](../../users-and-groups/task/t_CreateAUser.md) who has an email address that you can monitor, and then [create a group](../../users-and-groups/task/t_CreateAGroup.md#) that includes the user that you created.

    2.  Navigate to **Incident** &gt; **Open**, and then open an incident in which the **Priority** is **1 - Critical**.

    3.  In the **Assignment group** field, enter the group that you created.

    4.  From the form context menu, click **Save**.

    5.  Add comments to the form to update the incident, and then click **Update**.

    6.  Check the email account of the user member in the assignment group.


**Parent Topic:**[Create an email notification](t_CreateANotification.md)

