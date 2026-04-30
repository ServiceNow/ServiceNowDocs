---
title: Playbook activity stream component
description: The activity stream component displays a list of activities occurring on a case record.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook page templates, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Playbook activity stream component

The activity stream component displays a list of activities occurring on a case record.

The activities in the list can be collapsed or expanded. When collapsed, the agent can quickly scan the list to get an overview of case activities. When expanded, the agent can see detailed information on individual activities.

![The playbook activity stream component lists record activities in a collapsed or expanded format and uses tiles to represent the activity types.](../image/case-playbook-template-activity-stream.png "Playbook activity stream component")

**Note:** The activity stream uses [Modeless dialogs](csm-front-line-case-page-modeless-dialogs.md) for composing comments, work notes, and emails.

## Activity stream Case and Task tabs

The activity stream component includes tabs for tasks and cases. The Task tab appears when an agent is working on a playbook activity whose associated record is a case task.

## Activity stream tiles

The activities in the activity stream are represented by tiles that use icons and colors to indicate the activity type. These activity types include:

-   Comment
-   Work note
-   Attachment
-   Field change
-   Email sent or email received
-   Chat discussion
-   Custom icon

When collapsed, each activity in the list includes:

-   A tile that represents the activity type.
-   The name of the user responsible for the activity.
-   A brief one-line summary of the activity.
-   A badge that indicates if an activity is internal or external.
-   A relative timestamp.
-   An expand button that the agent can use to see a detailed summary of the activity.

When expanded, each activity also includes:

-   A full date and timestamp.
-   An action label that describes the type of activity.
-   For comments and work notes, the full text of the comment or work note.
-   For field updates, the field name and the updated field value.
-   For emails, detailed message information.
-   For attachments, a small preview of the attached file.
-   For chats, a sidebar chat card.

