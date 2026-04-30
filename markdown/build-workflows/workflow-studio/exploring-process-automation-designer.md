---
title: Playbook builder
description: Playbooks are a component in Workflow Studio. Workflow Studio gives you a streamlined way to author, configure, and monitor playbooks, flows, subflows, actions, and decision tables in one place.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Playbooks, Explore, Workflow Studio, Build workflows]
---

# Playbook builder

Playbooks are a component in Workflow Studio. Workflow Studio gives you a streamlined way to author, configure, and monitor playbooks, flows, subflows, actions, and decision tables in one place.

## Workflow Studio landing page

You can view the Workflow Studio landing page by navigating to **Process Automation** &gt; **Workflow Studio**. The landing page opens to Playbooks by default, but you can easily navigate to flows, subflows, actions, and decision tables. For more information on Workflow Studio, see [Workflow Studio](../../workflow-studio/reference/workflow-studio.md).

## Playbooks builder

The builder for Playbooks consists of the main header, design space, and side panel.

-   **Main header**

    The main header displays information about the playbook that you're currently designing. In the main header, you can:

    -   See the status and activation state of your playbook.
    -   Toggle between Diagram and Board view.
    -   Undo or redo your actions.
    -   See and navigate to your errors via the error tray.
    -   Turn [Optional activities](optional-activities.md#) on or off.
    -   Test and activate your playbook so that it runs as expected when triggered. You can also preview the Playbook Experience during testing. For more information, see [Playbook statuses and activation states](../reference/process-status-activation-state.md).
    -   In the **More actions** menu, you can also deactivate or duplicate your playbook.
    -   Also in the **More actions** menu, access the properties of your playbook. You can add or edit the name or description for your playbook, enable playbooks to restart, and edit the behavior of your trigger. For more information, see [Process definition properties](process-definitions.md#process-definition-properties).
-   **Design space**

    Build your playbooks in either Diagram or Board view. You can perform most of the same functions in either view.

    **Note:** Decision activities are not available in Board view, and Optional activities are not available in Diagram view.

    Organize activities into stages to design your playbook.

    -   An activity represents one step within your overall business process. An activity can automate operations on the ServiceNow AI Platform, such as creating or updating records, displaying record information, and running automated actions in the background.
    -   Organize a set of activities into stages within your business process.
    For more information, see [Stages and activities](process-automation-designer-lanes-activities.md).

-   **Side panel**

    The side panel lets you configure your activities, and stages. In the side panel, you can:

    -   Add or edit the name and description for your stage or activity.
    -   Define the start rule for your stage or activity.
    -   Define what your activity or stage does when restarted.
    -   Add or edit the inputs for your activity.
    -   Define additional properties for how your activity renders during runtime.
    -   Define if and how an AI agent performs the activity.

For more information on creating a playbook, see [Getting started with Playbooks](getting-started-processes.md).

**Parent Topic:**[Exploring playbooks](process-automation-designer.md)

