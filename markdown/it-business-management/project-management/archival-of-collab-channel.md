---
title: Archiving your project collaboration channel or team
description: Understand how your project Slack channel or Microsoft team is archived when your project is moved to a closed state.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collaborate with your project teams using PPM Collaboration application, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Archiving your project collaboration channel or team

Understand how your project Slack channel or Microsoft team is archived when your project is moved to a closed state.

## Moving the project to a closed state

When the project manager moves the project to Closed Complete, Closed Incomplete, or Closed skipped state, the following actions are triggered:

-   A notification about project closure is sent to the channel or team immediately.
-   The channel or team is archived within 15 days from the day the project is moved to a closed state.

    This duration of 15 days helps the project members to bring any pending communication to closure or share any pending project documentation.

    Project managers can contact their administrator to update this duration of 15 days to a value of their choice.


## Deletion of a project task

When a project task is deleted, the members in the corresponding Slack channel or Microsoft team are not removed automatically. To remove the members on deletion of a project task, you must enable the **Remove Users From Slack/Teams Channel** business rule. This business rule is created on the Project Task table and is not enabled by default. For more information, see Business rules.

## Deletion of the project channel or team

If the channel is deleted in the Slack application, or the team is deleted in the Microsoft Teams application, the PPM Collaboration application does not handle the deletion of the project's reference in the Entity Channel \[sn\_collab\_common\_entity\_channel\] table automatically. So, the project manager cannot see the **Enable Slack Collaboration** or **Enable MS Teams Collaboration** related link on the project form again.

If the project manager wants to create a channel or team again for this project, administrator must manually delete the project's reference from the Entity Channel table. Then, the related link to enable collaboration appears on the project form.

**Parent Topic:**[Using Project Management](../../project-management/concept/using-project-management.md)

**Related topics**  


[Collaborate with your project teams using PPM Collaboration application](ppm-collab-overview.md)

