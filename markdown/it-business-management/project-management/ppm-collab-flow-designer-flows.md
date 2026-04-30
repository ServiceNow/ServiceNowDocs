---
title: Flows designed to synchronize projects with your collaboration tool
description: Understand the flows designed for the PPM Collaboration application so that you can edit the configurations as required.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Collaborate with your project teams using PPM Collaboration application, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Flows designed to synchronize projects with your collaboration tool

Understand the flows designed for the PPM Collaboration application so that you can edit the configurations as required.

<table id="table_sjq_mnz_kmb"><thead><tr><th>

Slack Flow \[Name\]

</th><th>

Microsoft Teams Flow \[Name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action Slack\[action\_slack\]

</td><td>

Action Teams\[action\_teams\]

</td><td>

Posts a message to the project channel or team whenever an Action is created with priority **1-Critical** or **2-High** or if the priority of an existing Action is updated to **1-Critical** or **2-High**.

</td></tr><tr><td>

Add Assigned Users To Channel\[add\_assigned\_users\_to\_channel\]

</td><td>

Add Assigned Users To MS Group\[add\_assigned\_users\_to\_ms\_group\]

</td><td>

Handles adding the users in the **Assigned to** or **Additional Assignee list** fields of the project tasks to the project channel or team.

</td></tr><tr><td>

Archive Project Channel\[archive\_project\_channel\]

</td><td>

Archive MS Group\[archive\_group\]

</td><td>

Handles archival of the project channel or team based on the count of number of days from which the project is moved to a closed state. This flow is set to run daily at 08:00 AM.

</td></tr><tr><td>

Change Request Slack\[cr\_updated\_slack\]

</td><td>

Change Request Teams\[change\_request\_teams\]

</td><td>

Posts a message to the project channel or team whenever a Change request with priority **1-Critical** or **2-High** is created or if the priority of an existing Change request record is updated to **1-Critical** or **2-High**.

</td></tr><tr><td>

Daily Project Status Slack\[daily\_project\_status\]

</td><td>

Daily Project Status Teams\[daily\_project\_status\_teams\]

</td><td>

Triggers a message about the overall status of the project to the project channel or team everyday at 08:00 AM.

</td></tr><tr><td>

Decision Slack\[decision\_updated\_slack\]

</td><td>

Decision Teams\[decision\_teams\]

</td><td>

Posts a message to the project channel or team whenever a Decision with priority **1-Critical** or **2-High** is created or if the priority of an existing Decision is updated to **1-Critical** or **2-High**.

</td></tr><tr><td>

Issue Slack\[issue\_updated\_slack\]

</td><td>

Issue Teams\[issue\_teams\]

</td><td>

Posts a message to the project channel or team whenever an Issue with priority **1-Critical** or **2-High** is created or if the priority of an existing Issue is updated to **1-Critical** or **2-High**.

</td></tr><tr><td>

Milestone/KeyMilestone Slack\[milestonekeymilestone\]

</td><td>

Milestone/KeyMilestone Teams\[milestonekeymilestone\_teams\]

</td><td>

Posts a message to the project channel or team whenever a Milestone or a Key Milestone task is moved to the closed state.

</td></tr><tr><td>

Project Manager Changes Slack\[project\_manager\_changes\]

</td><td>

Project Manager Changes MS Teams\[project\_manager\_changes\_ms\_teams\]

</td><td>

Handles adding the new project manager as a member to the project channel or team. This flow also checks if the user who was the old project manager is assigned to any project tasks and if not assigned to any task, removes the user from the channel.

</td></tr><tr><td>

Project Status Slack\[project\_status\_slack\]

</td><td>

Project Status Teams\[project\_status\_teams\]

</td><td>

Posts a message to the project channel or team in the following three scenarios: -   **State** field is updated to Closed Complete, Closed Incomplete, or Close Skipped states
-   **Status** fields is updated
-   Project manager changes for this project

</td></tr><tr><td>

Risk Flow Slack\[risk\_created\_slack\]

</td><td>

Risk Flow Teams\[risk\_created\_teams\]

</td><td>

Posts a message to the project channel or team whenever a Risk with probability **High** or **Absolute** is created or if the probability of an existing risk is updated to **High** or **Absolute**.

</td></tr></tbody>
</table>All the flows, except the subflows, are inactive by default. Enable the collaboration between PPM and Slack or Microsoft Teams for a specific action by activating these flows. You can view all these flows by navigating to **Flow Designer** &gt; **Designer** and filtering the flows by the PPM collaboration application. For more information, see [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

If you want to update the configuration for any of these flows, you can edit them. For example, if you want to update the time of daily status update from 8:00 AM to 9:00 AM, you can edit the Daily Project Status Slack \[daily\_project\_status\] or Daily Project Status Teams \[daily\_project\_status\_teams\] flow. For more information, see [Edit a flow](https://www.servicenow.com/docs/access?context=flow-edit&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

**Parent Topic:**[Using Project Management](../../project-management/concept/using-project-management.md)

**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

[Flows](https://www.servicenow.com/docs/access?context=flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

