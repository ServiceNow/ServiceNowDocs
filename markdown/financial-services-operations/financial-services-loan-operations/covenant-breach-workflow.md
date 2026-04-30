---
title: Covenant Breach workflow
description: Learn how bank agents, using the Covenant Breach workflow, proactively contact a loan customer for a covenant breach and decide on an action plan for the future. The workflow applies to both business and personal loans.
locale: en-US
release: zurich
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Loan Operations workflows, Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Covenant Breach workflow

Learn how bank agents, using the Covenant Breach workflow, proactively contact a loan customer for a covenant breach and decide on an action plan for the future. The workflow applies to both business and personal loans.

## What are covenants

A covenant is a promise by a borrower to a bank to abide by certain conditions through the life of the loan. Covenants are set up by the bank at the time of originating a loan. Monitoring covenants is an ongoing activity for the bank. A covenant helps a bank to identify and mitigate potential risks that are associated with a loan. When a covenant is breached, it is a signal of a potential default by the borrower.

Examples of covenants for business loans could be:

-   Quarterly submissions of financial statements by the borrower
-   Monthly submissions of inventory and stock statement or unpaid invoices

An example of a covenant for personal loans could be a periodic submission of home insurance premium receipts.

The following diagram shows how the application helps bank agents work on a covenant breach for a loan.

![Workflow showing how a covenant breach is handled using the Loan Operations application. For the text description, refer to the workflow steps that follow.](../image/covenant-breach-workflow.png "Covenant Breach workflow")

The following workflow routes the case and tasks for a covenant breach to agents in different departments. The agents log in to Workspace to work on the tasks in their queue.

-   **As a credit agent or via an API**

    If a covenant breach is observed for a loan, an API in the backend triggers a Covenant Breach credit service case. A credit agent can also create this case.

-   **As back-office agents**

    After the case is initiated and a credit agent updates the case details, a workflow is triggered automatically. The assignment rules route the associated tasks to the appropriate back-office teams.

    1.  A credit agent reviews the case details and adds additional details such as the covenant compliance status.

        The document processor service determines the documents that must be verified for the case. The workflow generates an inbound document verification task for the document agent.

    2.  A document agent works on the inbound document verification task to verify each document that is listed in the task. If required, this agent can request for a deferment of a specific document.

        The workflow generates a credit authorization task for the credit agent.

    3.  A credit authorizer \(credit agent\) works on the credit task to review and approve it.

        The workflow generates a covenant update task for the credit agent.

    4.  A credit agent works on this credit task and updates the covenant information in the banking system.

After the case is complete, its state and the stage are set to Closed Complete and the work notes are updated.

