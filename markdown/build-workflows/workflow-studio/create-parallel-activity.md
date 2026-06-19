---
title: Parallel branches
description: Add branches for activities and stages that run in parallel to another branch of activities and stages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/create-parallel-activity.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Parallel branches

Add branches for activities and stages that run in parallel to another branch of activities and stages.

## Before you begin

Role required: playbook.admin or pd\_author

## About this task

Parallel activities create branches like decision activities. Unlike decision activities, the activities and stages on a parallel can run on the same conditions as other branches. For example, in this credit card approval playbook:

\[Omitted image "playbook-parallel-example.png"\] Alt text: Parallel activities and stages in Diagram view

In this example, agents verify information or identity at the same time as when they check credit scores. All activities and all stages will run.

## Procedure

1.  In Diagram view, hover on the object that you want to insert a parallel activity next to, and select the **+** icon to add an activity.

    The mini-picker displays.

2.  Select the parallel icon \[Omitted image "diagram-parallel-icon.png"\] Alt text: Parallel icon in diagram view to add a parallel branch.

    A parallel branch is added.


## What to do next

Add and configure the [stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/add-configure-stage.md) or [activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/add-configure-activity.md) that will run at the same time as the other branches of stages or activities.

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

