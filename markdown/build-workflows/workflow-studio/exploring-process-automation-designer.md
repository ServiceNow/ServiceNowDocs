---
title: Playbook builder
description: Playbooks is a component in Workflow Studio. Workflow Studio gives you a streamlined way to author, configure, and monitor playbooks, flows, subflows, actions, and decision tables in one place.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Playbook, Playbooks, Workflow Studio, Build workflows]
---

# Playbook builder

Playbooks is a component in Workflow Studio. Workflow Studio gives you a streamlined way to author, configure, and monitor playbooks, flows, subflows, actions, and decision tables in one place.

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
    -   Also in the **More actions** menu, access the properties of your playbook. You can add or edit the name or description for your playbook, enable playbooks to restart, and edit the behavior of your trigger.
-   **Design space**

    Build your Playbook in either Diagram or Board view. You can perform most of the same functions in either view.

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

For more information on creating a playbook, see [Building your first playbook](getting-started-processes.md).

## Playbook builder components

Playbooks in Workflow Studio consists of these components:

-   **Playbooks**

    A playbook is where a playbook owner configures and organizes multiple instances of Workflow Studio content into a coherent business process. A playbook consists of a trigger and a sequence of stages, which are made up of a sequence of activities.

-   **Trigger definitions**

    A trigger definition specifies the conditions that must be met to run a playbook. A user with the admin, playbook.admin, or pd\_trigger\_author role typically creates and configures a trigger definition that playbook authors can use as a template. A trigger definition specifies the record operation and table conditions that must be met to start running a playbook. A playbook owner typically selects a trigger template when creating a playbook.

-   **Trigger instances**

    A trigger instance is produced when you select a trigger template. The trigger instance stores the conditions that a record must meet to start running the playbook.

-   **Stages**

    A stage is a logical grouping of activities in a playbook. A playbook owner creates a stage to group activities and specify the start rule for when the stage should start running. A stage in your overall business process.

-   **Activity definitions**

    An activity definition maps [subflow](../../workflow-studio/reference/exploring-subflows.md) and [action](../../workflow-studio/concept/exploring-actions.md) inputs and outputs to an activity instance. An activity definition contains:

    -   The automation plan to map the triggering input record data to action or subflow inputs
    -   The activity experience to map action or subflow outputs to a user-facing view of the playbook
    A user with the admin, playbook.admin, or pd\_content\_author roles typically specifies the automation plan and activity experience when creating an activity definition.

-   **Activity instances**

    An activity instance is produced when you add an activity to a playbook. The activity instance stores the automation plan data mappings from the activity definition. You can change these data mappings when the default values do not fit your playbook. The playbook can specify the start rules for when the activity should start running.

-   **Start rules**

    A start rule specifies when a stage or an activity starts running. A playbook owner can use start rules to specify what parts of a playbook run simultaneously and what parts run serially.


**Parent Topic:**[Exploring Playbook](process-automation-designer.md)

