---
title: Getting started with workflows
description: The graphical Workflow Editor provides a drag-and-drop interface for automating multi-step processes across the platform.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Classic Workflow, Build workflows]
---

# Getting started with workflows

The graphical Workflow Editor provides a drag-and-drop interface for automating multi-step processes across the platform.

## Parts of a workflow

Workflows consist of these parts.

-   **Properties**

    Specify configuration settings such as the workflow name, the table whose records the workflow acts on, and the conditions under which to run it.

-   **Activities**

    Specify the sequence of operations the workflow performs such as generating records, notifying users of pending approvals, or running scripts.

-   **Transitions**

    Specify the conditions under which to run an activity.

-   **Exit conditions**

    Specify the conditions under which to run a transition.

-   **Contexts**

    Store historical runtime information about a specific workflow run in a Workflow Context record.

-   **Versions**

    Store historical design information about a specific workflow in a Workflow version record.


## Workflow life cycle

A workflow starts when a triggering event occurs. Common triggers include a record being inserted into a specific table, or a particular field in a table being set to a specified value. For example, you might create a workflow that runs whenever a user requests approval for an item they want to order from the catalog. You can also schedule workflows to run periodically or call them from scripts such as business rules.

When an activity completes, the workflow transitions to the next activity. An activity might have several different possible transitions to various activities, depending on the outcome of the activity. Continuing the example above, if the user's request is approved, the activity might transition to an activity that notifies someone to order the item. If the user's request is denied, the activity might transition to notifying the user that their request has been denied.

The graphical Workflow Editor represents workflows visually as a type of flowchart. It shows activities as boxes labelled with information about that activity and transitions from one activity to the next as lines connecting the boxes.

At each step in a workflow:

1.  An activity is processed and an action defined by that activity occurs.
2.  At the completion of an action by an activity, the workflow checks the activity's conditions.
3.  For each matching condition, the workflow follows the transition to the next activity.

When the workflow runs out of activities, the workflow is complete. The [Workflow Context](../../workflow-administration/reference/r_AdministeringWorkflowContexts.md) stores the execution history of the activities and transitions run. The [Workflow Version](../../using-workflows/concept/c_WorkflowVersions.md) stores the design history of the activities, transitions, and exit conditions available to run.

## Workflow properties

The workflow properties specify when to run a workflow and what records it acts on. For more information about workflow properties, see [Workflow properties](../../workflow-administration/reference/r_WorkflowProperties.md).

## Workflow activities

A workflow activity contains instructions that are processed by the workflow.

Activities can include running scripts, manipulating records, waiting for a set period of time, or logging an event. Workflow conditions determine whether or not the activity is performed. Activities can be added, removed, or rearranged. Transitions can be drawn between activities.

This is an activity that triggers a notification:

![Sample activity](../image/WfActivity.png "Sample activity")

Workflow runs activities as the user session that starts them. Workflows started from record operations will run activities as the user session that performed the record operation. Workflows started from schedules or restarted from timers run activities as the System user. Workflows started from script calls run activities as the user session that started the script.

For more information on available activities and their behaviors, see [Workflow activities](../../using-workflows/concept/c_WorkflowActivities.md).

## Transitions

After the workflow condition is evaluated, the workflow transition determines which activity is performed when the workflow condition is met.

This is a transition that always leads from the Change Approved script to the **Change Task** activity:

![Sample transition](../image/WfTransition.png "Sample transition")

## Exit conditions

After a workflow activity is performed, the workflow condition is evaluated to determine which transition is activated.

The condition determines behavior based on a change being approved or rejected:

![Sample exit conditions](../image/WfCondition.png "Sample exit conditions")

## Workflow example

During workflow editing or while an unpublished workflow is running, only the person who checked out the workflow can view the changes.

After a workflow is published, it is available to other users. The workflow moves through the process as defined in the Workflow Editor. The entire workflow is represented in one screen. For example, this is the Standard Change workflow:

![Sample change workflow](../image/RoutineChange.png "Sample change workflow")

