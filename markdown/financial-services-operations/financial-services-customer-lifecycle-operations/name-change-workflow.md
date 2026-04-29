---
title: Name change of customer workflow
description: Learn how agents, using the Name change workflow, resolve service requests for a change in customer's name. The workflow applies to Client Lifecycle service requests.
locale: en-US
release: australia
product: Financial Services Customer Lifecycle Operations
classification: financial-services-customer-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflows, Use, Customer Lifecycle Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Name change of customer workflow

Learn how agents, using the Name change workflow, resolve service requests for a change in customer's name. The workflow applies to Client Lifecycle service requests.

The following diagram shows how the application helps bank agents resolve a name change request.

![Workflow that shows how name change request is completed using the CLO application. For the text description, refer to the workflow steps that follow.](../image/fso-name-change-workflow.png "Name change workflow example")

The CLO admin can review and customize this predefined flow based on your organization's business needs.

The following workflow routes the case and tasks for changing a customer's name to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **As a customer**

    A customer contacts the financial institution and requests a name change in their financial account.

-   **As a CLO contributor**

    1.  A CLO contributor, such as a relationship manager, submits a request for a name change on behalf of a customer.

        A case is created based on the request type.

    2.  In the Initiate stage of the case playbook, the contributor enters the name change details as provided by the customer, collects the necessary documentation from the customer, and submits the application for fulfillment.
    A workflow generates further tasks and the assignment rules route the associated tasks to the appropriate back-office teams.

-   **As back-office agents**
    1.  The document agent works on the document task to review and verify the collected documentation. If the documents are legitimate, the agent marks the task as complete.
    2.  The KYC agent performs the due diligence. If the customer meets the KYC standards of the financial institution, the agent marks the KYC task as complete.
    3.  A CLO authorizer \(CLO agent\) reviews the case details and approves the CLO task to authorize the request.
    4.  When all prior tasks are complete, a CLO agent updates the customer's name in the core banking system, and closes the fulfillment CLO task.

The case is complete and the state and stage of the case are set to Closed Complete.

