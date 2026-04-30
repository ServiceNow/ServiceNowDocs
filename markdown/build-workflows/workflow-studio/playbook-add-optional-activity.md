---
title: Add an activity to a playbook
description: Add pre-selected optional activities to a playbook if available.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Running playbooks, Use, Workflow Studio, Build workflows]
---

# Add an activity to a playbook

Add pre-selected optional activities to a playbook if available.

## Before you begin

Role required: agent

## About this task

Add and complete optional playbook activities in a running playbook. This example shows how an optional activity can be added to a playbook. Playbook admins must pre-configure optional activities. You cannot insert an optional activity as the first activity in a stage or between two finished activities. Some optional activities can be added to any stage while others can only be added to a single stage. If optional activities are not configured for a playbook, no optional activities will be available.

## Procedure

1.  Open a playbook in workspace.

2.  Select the action menu icon \(![Playbook action menu icon](../image/playbook-ellipses.png)\).

3.  Select **Add Activity**.

    ![Add Activity button to add optional activities.](../image/playbook-add-activity-button.png)

    **Note:** **Add Activity** will not display if no optional activities available in this stage.

4.  Select **+ Add activity here** in the location you want to add the activity to the playbook.

    ![Add an activity to a playbook by selecting + Add activity here.](../image/playbook-add-activity-here.png)

5.  Select the activity you would like to add to the playbook.

    ![Add activity modal.](../image/playbook-add-activity-select.png)

6.  Select **Done**.

    The selected optional activity appears in your playbook.


## Result

The selected optional activity appears in your playbook.

![Optional activities appear in the location selected.](../image/playbook-add-activity-complete.png)

**Parent Topic:**[Running playbooks](../concept/playbook-agents-and-fulfillers.md)

