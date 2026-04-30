---
title: Partial Prepayment loan workflow
description: Learn how bank agents, using the Partial Prepayment loan workflow, resolve a service request for a partial prepayment of an outstanding loan with the bank before its maturity. The workflow applies to both business and personal loan service requests.
locale: en-US
release: xanadu
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Loan Operations workflows, Using Financial Services Loan Operations, Financial Services Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Partial Prepayment loan workflow

Learn how bank agents, using the Partial Prepayment loan workflow, resolve a service request for a partial prepayment of an outstanding loan with the bank before its maturity. The workflow applies to both business and personal loan service requests.

A partial prepayment is directly applied to the outstanding principal component of the loan. The customer is typically given an option to restructure the repayment on the remaining balance in one of the following ways:

-   Continue with the present repayment, which is higher and results in the early closure of the loan
-   Retain the current loan term, which means that the repayment amount gets recomputed and is spread across the pending loan term

The following diagram shows how the application helps bank agents resolve a Partial Prepayment service request.

![Workflow that shows how a loan request for a partial prepayment is resolved using the Loan Operations application.](../image/partial-prepayment-workflow.png "Partial Prepayment loan workflow")

The following workflow routes the case and tasks for a Partial Prepayment service request to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue.

-   **As a loan contributor, requester, or customer**

    A contributor or a requester submits a Partial Prepayment loan service request on behalf of a customer.

    A customer \(consumer or contact\) can directly submit a request from the Customer Service Portal, Consumer Service Portal, or another self-service portal.

    **Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    A case is initiated based on the request type.

-   **As back-office agents**

    After the case is initiated and an agent updates the case details, a workflow is triggered automatically. The assignment rules route the associated tasks to the appropriate back-office teams.

    1.  A loan agent reviews the case details and adds additional details, such as the fee.

        The document processor service determines the documents that must be verified for the request. The workflow automatically generates an inbound document verification task for the document agent.

    2.  A document agent works on the inbound document verification task to verify each document that is listed in the task. If required, this agent can request for a deferment of a specific document.

        The workflow generates a loan authorization task for the loan agent.

    3.  A loan authorizer \(loan agent\) reviews the case details and approves it.
    4.  A loan agent works on the loan update task and updates the loan account in the banking system.

        If the bank has enabled an integration, the loan account could also get automatically updated in the core banking system.


After the case is complete, its state and the stage are set to Closed Complete and the work notes are updated. A customer can view the status of the case from the Customer or Consumer Service Portal or another self-service portal.

