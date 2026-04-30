---
title: Working with alerts in SRM
description: Events take the form of alerts under reliability tasks in SRM. From creation to resolution, SRM enables you to manage your alerts through the entire alert life cycle.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Working with alerts in SRM

Events take the form of alerts under reliability tasks in SRM. From creation to resolution, SRM enables you to manage your alerts through the entire alert life cycle.

Alerts are created manually or within SRM using different integrations.

If the Alert automation application has been installed, alerts can be grouped during ingestion and before Alert management automations are run.

The **Assigned to** field on an alert specifies who should be notified. When a team is selected as a responder, team rules are checked to determine which schedule to use for the notifications. An alert can be assigned to multiple teams.

The **Assigned to** field is cleared when the **Assigned-team** or **Service** field is updated on an alert. Escalation policies run on newly assigned teams. The field remains cleared until a user on the new team acknowledges an escalation notification.

**Note:**

If the Service is changed and the new Service does not have an assigned team, no changes occur.

When a Service is deleted, its integrations, alerts, incidents, and automations are removed. This is not a recoverable action so consider deactivating the service instead.

Responders and above are notified for updates to alerts based on their notification preferences.

Selecting the attachments ![Attachments icon.](../image/icon-sr-attachment.png) icon toggles the **Attachments** panel open or closed.

For more information on the areas and fields available in an alert, see [SRM alert workspace](../reference/sr-alerts-workspace.md).

Respond to an alert in the following ways:

-   [Acknowledge an SRM alert](../task/sr-acknowledge-alert.md) that requires attention.
-   [Add work notes to an SRM alert](../task/sr-add-alert-worknotes.md)
-   [Update the severity of one or more SRM alerts](../task/sr-update-alert-severity.md)
-   [Reassign an SRM alert](../task/sr-reassign-alert-user.md)
-   [Manually create SRM tags](../task/sr-create-tags.md)
-   [Close an SRM alert](../task/sr-close-alert.md)

    If there have been no updates, open alerts are automatically closed after 7 days. Closed alerts are automatically deleted after 90 days.

-   [Reopen an SRM alert](../task/sr-reopen-alert.md)

-   **[Manually create an SRM alert](../task/sr-create-alert.md)**  
Create an alert for testing or if you think an issue poses a risk and should be evaluated as soon as possible.
-   **[Acknowledge an SRM alert](../task/sr-acknowledge-alert.md)**  
Place an alert in the Acknowledged state if the alert has issues that must be addressed. You can acknowledge an alert without assigning it to yourself.
-   **[Update the severity of one or more SRM alerts](../task/sr-update-alert-severity.md)**  
If the severity of an alert should be changed, you can manually update it to reflect its new criticality.
-   **[Update the state of one or more SRM alerts](../task/sr-update-alert-state.md)**  
If the state of an alert must be changed, you can manually update it to reflect its new status.
-   **[Add or edit a task on an SRM alert](../task/sr-add-alert-task.md)**  
If an alert has a task, you can manually add it.
-   **[Add or edit a parent on an SRM alert](../task/sr-add-alert-parent.md)**  
If an alert has a parent, you can manually update it to reflect its new criteria.
-   **[Add or edit a knowledge article to an SRM alert](../task/sr-add-alert-kb.md)**  
If an alert has a knowledge article associated with it, you can manually add it.
-   **[Reassign an SRM alert](../task/sr-reassign-alert-user.md)**  
Reassign an alert to a responder when the alert task should be addressed by a particular user.
-   **[Add work notes to an SRM alert](../task/sr-add-alert-worknotes.md)**  
Add work notes to an alert that are visible to all members of the alert team.
-   **[Close an SRM alert](../task/sr-close-alert.md)**  
Close an alert, if you think it is not an issue, or if it has already been handled.
-   **[Reopen an SRM alert](../task/sr-reopen-alert.md)**  
Reopen a closed alert if you think the issue is not yet resolved.
-   **[Promote an SRM alert to an incident](../task/sr-promote-incident-alert.md)**  
Promote an alert to an incident if you think the alert poses a serious issue and must be taken care of as soon as possible.

**Parent Topic:**[Working with SRM reliability tasks](../task/sr-work-reliability-tasks.md)

