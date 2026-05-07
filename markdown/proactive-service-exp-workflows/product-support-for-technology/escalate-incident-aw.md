---
title: Escalate an incident in Proactive Service Experience Workflows
description: Escalate an incident to continue the investigation and diagnosis of that incident. By escalating an incident, you can ask for help from a more-experienced resource so that the issue is resolved more quickly.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [About escalating incidents, Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# Escalate an incident in Proactive Service Experience Workflows

Escalate an incident to continue the investigation and diagnosis of that incident. By escalating an incident, you can ask for help from a more-experienced resource so that the issue is resolved more quickly.

## Before you begin

This task assumes that you have been working on an incident and you must escalate it to the next escalation group.

**Note:** Be sure that the administrator has assigned this role to the escalation groups. For information about how administrators assign roles, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Role required: sn\_ind\_tsm\_core.noc\_agent

## Procedure

1.  In the Service Operations Workspace, navigate to **List** &gt; **Incidents** &gt; **Open** and select an incident.

2.  On the incident record form, from the drop-down list at the top-right corner, select **Escalate**.

3.  In the Capture notes for the escalation pop-up window, enter a descriptive note and select **Escalate**.

    This action triggers the subflow for the next level of escalation group, and the Assignment Group automatically changes to the next escalation group.


## Result

-   The state of the incident task for the previous engineer is set to Closed Complete and the work note is logged.
-   An incident task is created for the newly assigned user with the state set to Work in Progress.
-   A work note in the activity stream provides instructions for the engineer at this level of escalation.
-   The incident Stage is updated with the next escalation level.
-   The Assignment Group is updated according to the escalation level.

**Parent Topic:**[About escalating incidents](../concept/psew-escalate-incident.md)

