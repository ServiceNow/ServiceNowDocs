---
title: Workflow status of the emergency notification
description: The table lists the different states to which the emergency notification proceeds in the Everbridge side. You can track the notification delivery and monitor its status in the workspace until it is successfully delivered to the contacts from the Everbridge side.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an emergency notification and monitor its workflow, Integrating Crisis Management with Everbridge, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Workflow status of the emergency notification

The table lists the different states to which the emergency notification proceeds in the Everbridge side. You can track the notification delivery and monitor its status in the workspace until it is successfully delivered to the contacts from the Everbridge side.

## Status flow of emergency notification

An emergency notification that you create for a crisis event, when sent to Everbridge creates a corresponding incident along with a notification. The short description of the event in the workspace is created as an incident with a notification in Everbridge.

-   **Notification state**

    The emergency notification that is created and sent from ServiceNow Business Continuity Management workspace is tracked in the **Notification state** field.

-   **Communication status**

    The emergency notification that is received in Everbridge and the different stages to which it moves until it is delivered are tracked in the **Communication status** field.


<table id="table_d1h_3gt_rpb"><thead><tr><th>

Notification state

</th><th>

Communication status

</th></tr></thead><tbody><tr><td>

**Draft**: Draft is stored in the workspace.

</td><td>

 

</td></tr><tr><td>

**Attempting to send**: Notification is being sent from the workspace.

</td><td>

 

</td></tr><tr><td>

**Error**: Error in creating the notification in Everbridge.

</td><td>

 

</td></tr><tr><td>

**In Progress**: Notification is successfully created in Everbridge.

</td><td>

**Active**: A notification is created and is active.An incident and a notification for the incident are created. The notification remains active for the duration set in Everbridge.

</td></tr><tr><td>

 

</td><td>

**Sent**: After the set duration has elapsed, the state moves to Sent.

</td></tr><tr><td>

**Completed**: The notification is sent.

</td><td>

 

</td></tr><tr><td>

 

</td><td>

**Stopped**: Notification is stopped from being sent.

</td></tr></tbody>
</table>