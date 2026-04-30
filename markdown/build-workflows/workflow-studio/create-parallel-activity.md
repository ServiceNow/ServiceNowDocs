---
title: Parallel branches
description: Add branches for activities and stages that run in parallel to another branch of activities and stages.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Parallel branches

Add branches for activities and stages that run in parallel to another branch of activities and stages.

## Before you begin

Role required: playbook.admin or pd\_author

## About this task

Parallel activities create branches like decision activities. Unlike decision activities, the activities and stages on a parallel can run on the same conditions as other branches. For example, in this credit card approval playbook:

![Parallel activities and stages in Diagram view](../images/playbook-parallel-example.png "Parallel activities and stages")

In this example, agents verify information or identity at the same time as when they check credit scores. All activities and all stages will run.

## Procedure

1.  In Diagram view, hover on the object that you want to insert a parallel activity next to, and select the **+** icon to add an activity.

    The mini-picker displays.

2.  Select the parallel icon ![Parallel icon in diagram view](../images/diagram-parallel-icon.png) to add a parallel branch.

    A parallel branch is added.


## What to do next

Add and configure the [stage](add-configure-stage.md) or [activity](add-configure-activity.md) that will run at the same time as the other branches of stages or activities.

**Parent Topic:**[Stages and activities](../concept/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](add-configure-stage.md)

[Activity definitions](../concept/activity-definitions.md)

[Add and configure an activity in a playbook](add-configure-activity.md)

[Automation Assets](../concept/automation-assets.md)

[Start with delay input properties](../reference/start-with-delay-properties.md)

[Optional activities](../concept/optional-activities.md#)

[Decision activities](create-a-decision-activity.md)

[Questionnaire activity](../reference/questionnaire-activity.md)

[Add dynamic inputs to an activity](add-dynamic-inputs-to-activity.md)

