---
title: Loan Write off workflow
description: Learn how bank agents, using the Loan Write off workflow, handle writing off a portion or full amount of an outstanding loan when the recovery mechanisms fail. The workflow applies to both business and personal loans.
locale: en-US
release: australia
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Loan Operations workflows, Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Loan Write off workflow

Learn how bank agents, using the Loan Write off workflow, handle writing off a portion or full amount of an outstanding loan when the recovery mechanisms fail. The workflow applies to both business and personal loans.

A bank writes off a loan when all means of recovery are exhausted. It is an action taken up by banks to clear their balance sheets.

The following diagram shows how the application helps bank agents work on a loan write-off.

![Workflow that shows how a loan write-off is handled using the Loan Operations application.](../image/loan-write-off-workflow.png "Loan Write off workflow")

The following workflow routes the case and tasks for a loan write-off to agents in different departments. The agents log in to Workspace to work on the tasks in their queue.

-   **As a credit agent or via an API**

    A loan agent creates a Loan Write Off loan service case. An API in the backend can also trigger this loan service case.

-   **As back-office agents**

    After the case is initiated and an agent updates the case details, a workflow is triggered automatically. The assignment rules route the associated tasks to the appropriate back-office teams.

    1.  A loan agent reviews the case details and adds additional details such as outstanding principal and interest amounts.

        The document processor service determines the documents that must be verified for the request. The workflow generates an inbound document verification task for the document agent.

    2.  A document agent works on the inbound document verification task to verify each document that is listed in the task. If required, this agent can request for a deferment of a specific document.

        The workflow generates a loan authorization task for the loan agent.

    3.  A loan authorizer \(loan agent\) reviews the case details and approves it.
    4.  A loan agent works on the loan update task and updates the loan information in the banking system.

        If the bank has enabled an integration, the loan account could also get automatically updated in the core banking system.


After the case is complete, its state and the stage are set to Closed Complete and the work notes are updated. A customer can view the status of the case from the Customer or Consumer Service Portal or another self-service portal.

