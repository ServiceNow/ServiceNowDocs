---
title: Add, modify, and cancel standing order workflows
description: Learn how agents, using the standing order workflows, resolve service requests for adding, modifying, and canceling standing orders to deposit accounts. The workflows apply to both business and personal deposit service requests.
locale: en-US
release: zurich
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Deposit Operations workflows, Use, Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Add, modify, and cancel standing order workflows

Learn how agents, using the standing order workflows, resolve service requests for adding, modifying, and canceling standing orders to deposit accounts. The workflows apply to both business and personal deposit service requests.

The following diagram shows how the application helps bank agents resolve a deposit request for a standing order.

![Workflow that shows how a deposit request for adding a standing order is resolved using the Deposit Operations application. For the text description, refer to the workflow steps that follow.](../image/add-standing-order-workflow.png "Adding standing order workflow example")

The deposit admin can review and customize this predefined flow based on the business needs of your organization.

The following workflow routes the case and tasks for adding a standing order to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **As a deposit contributor, requester, or customer**

    A deposit contributor or a requester submits a request on behalf of a customer.

    A customer \(consumer or contact\) can directly submit a request from the Customer Service Portal, Consumer Service Portal, or another self-service portal.

    **Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    A deposit service case is created based on the request type.

-   **As a deposit contributor**

    In the case playbook, the contributor updates the case details in the Initiate and review stage and submits the application for fulfillment.

    A workflow is triggered automatically and the assignment rules route the associated tasks to the appropriate back-office teams.

-   **As back-office agents**
    1.  In the case playbook, a deposit agent verifies the operating instructions for the standing order. The agent approves and marks the deposit task as complete.
    2.  A deposit authorizer \(deposit agent\) reviews the case details and approves the deposit task to authorize the deposit request.
    3.  When all prior tasks are completed, a deposit agent updates the deposit account in the core banking system and closes the update deposit task in the playbook.

The case is complete and the state and stage of the case are set to Closed Complete.

**Parent Topic:**[Financial Services Deposit Operations workflows](deposit-operations-workflows.md)

