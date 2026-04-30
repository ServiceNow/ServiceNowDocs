---
title: Schedule delivery of Microsoft Teams notification content
description: Schedule posting of notifications in Microsoft Teams channels.Complete the Schedule content form to schedule the posting of notifications in Microsoft Teams channels.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a Microsoft Teams campaign with content publishing, Sending notifications to employees using Microsoft Teams, Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Schedule delivery of Microsoft Teams notification content

Schedule posting of notifications in Microsoft Teams channels.

## Before you begin

Role required: sn\_cd.content\_manager, admin

## Procedure

1.  Navigate to **All** &gt; **Content Publishing** &gt; **Schedule Content**.

2.  Select the content to schedule.

3.  From the Schedule Content related list, select **New**.

4.  On the Schedule content form, fill in the fields.

    For a description of the field values, see [Schedule content form for Microsoft Teams notifications](schedule-delivery-content-mt.md#).

5.  Select **Submit**.


**Parent Topic:**[Create a Microsoft Teams campaign with content publishing](../concept/create-campaign-content-publishing-mt.md)

## Schedule content form for Microsoft Teams notifications

Complete the Schedule content form to schedule the posting of notifications in Microsoft Teams channels.

<table id="table_r2q_2gy_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content

</td><td>

Content or information you want to make available to employees.

</td></tr><tr><td>

Title

</td><td>

Name for the schedule content record.

 This field is automatically set to the name of your content selected in the **Content** field.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the schedule for content is active and available to employees.

</td></tr><tr><td>

Add Users

</td><td>

Option to indicate that you want to add specific users to view your content.

 Selecting this option clears the values in the **Audience** field.

</td></tr><tr><td>

Audience

</td><td>

Names of the users from the list who you want to see the content.

</td></tr><tr><td>

Approvers

</td><td>

Names of the users to approve the content before it is publicly available.

 **Note:** This field can contain only users with the Content Approver \[sn\_ca.content\_approver\] role.

</td></tr><tr><td>

When to process

</td><td>

Date and time on which you want the content to be sent, created, or posted.

</td></tr><tr><td>

Content status

</td><td>

The status of your to-do content.

 -   Pending: The Content Publishing scheduled jobs have not processed the content.
-   Scheduled: The content is scheduled and is queued to be processed.
-   Max Exceeded: The scheduled content exceeded the allowable time.

The maximum value is configured in the **sn\_cd.todo.max\_run\_time** property.

-   Error: An error in scheduling or posting the content occurred.

</td></tr><tr><td>

Completed on

</td><td>

The date and time the Content Publishing: Create To-dos scheduled job completed.

</td></tr></tbody>
</table>