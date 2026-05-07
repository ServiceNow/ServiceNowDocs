---
title: Enabling playbook restart
description: Learn how playbook restart during runtime works and how restart rules control the behavior of stages and activities during a restarted run.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Enabling playbook restart

Learn how playbook restart during runtime works and how restart rules control the behavior of stages and activities during a restarted run.

Playbook restart lets agents and fulfillers in Playbook Experience restart a playbook from the beginning, or from a specific stage or activity. Playbooks administrators enable restart in Workflow Studio and define restart rules for each stage and activity.

Restart is automatically enabled for new playbooks. For existing playbooks, an administrator must enable restart manually. Once enabled, restart cannot be disabled.

## Restart rules

When you configure restart for a stage or activity, you define what it does when a playbook is restarted. The following rules are available:

|Rule|Description|
|----|-----------|
|Skip on restart|The stage or activity runs only during the initial run. It does not run when the playbook is restarted. Use this rule when you don't want new tasks or records to be created during a restarted run, because the original execution and its resulting record are still relevant.|
|Run always|The stage or activity runs during both the initial run and any restarted run.|
|Skip on first run|The stage or activity runs only during a restarted run. It never runs during the initial run.|

## Restart states

The state of a playbook, stage, or activity determines whether it can be restarted.

A playbook can only be restarted when it is in an active state. The only active state is In Progress. Playbooks in a terminal state — Complete, Error, or Cancelled — cannot be restarted.

The opposite is true for stages and activities. A stage or activity can only be restarted when it is in a complete or error state.

## Design considerations

Follow these design considerations when configuring restart for your playbook, stages, and activities.

-   **Last stages and activities**

    Avoid setting the last stage or activity of a playbook to **Skip on first run** if there are no parallel stages or activities. If the playbook is restarted before the last stage or activity can run, the last stage or activity never runs.

-   **Stages**

    Avoid grouping all activities that are configured to **Skip on first run** in one \(1\) stage. If you do so, the stage is completely hidden the first time that it runs. The stage must run twice to become visible.


-   **[Configure restart for Playbooks](../task/enable-define-restart.md)**  
Configure restart so that agents and fulfillers in Playbook Experience can restart a playbook from the beginning, or from a specific stage or activity.

**Parent Topic:**[Creating and managing Playbooks](creating-managing-playbooks.md)

**Related topics**  


[Configure restart for Playbooks](../task/enable-define-restart.md)

