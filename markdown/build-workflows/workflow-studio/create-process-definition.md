---
title: Create a playbook
description: Enable playbook owners to configure and organize multiple instances of Workflow Studio content into an automated business process on the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Playbooks in Workflow Studio, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a playbook

Enable playbook owners to configure and organize multiple instances of Workflow Studio content into an automated business process on the ServiceNow AI Platform®.

## Before you begin

-   [Activate playbooks](../concept/activate-process-automation-designer.md#) for your appropriate application.
-   Familiarize yourself with the tables and relationships that your application uses for the playbook that you want to create.
-   Make sure to familiarize yourself with any features that your business uses to automate operations on the ServiceNow AI Platform, such as [flows](../../workflow-studio/concept/exploring-flows.md), [subflows](../../workflow-studio/reference/exploring-subflows.md), and [actions](../../workflow-studio/concept/exploring-actions.md).
-   Learn how to [get started with ServiceNow® Process Automation](../concept/getting-started-process-automation.md).
-   Role required: admin, playbook.admin, or playbook.write.

## About this task

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

    The Workflow Studio landing page appears. Playbooks are shown by default, but you can toggle to flows, subflows, actions, and decisions.

2.  In the upper right corner, click **New** and select **Playbook** from the drop-down menu.

    The Playbooks builder details screen for a new playbook opens in a new tab.

3.  Fill in the following fields.

    |Field|Action|
    |-----|------|
    |**Playbook name**|Enter a unique, user-facing name for your playbook. This name appears to agents and fulfillers during runtime of your playbook.|
    |**Description**|Optionally, enter some descriptive details about your playbook.|
    |**Application**|Choose an application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).|

    The builder displays in **Diagram view** by default, but you can select **Board view** to switch views. Switch between views anytime as you build your playbook.

    ![Diagram and Board view toggle](../images/board-view.png)

4.  [Configure your trigger.](add-configure-trigger.md)

5.  [Add a stage.](add-configure-stage.md)

6.  [Add an activity.](add-configure-activity.md)

7.  Keep adding stages and activities according to your manual playbook.

    For an example of how to design an entire digitized process with Playbooks, see [Design an automated process](design-automated-process.md).

8.  If you don't see the activity you need to add in the activity picker, [create an activity definition](create-activity-definition.md).

9.  [Add a decision activity.](create-a-decision-activity.md)

10. [Add parallel activities.](create-parallel-activity.md)

11. [Add optional activities.](../concept/optional-activities.md#)

12. After you've added all appropriate stages and activities to your playbook, select **Activate** in the header.

    Activating your playbook publishes it so that it runs when triggered.

    **Note:** If you change your playbook after activating it, the system saves your changes but deactivates your playbook. You must click **Activate** again to publish any new changes to your playbook. For more information, see [Playbook statuses and activation states](../reference/process-status-activation-state.md).


## Result

When your playbook's trigger conditions are met, your playbook runs. As a result, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process that renders as a playbook, see [Design an automated process](design-automated-process.md).

## What to do next

Set up the Playbook Experience for your agents and fulfillers.

**Parent Topic:**[Playbooks in Workflow Studio](../concept/process-definitions.md)

**Related topics**  


[Playbook variants](../concept/playbook-variants.md)

[Test a playbook](test-process.md)

[Restart](../concept/restart.md)

[Duplicate Playbooks](duplicate-process.md)

[Add translations for playbooks](add-translations-playbooks.md)

