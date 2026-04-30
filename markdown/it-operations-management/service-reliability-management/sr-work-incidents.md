---
title: Working with incidents in SRM
description: Plan ahead of service disruptions and have SRM send notifications and create status when incidents occur. Distractions are minimized and teams stay focused on remediation.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Working with incidents in SRM

Plan ahead of service disruptions and have SRM send notifications and create status when incidents occur. Distractions are minimized and teams stay focused on remediation.

You can manually create incidents within SRM or create an error budget action to do so. See [Manually create an SRM incident](../task/sr-create-incident.md) or [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md) for more information.

-   [Manual creation from an alert](../../service-operations-workspace-itom/task/open-incident.md).
-   [Manual creation from the incident view](../task/sr-create-incident.md).
-   Automatically from Alert automations, if Alert automations are installed.

The **Assigned to** field on an incident specify who should be notified. When a team is selected as a responder, team automations are checked to determine which schedule to use for the notifications.

**Note:**

The **Assigned to** field is cleared when the **Assigned-team** or **Service** field is updated on an incident. Escalation policies for the newly assigned teams run. The field remains cleared until a user on the new team acknowledges an escalation notification.

If the Service is changed and the new Service does not have an assigned team, no changes occur.

When a service is deleted, its integrations, alerts, incidents, and automations are removed. Deleting a service isn't a recoverable action so consider deactivating the service instead.

Responders and above are notified for updates to incidents based on their notification preferences. If you made the update, you won't be notified.

You can resolve incidents by selecting specific incidents or in bulk. See [Resolve an SRM incident](../task/sr-resolve-incident.md), or [Close an SRM incident](../task/sr-close-incident.md) or [Cancel an SRM incident](../task/sr-cancel-incident.md).

**Note:**

Incidents in the **Resolved** state are automatically closed after 3 days.

For more information on the areas and fields available in an incident, see [SRM incidents](../reference/sr-incidents-workspace.md).

[Export list information to a file](../task/sr-export-to-file.md) from the list view.

Respond to an incident in the following ways:

-   [Tag an incident](../task/sr-create-tags.md).
-   [Update the priority of an SRM incident](../task/sr-update-incident-severity.md).
-   [Set the state of the incident](sr-incident-states.md).
-   [Copy an SRM incident](../task/sr-copy-incident.md).
-   [Add a service to an SRM incident](../task/sr-add-incident-service.md).
-   [SRM incidents](../reference/sr-incidents-workspace.md).
-   [Resolve an SRM incident](../task/sr-resolve-incident.md).
-   [Cancel an SRM incident](../task/sr-cancel-incident.md).
-   [Close an SRM incident](../task/sr-close-incident.md).
-   [Reopen an SRM incident](../task/sr-reopen-incident.md).

-   **[Manually create an SRM incident](../task/sr-create-incident.md)**  
Create an incident if you think an issue poses a serious risk and should be taken care of as soon as possible.
-   **[Reassign an SRM incident](../task/sr-reassign-incident-user.md)**  
Reassign an incident to a responder when the incident tasks should be addressed by a particular team member.
-   **[Update the priority of an SRM incident](../task/sr-update-incident-severity.md)**  
If the priority of an incident should be changed, you can manually update it to reflect its new criticality.
-   **[Add a service to an SRM incident](../task/sr-add-incident-service.md)**  
Add a service to an incident to increase the amount of data for the incident.
-   **[Add resolution code and notes to an SRM incident](../task/sr-add-incident-resolution-notes.md)**  
Add a resolution code and notes to an incident when you have resolved the incident.
-   **[Copy an SRM incident](../task/sr-copy-incident.md)**  
Copy an incident, if you have a similar issue.
-   **[Resolve an SRM incident](../task/sr-resolve-incident.md)**  
Resolve an incident, if you need it reviewed, or you think it has already been handled, but aren't ready to close it.
-   **[Cancel an SRM incident](../task/sr-cancel-incident.md)**  
Close an incident, if you think it is not an issue, or if it has already been handled.
-   **[Close an SRM incident](../task/sr-close-incident.md)**  
Close an incident when it’s not an issue or has already been handled.
-   **[Reopen an SRM incident](../task/sr-reopen-incident.md)**  
Reopen a closed incident if you think the issue is not yet resolved.

**Parent Topic:**[Working with SRM reliability tasks](../task/sr-work-reliability-tasks.md)

