---
title: Request, review, and approve change membership request workflows
description: Learn how agents, using the change member info workflows, resolve service requests for requesting, reviewing, and approving group life insurance member change requests.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Group Life Servicing, Group Life Servicing, Life Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Request, review, and approve change membership request workflows

Learn how agents, using the change member info workflows, resolve service requests for requesting, reviewing, and approving group life insurance member change requests.

The following diagram shows how the application helps agents resolve a change policy membership request.

![Workflow that shows how a change membership request for a policy is resolved using the Group Life Servicing application. For the text description, refer to the workflow steps that follow.](../image/change-membership-workflow.png "Group Life Servicing - Change membership workflow example")

The insurance policy admin can review and customize this predefined flow based on the business needs of your organization.

The following workflow routes the case and tasks for changing membership for a policy to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **Submitting a request as a policy contributor or processor**

    An insurance policy contributor submits a request on behalf of a customer.

    A customer \(consumer or contact\) can directly submit a request from the Customer Service Portal, Consumer Service Portal, or another self-service portal.

    **Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    A policy service case is created based on the request type, and routes to the processor.

    **Note:** In the case playbook, the requester or contributor updates the case details in the Initiate and review stage, and submits the change for fulfillment.

    A workflow triggers automatically, and the assignment rules route the associated tasks to the appropriate processor teams.

-   **Reviewing a request and submitting a decision as a processor**
    1.  In the case playbook, the processor reviews the policy change request and determines if underwriting is required. The processor approves or rejects the request.
        -   If the processor approves the change request, a quote for the requested change is sent to the customer or contributor.
        -   If the processor is not sure about whether to approve the requested change, a task is created to advance the case to an underwriter.
    2.  An underwriter reviews the case details and approves or rejects the case. If they approve the case to authorize the policy change request, a quote for the requested change is sent to the customer or contributor.
    3.  If the customer approves the quote, the processor updates the policy record, sends updated policy documents to the customer, and closes the change membership task in the playbook.
-   **Approving or rejecting a case as an underwriter**

    When a processor is not sure about whether to approve the requested change and a created task advances the case to the underwriter, the underwriter reviews the case details and approves or rejects the case. If the underwriter approves the case to authorize the policy change request, a quote for the requested change is sent to the customer or contributor.

-   **Accepting or rejecting a quote as a customer**

    When the customer receives a quote after acceptance of the requested policy change, they can accept or reject the quote.


The case is complete, and the state and stage of the case are set to Closed Complete.

