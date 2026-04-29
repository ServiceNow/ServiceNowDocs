---
title: Playbook terminology
description: Use the following list of terms to gain an understanding of playbook structure, tools, and configuration.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Playbook terminology

Use the following list of terms to gain an understanding of playbook structure, tools, and configuration.

A playbook is an end-to-end workflow that includes the steps, strategies, and guidance to lead users through a business process. A playbook:

-   VISUALIZES a workflow in a task-oriented view and guides users through sequences of tasks.
-   INCLUDES a series of steps that a user must complete to achieve a particular goal.
-   PROVIDES guidance for completing those steps.

## Playbook structure

A playbook contains one or more stages, or groups of tasks, and sequences of activities within each stage. A playbook also includes a trigger. The structure of a playbook is created in [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

<table id="table_playbook_structure_terms"><thead><tr><th>

Term

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Trigger

</td><td>

A trigger determines when a playbook starts running. Each trigger has a type and conditions that, when met, start running an activated playbook.The trigger type represent a record operation, such as when a record is created or updated.

Trigger conditions determine when and how a trigger is fired.

[Triggers](https://www.servicenow.com/docs/access?context=create-trigger-definition&version=australia&pubname=australia-build-workflows&ft:locale=en-US) are created in [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Stage

</td><td>

A stage is a sequence of activities in a playbook that are grouped in a logical way. A playbook can contain one or more stages and each stage includes one or more activities for a user to complete. Stages can also include automated activities.[Stages](https://www.servicenow.com/docs/access?context=process-automation-designer-lanes-activities&version=australia&pubname=australia-build-workflows&ft:locale=en-US) are added to a playbook in [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Activity

</td><td>

An activity is one step in the overall business process represented in a playbook. Activities are the tasks, steps, or actions that a user takes to complete a playbook. Activities are grouped in stages and are sequenced in a logical order. Users can complete or skip manual activities. Activities can also be completed automatically.[Activities](https://www.servicenow.com/docs/access?context=process-automation-designer-lanes-activities&version=australia&pubname=australia-build-workflows&ft:locale=en-US) are added to playbook stages in [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td></tr></tbody>
</table>## Playbook UI components

Customer service agents interact with playbooks in CSM Configurable Workspace. The record pages that display playbooks in a workspace are created or customized in [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US). Different components make up the playbook record pages.

<table id="table_a2t_xmt_bcc"><thead><tr><th>

Term

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Playbook picker

</td><td>

A playbook picker can be used to select a playbook in the user interface. A playbook picker is available if there are multiple playbooks on a record.

</td></tr><tr><td>

Stage picker

</td><td>

A stage picker displays the stages in a playbook. It gives the user a complete view of the playbook and where they are within the playbook. A stage picker can be oriented horizontally or vertically and includes icons that indicate the stage status.

</td></tr><tr><td>

Horizontal stage picker

</td><td>

A horizontal stage picker displays the playbook stages horizontally at the top of the record page and highlights the current stage. It displays activities within the current stage in the activity picker.![playbook horizontal stage picker with four stages: Intake, Investigate, Work in progress, Resolve](../image/csm-playbook-horiz-stage-picker.png)

</td></tr><tr><td>

Vertical stage picker

</td><td>

A vertical stage picker displays the playbook stages and activities vertically on the side of the record page. It highlights and expands the current stage to display the activities within that stage.![playbook vertical stage picker with four stages: Intake, Investigate, Work in progress, Resolve](../image/csm-playbook-vert-stage-picker.png)

</td></tr><tr><td>

Activity picker

</td><td>

The activity picker displays the activities in the current stage. It includes indicators that show the activity state.![Activity viewer expanded to show the list of activities for the current stage. The current activity is highlighted.](../image/csm-playbook-activity-picker.png)

</td></tr><tr><td>

Activity viewer

</td><td>

The activity viewer displays the details of the current activity. This is where a user performs the work necessary to complete the current activity.

</td></tr><tr><td>

Activity card

</td><td>

An activity card displays the details of the current activity. Users use the cards to complete the work for each activity.

</td></tr></tbody>
</table>