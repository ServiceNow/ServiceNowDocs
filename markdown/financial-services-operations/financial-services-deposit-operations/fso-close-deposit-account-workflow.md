---
title: Close deposit account workflow
description: Learn how agents, using the Close deposit account workflow, resolve service requests for closing a checking or saving deposit account. The workflows apply to both business and personal deposit service requests.
locale: en-US
release: xanadu
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Financial Services Deposit Operations workflows, Using Financial Services Deposit Operations, Financial Services Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Close deposit account workflow

Learn how agents, using the Close deposit account workflow, resolve service requests for closing a checking or saving deposit account. The workflows apply to both business and personal deposit service requests.

The following diagram shows how the application helps bank agents resolve a deposit request for an account closure.

![Workflow showing how the closure of a deposit account is completed using the deposit operations application. For the image description, see the text that follows.](../image/close-deposit-account-workflow.png "Close deposit account workflow example")

The deposit admin can review and customize this predefined flow based on the business needs of your organization.

The following workflow routes the case and tasks for closing a deposit account to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **As a deposit contributor, requester, or customer**

    A deposit contributor or a requester submits a request on behalf of a customer.

    A customer \(consumer or contact\) can directly submit a request from the Customer Service Portal, Consumer Service Portal, or another self-service portal.

    **Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    A case is created based on the request type.

-   **As a deposit contributor**

    In the case playbook, the contributor updates the account closure details in the Initiate and review stage, collects the necessary documentation from the customer, and submits the application for fulfillment.

    A workflow is triggered automatically and the assignment rules route the associated tasks to the appropriate back-office teams.

-   **As back-office agents**
    1.  The document agent works on the document task to review and verify the collected documentation. If the documents are legitimate, the agent marks the task as complete.

        The workflow generates fulfillment tasks for a deposit agent to work on them.

    2.  In the case playbook, a deposit agent works on the deposit task and delinks the deposit account from other financial accounts in the core banking system.
    3.  When all prior tasks are completed, the deposit agent updates the deposit account in the core banking system and closes the update deposit task in the playbook.

The case is complete and the state and stage of the case are set to Closed Complete.

**Parent Topic:**[Financial Services Deposit Operations workflows](deposit-operations-workflows.md)

