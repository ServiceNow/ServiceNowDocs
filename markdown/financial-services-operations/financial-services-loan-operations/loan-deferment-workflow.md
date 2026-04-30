---
title: Loan Deferment workflow
description: Learn how bank agents, using the Loan Deferment workflow, resolve a loan service request for a temporary postponement of a scheduled loan repayment. The workflow applies to both business and personal loan service requests.
locale: en-US
release: zurich
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Loan Operations workflows, Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Loan Deferment workflow

Learn how bank agents, using the Loan Deferment workflow, resolve a loan service request for a temporary postponement of a scheduled loan repayment. The workflow applies to both business and personal loan service requests.

With loan deferment, the customer is not expected to pay any amount for an agreed duration. In addition, the bank may consider waiving the interest during the deferment period.

Forbearance is also a temporary postponement of scheduled loan repayments where the customer is not expected to pay any amount for an agreed duration. In this case, the bank accrues the interest on the outstanding amount and collects it when the regular repayments start on the loan.

**Note:** Banks use Deferment and Forbearance interchangeably on a case-to-case basis.

The following diagram shows how the application helps bank agents resolve a Loan Deferment service request.

![Workflow that shows how a loan service request for deferment is resolved using the Loan Operations application.](../image/loan-deferment-workflow.png "Loan Deferment workflow")

The following workflow routes the case and tasks for a Loan Deferment service request to agents in different departments. The agents log in to Workspace to work on the tasks in their queue. For Loan Deferment workflow for personal loan operations, agents can also use the case playbook that guides them through the steps that are needed to resolve the case.

-   **As a loan contributor, requester, or customer**

    A loan contributor or a requester submits a Loan Deferment loan service request on behalf of a customer.

    A customer \(consumer or contact\) can directly submit a request from the Customer Service Portal, Consumer Service Portal, or another self-service portal.

    **Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    A case is initiated based on the request type.

-   **As back-office agents**

    After the case is initiated and an agent updates the case details, a workflow is triggered automatically. The assignment rules route the associated tasks to the appropriate back-office teams.

    1.  A loan agent reviews the case details and adds additional details, such as the fee.

        The document processor service determines the documents that must be verified for the request. The workflow generates an inbound document verification task for the document agent.

    2.  A document agent works on the inbound document verification task to verify each document that is listed in the task. If required, they can request a deferment of a specific document.

        The workflow generates a credit assessment task for the credit agent.

    3.  A credit agent works on the credit task to review the credit for the customer and approve the request.

        The workflow generates a loan authorization task for the loan agent.

    4.  A loan authorizer \(loan agent\) reviews the case details and approves it.
    5.  A loan agent works on the loan update task and updates the loan account in the banking system.

        If the bank has enabled an integration, the loan account could also get automatically updated in the core system.


After the case is complete, its state and the stage are set to Closed Complete and the work notes are updated. A customer can view the status of the case from the Customer or Consumer Service Portal or another self-service portal.

