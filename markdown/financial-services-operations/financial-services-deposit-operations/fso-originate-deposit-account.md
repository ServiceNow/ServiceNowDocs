---
title: Originate deposit account workflow
description: Learn how agents, using the originate deposit account workflow, resolve service requests for opening a new deposit account. The workflow applies to both business and personal deposit service requests.
locale: en-US
release: zurich
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Deposit Operations workflows, Use, Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Originate deposit account workflow

Learn how agents, using the originate deposit account workflow, resolve service requests for opening a new deposit account. The workflow applies to both business and personal deposit service requests.

The following diagram shows how the application helps bank agents resolve a deposit request for a new deposit account.

![Workflow that shows how origination of a new deposit account is completed using the deposit operations application. For the text description, refer to the workflow steps that follow.](../image/origin-standing-order-workflow.png "Originate deposit account workflow example")

The deposit admin can review and customize this predefined flow based on the business needs of your organization.

The following workflow routes the case and tasks for originating a deposit account to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **As a deposit contributor, requester, or customer**

    A deposit contributor or a requester submits a request for a new deposit account on behalf of a customer.

    A customer \(consumer or contact\) can directly submit a request from the Customer Service Portal, Consumer Service Portal, or another self-service portal.

    **Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    A case is created based on the request type.

-   **As a deposit contributor**

    1.  In the Initiate and review stage of the case playbook, the contributor updates the product details based on the customer requirements. For a business customer, the contributor also adds the operating instructions for the new account.
    2.  The contributor collects the necessary documentation from the customer and submits the application for fulfillment.
    A workflow is triggered automatically and the assignment rules route the associated tasks to the appropriate back-office teams.

-   **As back-office agents**
    1.  The document agent works on the document task to review and verify the collected documentation. If the documents are legitimate, the agent marks the task as complete.

        The workflow generates further tasks for deposit agents to work on them.

    2.  In the case playbook, a deposit agent configures the deposit account with the interest rate information.
    3.  A deposit authorizer \(deposit agent\) reviews the case details and approves the deposit task to authorize the deposit request.
    4.  When all prior tasks are completed, a deposit agent creates and activates the deposit account in the core banking system, sends the account opening kit to the customer, and closes these deposit tasks.

The case is complete and the state and stage of the case are set to Closed Complete.

**Parent Topic:**[Financial Services Deposit Operations workflows](deposit-operations-workflows.md)

