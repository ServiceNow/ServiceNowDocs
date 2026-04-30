---
title: Address change workflow
description: Learn how agents, using the Address change workflow, resolve service requests for a change in customer's address. The workflow applies to both business and personal CLO service requests.
locale: en-US
release: zurich
product: Financial Services Customer Lifecycle Operations
classification: financial-services-customer-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workflows, Use, Customer Lifecycle Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Address change workflow

Learn how agents, using the Address change workflow, resolve service requests for a change in customer's address. The workflow applies to both business and personal CLO service requests.

The following diagram shows how the application helps bank agents resolve an address change request.

![Workflow that shows how the address for a customer is updated using the CLO application. For the text description, refer to the workflow steps that follow.](../image/fso-address-change-workflow.png "Address change workflow example")

The CLO admin can review and customize this predefined flow based on your organization's business needs.

The following workflow routes the case and tasks for changing a customer's address to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **As a CLO contributor or customer**

    A CLO contributor, such as a relationship manager, submits a request for an address change on behalf of a customer.

    A customer \(consumer or contact\) can also directly submit a request from the Customer Service Portal, Consumer Service Portal, or another self-service portal.

    **Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    A case is created based on the request type.

-   **As a CLO contributor**

    1.  In the Initiate stage of the case playbook, the contributor enters the address change details as provided by the customer.
    2.  The contributor collects the necessary documentation from the customer and submits the application for fulfillment.
    A workflow generates further tasks and the assignment rules route the associated tasks to the appropriate back-office teams.

-   **As back-office agents**
    1.  The document agent works on the document task to review and verify the collected documentation. If the documents are legitimate, the agent marks the task as complete.
    2.  The KYC agent performs the due diligence. If the customer meets the KYC standards of the financial institution, the agent marks the KYC task as complete.
    3.  A CLO authorizer \(CLO agent\) reviews the case details and approves the CLO task to authorize the request.
    4.  When all prior tasks are complete, a CLO agent updates the customer's address in the core banking system, and closes the fulfillment CLO task.

The case is complete and the state and stage of the case are set to Closed Complete.

