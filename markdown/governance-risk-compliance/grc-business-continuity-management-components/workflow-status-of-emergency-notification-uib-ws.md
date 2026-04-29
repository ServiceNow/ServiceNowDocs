---
title: Status of emergency notifications
description: When you send an emergency notification for a crisis event with Everbridge, it creates a corresponding incident along with a notification. You can track the notification delivery and monitor its status in the Business Continuity Workspace until it’s successfully delivered to the contacts from Everbridge.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, Business Continuity Management, Governance, Risk, and Compliance]
---

# Status of emergency notifications

When you send an emergency notification for a crisis event with Everbridge, it creates a corresponding incident along with a notification. You can track the notification delivery and monitor its status in the Business Continuity Workspace until it’s successfully delivered to the contacts from Everbridge.

## Status flow for an emergency notification

The status flow for an emergency notification lists different states of an emergency notification in Everbridge. The short description of the event in the Business Continuity Workspace is created as an incident with a notification in Everbridge.

-   **Notification state**

    The emergency notification that is created and sent from the ServiceNow Business Continuity Management Workspace is tracked in the **Notification state** field.

-   **Communication status**

    The emergency notification that is received in Everbridge and the different stages to which it moves until it’s delivered are tracked in the **Communication status** field.


<table id="table_d1h_3gt_rpb"><thead><tr><th>

Notification state

</th><th>

Communication status

</th></tr></thead><tbody><tr><td>

**Draft**: The draft of the notification is stored in Business Continuity Workspace.

</td><td>

**None**

</td></tr><tr><td>

**Attempting to send**: The notification is being sent from Business Continuity Workspace.

</td><td>

**None**

</td></tr><tr><td>

**Error**: An error occurs in creating the notification in Everbridge.

</td><td>

**None**

</td></tr><tr><td>

**In Progress**: The notification is successfully created in Everbridge.

</td><td>

**Active**: A notification is created and is active.An incident and a notification for the incident are created. The notification remains active for the duration set in Everbridge.

</td></tr><tr><td>

**Stopped**

</td><td>

**Stopped**: Notification is stopped from being sent.

</td></tr><tr><td>

**Sent**

</td><td>

**Sent**: After the set duration has elapsed, the state moves to Sent.

</td></tr><tr><td>

**Completed**: The notification is sent.

</td><td>

**Completed**: The state moves to Completed.

</td></tr></tbody>
</table>**Parent Topic:**[Sending notifications with Everbridge](../concept/ebn-collective-tasks.md)

