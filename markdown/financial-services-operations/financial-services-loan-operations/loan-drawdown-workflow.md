---
title: Loan Drawdown workflow
description: Learn how bank agents, using the Loan Drawdown workflow, resolve a loan service request for disbursement of the drawdown amount from a line of credit that has been pre-approved. The workflow applies to business loans only.
locale: en-US
release: yokohama
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Loan Operations workflows, Using Financial Services Loan Operations, Loan Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Loan Drawdown workflow

Learn how bank agents, using the Loan Drawdown workflow, resolve a loan service request for disbursement of the drawdown amount from a line of credit that has been pre-approved. The workflow applies to business loans only.

A drawdown is related to the line of credit facilities that allows the borrower to obtain funds from a credit line during a loan period. A drawdown refers to each amount that the borrower accesses from the line of credit facility.

The following diagram shows how the application helps bank agents resolve a Loan Drawdown service request.

![Workflow that shows how a loan service request for a drawdown is resolved using the Loan Operations application.](../image/loan-drawdown-workflow.png "Loan Drawdown workflow")

The following workflow routes the case and tasks for a Loan Drawdown service request to agents in different departments. The agents log in to Workspace to work on the tasks in their queue.

-   **As a loan contributor, requester, or customer**

    A loan contributor or a requester submits a Loan Drawdown service request on behalf of a customer.

    A customer \(account or contact\) can directly submit a request through the Customer Service Portal or another self-service portal.

    A case is initiated based on the request type.

-   **As back-office agents**

    After the case is initiated and an agent updates the case details, a workflow is triggered automatically. The assignment rules route the associated tasks to the appropriate back-office teams.

    1.  A loan agent reviews the case details and adds additional details, if any.

        The workflow generates a loan authorization task for the loan agent.

    2.  A loan authorizer \(loan agent\) reviews the case details and approves it.

        The workflow creates two tasks: an outbound document verification task and a loan task to disburse the drawdown amount.

        The document processor service determines the documents that must be verified for the request.

    3.  A loan agent works on the loan disbursement task and releases the drawdown amount to the borrower.

After the case is complete, its state and stage are set to Closed Complete and the work notes are updated. A customer can view the status of the case from the Customer Service Portal or another self-service portal.

