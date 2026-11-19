---
title: Restart
description: Give agents and fulfillers the ability to restart a playbook, stage, or activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/restart.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Playbooks in Workflow Studio, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Restart

Give agents and fulfillers the ability to restart a playbook, stage, or activity.

In the Workflow Studio Playbooks builder, Playbooks administrators enable restart for Playbook Experience agents and fulfillers. Playbooks can be restarted from the beginning, or from certain activities or stages during runtime. Playbooks administrators also define what each activity and stage does when an agent restarts.

## Workflow Studio

In Workflow Studio, Playbooks admins [enable restart for playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/enable-define-restart.md), and define the rules for what an activity or stage does during restart:

-   **Skip on restart**: The stage or activity only runs during a playbook's initial run. It does not run on restart.

    **Note:** This setting is helpful if you don't want new tasks or records to be created during a restarted run, because the original execution and resulting record is still relevant.

-   **Run always**: The stage or activity always runs, whether during an initial or restarted run.
-   **Skip on first run**: The stage or activity runs only on restart. It never runs during an initial run.

## Playbook Experience

During runtime, [agents and fulfillers can restart playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/restart-a-playbook.md) from the beginning, or from certain stages or activities.

**Note:** Playbooks in an active state can be restarted:

-   **Queued**
-   **Pending Cancel**
-   **In Progress**

Playbooks in a terminal state cannot be restarted:

-   **Complete**
-   **Error**
-   **Cancelled**

\[Omitted image "restart-playbook-pe.png"\] Alt text: Restarting a playbook during runtime

The opposite is true for activities and stages. Activities and stages must be complete or in an error state before they can be restarted.

\[Omitted image "restart-stage-pe.png"\] Alt text: Restarting a stage during runtime

## Design considerations

Follow these design considerations when configuring restart for your playbook, stages, and activities.

-   **Last stages and activities**

    Avoid setting the last stage or activity of a playbook to **Skip on first run** if there are no parallel stages or activities. If the playbook is restarted before the last stage or activity can run, the last stage or activity never runs.

-   **Stages**

    Avoid grouping all activities that are configured to **Skip on first run** in one \(1\) stage. If you do so, the stage is completely hidden the first time that it runs. The stage must run twice to become visible.


-   **[Enable and Configure Restart for Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/enable-define-restart.md)**  
Configure your playbook so that agents and fulfillers in Playbook Experience can restart a playbook from the beginning, or from a specific stage or activity.

**Parent Topic:**[Playbooks in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-definitions.md)

**Related topics**  


[Create a playbook]()

[Playbook variants]()

[Test a playbook]()

[Duplicate Playbooks]()

[Add translations for playbooks]()

