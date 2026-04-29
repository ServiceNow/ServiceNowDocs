---
title: Loan Rollover workflow
description: Learn how bank agents, using the Loan Rollover workflow, resolve a loan service request for renewal or rollover of an outstanding loan. The workflow applies to business loans only.
locale: en-US
release: australia
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Loan Operations workflows, Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Loan Rollover workflow

Learn how bank agents, using the Loan Rollover workflow, resolve a loan service request for renewal or rollover of an outstanding loan. The workflow applies to business loans only.

The following diagram shows how the application helps bank agents to resolve a Loan Rollover service request.

![Workflow that shows how bank employees successfully roll over a loan.](../image/loan-rollover-workflow.png "Loan Rollover workflow")

The following workflow routes the case and tasks for a Loan Rollover service request to agents in different departments. The agents log in to Workspace to work on the tasks in their queue.

-   **As a loan contributor, requester, or customer**

    A loan contributor or a requester submits a Loan Rollover service request on behalf of a customer.

    A customer \(account or contact\) can directly submit a request through the Customer Service Portal or another self-service portal.

    A case is initiated based on the request type.

-   **As back-office agents**

    After the case is initiated and an agent updates the case details, a workflow is triggered automatically. The assignment rules route the associated tasks to the appropriate back-office teams.

    1.  A loan agent reviews the case details and adds additional details such as the fee and rollover details.

        The document processor service determines the documents that must be verified for the request. The workflow generates an inbound document verification task for the document agent.

    2.  A document agent works on the inbound document verification task to verify each document that is listed in the task. If required, this agent can request for a deferment of a specific document.

        The workflow generates a credit task for the credit agent.

    3.  A credit agent works on the credit task to review the credit for the customer and approves the request.

        The workflow generates a loan authorization task for the loan agent.

    4.  A loan authorizer \(loan agent\) reviews the case details and approves it.
    5.  A loan agent works on the loan update task and updates the loan account in the banking system.

        If the bank has enabled an integration, the loan account could also get automatically updated in the core system.


After the case is complete, its state and stage are set to Closed Complete and the work notes are updated. A customer can view the status of the case from the Customer Service Portal or another self-service portal.

