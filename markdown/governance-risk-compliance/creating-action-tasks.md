---
title: Creating an action task for the operational vulnerability
description: The Operational vulnerability analysts gather additional information or an evidence on the vulnerability by creating one or more action tasks. An action task can be of an assessment or investigation type.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Creating an action task for the operational vulnerability

The Operational vulnerability analysts gather additional information or an evidence on the vulnerability by creating one or more action tasks. An action task can be of an assessment or investigation type.

The Operational vulnerability analysts assign the assessment or investigation action tasks to appropriate task owners. The task owners then review the tasks, note their observations, finish the assigned work, and inform the task owners to review their work.

Task owners typically perform the following actions:

-   [Manage an assessment-type action task](../task/create-action-task-op-vul.md)
-   [Manage an investigation-type action task](../task/update-state-of-action-task.md)

## Workflow states for an action task

An action task moves through the following workflow states.

|States|Description|
|------|-----------|
|**Draft**|The action task is in the draft stage.|
|**Assigned**|The action task has been assigned to an appropriate user.|
|**Work in progress**|Work on the action task is in progress.|
|**Review**|The action task is in the review stage.|
|**Closed complete**|The action task is in the Closed complete stage.|
|**Closed incomplete**|The action task is in the Closed incomplete stage.|
|**Canceled**|The action task has been canceled.|

## Notifications for the action tasks associated with the vulnerabilities

When an action task \[sn\_grc\_case\_mgmt\_case\_task\] associated with the vulnerability is assigned to the users, they receive email notifications informing them about the task details, upcoming actions, and due dates. Email notifications are sent to the following users:

1.  When the action task is assigned to the task owner, they receive the email notification.
2.  When the action task is assigned to the assignment group, the users in the assignment group receive the email notifications.
3.  When the action task is submitted for a review, the analyst assigned to the operational vulnerability record receives the email notification to review the task.

