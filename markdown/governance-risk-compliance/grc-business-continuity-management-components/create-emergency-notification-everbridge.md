---
title: Create an emergency notification and monitor its workflow
description: Use the Emergency notification tab in the event workspace to create a notification for a crisis event or an exercise event where the exercise method is Functional.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrating Crisis Management with Everbridge, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create an emergency notification and monitor its workflow

Use the **Emergency notification** tab in the event workspace to create a notification for a crisis event or an exercise event where the exercise method is Functional.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager, or sn\_bcm.admin

## About this task

Send an event notification from the workspace that triggers a complete workflow of activities from the **Draft** to **Complete** state in Everbridge, where all the activities can be monitored from the workspace.

When you send an emergency notification from the workspace, the action creates an incident and a notification for the incident in Everbridge to be sent to the right contacts and groups.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click **Pending** state in the Crisis Events list.

    **Note:** If the **Exercise Method** is **Functional**, then you can create an emergency notification for an exercise event.

4.  Click the link to the event record in the **Number** column.

5.  Click the **Emergency Notifications** related list.

6.  Click **New**.

    New Notification form opens in a separate tab.

7.  On the form, fill in the fields.

<table id="table_ot2_4zs_rpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Title of the emergency notification

</td></tr><tr><td>

Template

</td><td>

Pre-configured template that has the subject of the mail and the delivery channels for the contacts.

</td></tr><tr><td>

Notification state

</td><td>

State of notification in the ServiceNow workspace.

</td></tr><tr><td>

Communication status

</td><td>

State of notification in Everbridge.

</td></tr><tr><td>

Description

</td><td>

Description of the notification.

</td></tr><tr><td class="sub-head" colspan="2">

Contacts and Groups

</td></tr><tr><td>

Contacts

</td><td>

Persons to whom the notification is sent.Contacts that are successfully synced with Everbridge are listed.

</td></tr><tr><td>

Notification contact groups

</td><td>

Groups of contact to whom the notification is sent.Successfully synced contact groups are listed.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Acknowledgement required

</td><td>

Option if an acknowledgement is required from the contact for the notification received.

</td></tr><tr><td>

Delivery channels

</td><td>

Communication channels used for sending the notification.

</td></tr><tr><td class="sub-head" colspan="2">

Message Details

</td></tr><tr><td>

Subject

</td><td>

Title of the notification.

</td></tr><tr><td>

Message body

</td><td>

Introductory text message for the notification.If a template is selected, then the message details are auto-populated from the template.

</td></tr><tr><td>

Foot note

</td><td>

Closing message for the notification.

</td></tr><tr><td>

SMS text

</td><td>

Message sent through SMS.

</td></tr></tbody>
</table>    The notification that you create is in **Draft** stage.

8.  To save the notification and send it later, click **Save**.

9.  To delete the notification that is in **Draft** stage, click **Delete**.

10. Click **Send**.

    The send action creates a notification in Everbridge.

    When you create and send a notification for a crisis event in the workspace, a corresponding incident is created along with a notification in Everbridge.

11. To know if there are any errors in sending the notification, refresh the page.

    If there is an error in sending, the **Notification state** moves to **Error**.

12. To get the state from Everbridge for the notification sent to the contacts in the **Communication status** field, click the **Get response status** button.

    The **Summary** section displays the list of contacts and groups to whom the notification was sent and their responses. It also displays the number of contacts who could not be reached, the number of contacts who acknowledged the notification, and the number of pending acknowledgements. This information is retrieved from Everbridge and displayed on your workspace.

    ![Summary of the notification sent to contacts.](../image/SummaryEmergNotif.png "Summary of the notification sent to contacts")

    -   **Sent to**

        Number of contacts to whom the notification was sent.

    -   **Unreachable**

        Number of contacts to whom notification was not sent.

    -   **Acknowledged**

        Number of contacts who acknowledged the receipt of notification.

    -   **Pending acknowledgement**

        Number of contacts who did not acknowledge the receipt of notification.

    -   **Late acknowledgement**

        Number of contacts who confirmed the receipt of notification after the notification duration had elapsed.

    If there are many contacts to whom the notification could not be delivered, then create another notification for the same crisis event. This time, you can send to a team of managers, as the previous notification did not reach many contacts.

    Before you submit an event for approval, all the notifications that are In Progress must be closed.

    1.  To delete a notification that is in **Draft** or **Error** state, click the link to the emergency notification record in the **Number** column.

        **Note:** You cannot delete a notification that is in **Attempting to send**, **In Progress** or **Completed** state.

    2.  Click **Delete** in the more actions icon \(![More actions action for delete action.](../image/MoreActionsicon.png)\).

        **Note:** Now that the event is closed and the corresponding incident in Everbridge is also closed, you cannot create any more notifications for this event.


