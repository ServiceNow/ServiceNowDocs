---
title: Workflow of risk response task
description: The risk response task workflow is a structured process to manage assessed risks by defining plans of action to either accept, mitigate, avoid, or transfer those risks.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of risk response task

The risk response task workflow is a structured process to manage assessed risks by defining plans of action to either accept, mitigate, avoid, or transfer those risks.

## Exploring the user journey for Risk response task

The states of a risk response task are as follows:

1.  **Draft**: The default state when a risk response task is created.
2.  **Work in progress**: The state when the risk response task owner starts working on it and sends it to the approver for review.
3.  **Awaiting approval**: The state when the approver reviews the risk response task and either approves or rejects it.
4.  **Closed**: The state when the approver approves the risk response task, moving it to the Closed state.

The risk response task workflow consists of the following stages:

-   **Create a risk response task**

    After an assessor identifies the risk response plans, the assessor then creates risk response tasks. The user with the sn\_risk\_advanced.ara\_assessor role can create a risk response task and assigns them to the risk user with the role sn\_risk.user. After creation, the risk response task moves to the Draft state. For more information, see [Create a risk response task in the Risk Workspace](../task/create-risk-response-task-risk-workspace.md).

-   **Create action items**

    The risk assessor can create multiple strategies with various action items for each risk response task. Action items are specific, granular tasks defined within a risk response task to address and manage risks effectively. Action items can be created and defined when the risk response task is in either the Draft state or the Work in progress state. For more information, see [Create an action item in the risk response task](../task/create-action-item-risk-response-task.md).

    Action items have their own independent workflow. For more information, see [Workflow of action item in risk response task](workflow-action-item-risk-response-task.md).

    **Note:** You can create risk response action items for all types of risk response tasks except for Risk acceptance tasks.

-   **Respond to the risk response tasks**

    After the risk response task is assigned, the risk response task owner moves the risk response task to the Work in progress state. In this stage, the risk response task owner defines a plan of action for the risk response task. After defining the plan of action, the task owner can request for approval from the approvers defined in the approval configurator. By default, a single level of approval is enabled for all types of risk response tasks, where the risk owner can approve the tasks. These approvals can be configured based on requirements. After the task owner request for approval, the risk response task moves to the Awaiting approval state.

    **Important:** All action items associated with the risk response task must be closed to move the risk response task from Work in progress to Awaiting approval state.

-   **Approve or reject the risk response task**

    In the Awaiting approval state, the approvers defined in the approval configurator can review the plan of action and either approve or reject the risk response task. The risk response task moves to the Closed state, if the all the approvers approve the task. If any of the approvers reject the task, then the risk response task moves back to the Work in progress state.


**Parent Topic:**[Using the Risk Workspace](../../grc-workspace-risk/concept/using-risk-workspace.md)

