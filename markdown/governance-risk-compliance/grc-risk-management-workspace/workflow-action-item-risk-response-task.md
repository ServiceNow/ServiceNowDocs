---
title: Workflow of action item in risk response task
description: The action item workflow is a structured process for managing the granular tasks associated with risk response tasks, which are assigned to multiple stakeholders.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of action item in risk response task

The action item workflow is a structured process for managing the granular tasks associated with risk response tasks, which are assigned to multiple stakeholders.

## Exploring the user journey for an Action item

The states of an action item are as follows:

1.  **Draft**: The default state when an action item is created.
2.  **Assigned**: The state when the action item is assigned to a user.
3.  **Work in progress**: The state when the action item owner starts working on it and sends it to the risk response task owner for review.
4.  **Review**: The state when the risk response task owner reviews the action item and either approves or rejects it.
5.  **Closed**: The state when the risk response task owner approves the action item, moving it to the Closed state.

The action item workflow consists of the following stages:

-   **Create action items**

    The risk assessor or risk response task owner can create multiple strategies with various action items for each risk response task. Action items are specific, granular tasks defined within a risk response task to address and manage risks effectively. The risk response task owner defines a plan of action for the action item. Action items can be created when the risk response task is in either the Draft state or the Work in progress state. For more information, see [Create an action item in the risk response task](../task/create-action-item-risk-response-task.md).

    **Note:** You can create risk response action items for all types of risk response tasks except for Risk acceptance tasks.

-   **Respond to the action item**

    The assignee of the risk response action item moves the action item to the Work in progress state. In this stage, the action item owner specifies the action taken in the **Assignee comments** field, along with any other required steps. The action item owner then sends the action item to the risk response task owner for approval. After the action item owner request for approval, the action item moves to the Review state.

-   **Approve or reject the action item**

    In the Review state, the risk response task owner can review the assignee comments and either approve or reject the action item. If the approver approves the action item, it moves to the Closed state. If approver rejects the action item, then the action item moves back to the Work in progress state.

    **Important:** All action items associated with the risk response task must be closed to move the risk response task from Work in progress to Awaiting approval state.


**Parent Topic:**[Using the Risk Workspace](../../grc-workspace-risk/concept/using-risk-workspace.md)

