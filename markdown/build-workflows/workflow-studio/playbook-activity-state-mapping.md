---
title: Playbook activity state mapping
description: Use playbook activity state mapping to override the status of a playbook card.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Stages and activities, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Playbook activity state mapping

Use playbook activity state mapping to override the status of a playbook card.

A playbook card's state comes from the Activity State by default. Activity states come from the Sub Flow or Flow Action powering the activity.

Activity Definition authors can specify a records to provide the status shown in playbook cards. This record is referred to as an **Experience Status Record**. It is specified within an Activity Definition's experience properties.

![Tables and records for an activity definition](../../process-automation-designer/images/activity-definition-tables-records.png)

Any record from any table can be used as an Experience Status Record. Default activity definitions use **sys\_flow\_data** records as their Experience Status Record.

![Playbook activity states shown in card view](../image/playbook-activity-card-states.png "Activity States displayed in card view")

## Default Activity States

|Status|Flow State|
|------|----------|
|Pending|Flow has not started|
|Ready|Flow is|
|In Progress|Flow is running|
|Complete|Flow has finished|
|Skipped|Flow was skipped due to conditions|
|Error|Flow encountered an error|
|Canceled|Flow was canceled|

Activity states are used in the following:

-   Declarative Action conditions
-   Activity Override conditions
-   Animations
-   Card visual experience

## Exceptions

Business logic doesn't always align one-to-one with the flow. The following are examples of exceptions:

-   An agent clicks **Skip** on an instructional card. The flow displays as complete, but the business logic is skipped.
-   A flow may never complete if a task is waiting for input from an agent to restart a loop. The associated task is effectively complete in this state.

-   **[Playbook activity state-mapping rules](playbook-activity-state-mapping-rules.md)**  
Map playbook activity states to states from the given experience record.
-   **[Playbook activity state-mapping permissions](playbook-act-state-permissions.md)**  
User permissions must be assigned to allow agents to complete or skip activities in playbook using activity state mapping.

**Parent Topic:**[Stages and activities](../../process-automation-designer/concept/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](../../process-automation-designer/task/add-configure-stage.md)

[Activity definitions](../../process-automation-designer/concept/activity-definitions.md)

[Add and configure an activity in a playbook](../../process-automation-designer/task/add-configure-activity.md)

[Use AI agent as an activity](../../process-automation-designer/task/ai-agent-as-activity.md)

[Automation Assets](../../process-automation-designer/concept/automation-assets.md)

[Start with delay input properties](../../process-automation-designer/reference/start-with-delay-properties.md)

[Optional activities](../../process-automation-designer/concept/optional-activities.md#)

[Decision activities](../../process-automation-designer/task/create-a-decision-activity.md)

[Decision stages](../../process-automation-designer/task/create-decision-stage.md)

[Questionnaire activity](../../process-automation-designer/reference/questionnaire-activity.md)

[Parallel branches](../../process-automation-designer/task/create-parallel-activity.md)

[Add dynamic inputs to an activity](../../process-automation-designer/task/add-dynamic-inputs-to-activity.md)

