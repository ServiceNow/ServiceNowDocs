---
title: Request, review, and approve increase coverage request workflows
description: Learn how agents, using the increase coverage workflow, resolve service requests for requesting, reviewing, and approving individual life insurance policy change requests.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Individual Life Servicing, Individual Life Servicing, Life Insurance Servicing, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Request, review, and approve increase coverage request workflows

Learn how agents, using the increase coverage workflow, resolve service requests for requesting, reviewing, and approving individual life insurance policy change requests.

The following diagram shows how the application helps agents resolve an increase coverage request.

![Workflow displaying the Increase coverage process. For the text description, refer to the following workflow routes.](../image/individual-life-servicing-increase-coverage-workflow.png "Individual Life Servicing - Increase coverage workflow example")

The insurance policy admin can review and customize this predefined flow based on the business needs of your organization.

The following workflow routes the case and tasks for increasing coverage for a policy to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **Submitting a request as a policy contributor or processor**

    An insurance policy contributor creates a request on behalf of a customer.

    A customer \(consumer or contact\) can directly submit a request from the Customer Service Portal, Consumer Service Portal, or another self-service portal.

    **Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    A policy service case is created based on the request type, and a task creates to send a request to send to the customer the increase coverage .pdf document for their signature. Once the customer signs the document, and the contributor submits the case.

    **Note:** In the case playbook, the requester or contributor updates the case details in the Initiate and review stage, and submits the change for fulfillment.

    A workflow triggers automatically, and the assignment rules route the associated tasks to the appropriate processor teams.

-   **Reviewing a request and submitting a decision as a processor**
    1.  In the case playbook, the processor reviews the policy change request and determines the new premium amount. The processor determines if underwriting is required.
        -   If the processor approves the request, a quote for the requested increase coverage change is sent to the customer or contributor.
        -   If the processor is not sure about whether to approve the requested change, a task is created to advance the case to an underwriter.
        -   If the processor rejects the request, the case becomes closed.
    2.  If the customer approves the quote, the processor updates the policy record, sends updated policy documents to the customer, and closes the increase coverage task in the playbook.
-   **Approving or rejecting a case as an underwriter**

    When a processor is not sure about whether to approve the requested change and a created task advances the case to the underwriter, the underwriter reviews the case details, may request a medical exam for the customer, or approves or rejects the case. If the underwriter approves the case to authorize the increase coverage change request, an updated premium quote for is sent to the customer or contributor.

-   **Accepting or rejecting a quote as a customer**

    After a contributor or processor updates and sends the customer the increase coverage document with the changes for the customer's signature, the customer reviews the request details and signs the document. After the processor or underwriter approves the increase coverage request, the customer is sent an adjusted premium quote and can accept or reject the quote.


The case is complete, and the state and stage of the case are set to Closed Complete.

