---
title: Failed standing order workflow
description: Learn how bank agents, using the failed standing order workflow, proactively contact a customer for a failed standing order for their deposit account and decide on an action plan. The workflow applies to both business and personal deposit accounts.
locale: en-US
release: australia
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Deposit Operations workflows, Use, Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Failed standing order workflow

Learn how bank agents, using the failed standing order workflow, proactively contact a customer for a failed standing order for their deposit account and decide on an action plan. The workflow applies to both business and personal deposit accounts.

The following diagram shows how the application helps bank agents handle a failed standing order for a deposit account.

![Workflow that shows how a failed standing order is handled using the Deposit Operations application. For the text description, refer to the workflow steps that follow.](../image/failed-standing-order-workflow.png "Failed standing order workflow example")

The deposit admin can review and customize this predefined flow based on the business needs of your organization.

The following workflow routes the case and tasks for a failed standing order to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **As a deposit agent or via an API**

    If the system observes a failure in the execution of a standing order from a deposit account, an API in the backend triggers a Failed standing order deposit service case. A deposit agent can also create this case.

-   **As back-office agents**

    -   A deposit agent works with the customer and finalizes the action plan.
    -   In the case playbook, the deposit agent updates the failure reason, selects an appropriate corrective action in the Initiate and review stage, and submits the application for fulfillment.
    The workflow triggers next tasks or a case based on the selected corrective action and the assignment rules route the associated case or tasks to the appropriate back-office teams.

    -   **Retry or waive a standing order occurrence**

        If the corrective action based on the customer's request is to retry or waive off the standing order occurrence, the workflow automatically generates a deposit authorization task for the deposit agent.

        -   A deposit authorizer \(deposit agent\) reviews the case details and approves the deposit task.
        -   A deposit agent retries to execute the standing order for the deposit account in the core banking system and closes the retry deposit task in the playbook.

            **Note:** The Retry deposit task is generated only for the Retry corrective action.

        The case is complete and the state and stage of the case are set to Closed Complete.

    -   **Creating a corrective action service case**

        If the corrective action is to modify or cancel the standing order, the workflow automatically creates one of the following child cases to resolve the case:

        -   Modify standing order
        -   Cancel standing order
        The new child deposit case then handles this issue.

        After the child case is complete, the state and the stage of the parent case \(failed standing order\) are set to Closed Complete.


**Parent Topic:**[Financial Services Deposit Operations workflows](deposit-operations-workflows.md)

