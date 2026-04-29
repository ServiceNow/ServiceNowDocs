---
title: Enabling playbook restart
description: Give agents and fulfillers the ability to restart a playbook, stage, or activity.
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

Give agents and fulfillers the ability to restart a playbook, stage, or activity.

In the Workflow Studio Playbooks builder, Playbooks administrators enable restart for Playbook Experience agents and fulfillers. Playbooks can be restarted from the beginning, or from certain activities or stages during runtime. Playbooks administrators also define what each activity and stage does when an agent restarts.

## Workflow Studio

In Workflow Studio, Playbooks admins [enable restart for playbooks](../task/enable-define-restart.md), and define the rules for what an activity or stage does during restart:

-   **Skip on restart**: The stage or activity only runs during a playbook's initial run. It does not run on restart.

    **Note:** This setting is helpful if you don't want new tasks or records to be created during a restarted run, because the original execution and resulting record is still relevant.

-   **Run always**: The stage or activity always runs, whether during an initial or restarted run.
-   **Skip on first run**: The stage or activity runs only on restart. It never runs during an initial run.

## Playbook Experience

During runtime, [agents and fulfillers can restart playbooks](../task/restart-a-playbook.md) from the beginning, or from certain stages or activities.

**Note:** Playbooks in an active state can be restarted:

-   **In Progress**

Playbooks in a terminal state cannot be restarted:

-   **Complete**
-   **Error**
-   **Cancelled**

![Restarting a playbook during runtime](../images/restart-playbook-pe.png)

The opposite is true for activities and stages. Activities and stages must be complete or in an error state before they can be restarted.

![Restarting a stage during runtime](../images/restart-stage-pe.png)

## Design considerations

Follow these design considerations when configuring restart for your playbook, stages, and activities.

-   **Last stages and activities**

    Avoid setting the last stage or activity of a playbook to **Skip on first run** if there are no parallel stages or activities. If the playbook is restarted before the last stage or activity can run, the last stage or activity never runs.

-   **Stages**

    Avoid grouping all activities that are configured to **Skip on first run** in one \(1\) stage. If you do so, the stage is completely hidden the first time that it runs. The stage must run twice to become visible.


-   **[Configure restart for Playbooks](../task/enable-define-restart.md)**  
Configure your playbook so that agents and fulfillers in Playbook Experience can restart a playbook from the beginning, or from a specific stage or activity.

**Parent Topic:**[Creating and managing Playbooks](creating-managing-playbooks.md)

