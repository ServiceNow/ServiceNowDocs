---
title: Use Playbooks
description: Use a playbook to guide a demand through each stage of its life-cycle, from creating the initial brief to final approval and completion. Playbooks provide step-by-step activities within each stage, ensuring that all required information is captured and governance processes are followed.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage demands, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Use Playbooks

Use a playbook to guide a demand through each stage of its life-cycle, from creating the initial brief to final approval and completion. Playbooks provide step-by-step activities within each stage, ensuring that all required information is captured and governance processes are followed.

## Before you begin

-   Role required: it\_demand\_user, it\_demand\_manager
-   As an administrator, ensure that either the default or custom playbooks are activated.

## About this task

A playbook defines the standard stages of a demand \(for example, Initiation, Planning, Execution, Monitoring, and Closure\) and includes activities or action items to complete at each stage.

**Note:** The playbook presents demand information in a guided, stage-based workflow. The same fields and lists are also available in the **Details** page of the demand record. You can update demand information from either location, and changes made in one are reflected in the other.

This task topic follows the demand AI playbook. It’s a standard playbook comprising the following seven stages:

-   Create demand brief
-   Define demand alignment
-   Estimate demand cost and effort
-   AI checkpoint
-   Confirm demand readiness for review
-   Approve and finalize demand
-   Complete demand

![The stages and activities of a demand AI playbook.](../images/demand-playbook.png)

**Note:** The AI checkpoint stage is available if the AI Control Tower plugin is installed and the investment type of the demand is set to artificial intelligence.

Each stage consists of activities, action items, or steps that guide the demand manager in successfully completing the demand. You can view the **Playbook** menu only if the demand matches the trigger condition defined for that playbook.

**Note:** A demand created in Next Experience for Demand Management opens in the playbook page.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Demands**.

2.  Open an existing demand or create a demand.

    For more information on creating demands, refer to [Create a demand](create-demand-from-dw.md).

3.  Use the default playbook or create or customize one.

    -   To use the default playbook:

        1.  Select **Playbooks** from the L-2 \(level 2\) navigation menu.
        2.  Select a stage to view its activities. Each activity displays its status \(In Progress, Pending, or Complete\) and the fields or lists to update.

            **Note:** The default playbook is a stage-gate playbook, that is, a stage is unlocked only when its prior stages are marked as completed or skipped.

        3.  Complete the activities within each stage. For more information, see [Demand default playbook stages and activities](../reference/demand-default-playbook-stages.md).
        4.  For each activity, perform one of the following actions:
            -   Select **Mark Complete** to mark the activity as done and move to the next activity.
            -   Select **Save** to save your progress without completing the activity.
            -   Select **Skip** to bypass the activity and move to the next one.
        **Note:**

        -   An activity becomes read-only when you select **Mark Complete** or **Skip**.
        -   A stage is marked as completed once all activities within it are either completed or skipped.
        -   Use the **Restart** option \(available at both the activity and stage levels\) to revisit or edit completed or skipped activities.
        -   Some stages include an automated task that advances the demand state when all activities in the stage are completed. These automated tasks don’t require manual action.
    -   To create a playbook, define the trigger condition in Workflow Studio. For more information, see Triggers.
    For more information on how to create and use playbooks, see Building Playbooks and Designing Playbook Experience.


**Related topics**  


[bundle-crworkflow.playbook-agents-and-fulfillers]

[bundle-crworkflow.process-automation-designer-reference]

[Create and customize playbooks](playbooks-configuration-for-dmnd-wpc.md)

[Playbooks in Next Experience for Demand Management](../concept/playbooks-in-demand-workspace.md)

[Demand default playbook stages and activities](../reference/demand-default-playbook-stages.md)

