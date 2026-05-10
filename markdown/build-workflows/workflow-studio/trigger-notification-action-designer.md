---
title: Notification step
description: Trigger a notification as a step within an action by selecting a record \(such as an incident, change request, problem, or user record\) to trigger a notification and defining the associated notification.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Notification step

Trigger a notification as a step within an action by selecting a record \(such as an incident, change request, problem, or user record\) to trigger a notification and defining the associated notification.

[Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notifications.md) is a platform feature. Before triggering a notification as an action step in Workflow Studio, ensure that the notification is set up for use in the platform.

-   When you [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md), set the **Send when** field in the **When to send** tab of the Notification form to Triggered.
-   Verify that your users have an active primary email channel and that all their notifications are active.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

<table id="table_lx2_tkf_y1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record

</td><td>

Drag-and-drop an input record or a record from a previous step. This is the record that will trigger a notification. **Note:** Some notifications are not associated with a specific record or table, such as the **Passwords Require Updating** notification. If configuring such a notification, leave this field blank.

</td></tr><tr><td>

Table name

</td><td>

Read-only. Set to the table of the triggering record.

</td></tr><tr><td>

Notification

</td><td>

Select the notification to be triggered. The notifications that can be selected are associated with the table of the specified record. If no record was selected, you can select a notification that does not have an associated record or table. To create notifications, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md)

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


## Example

![Example Notification step in an action.](../images/notification-step-example.png)

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

