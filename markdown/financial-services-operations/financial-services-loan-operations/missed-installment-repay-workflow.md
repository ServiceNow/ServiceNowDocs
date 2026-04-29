---
title: Missed Installment Repayment workflow
description: Learn how bank agents, using the Missed Installment Repayment workflow, proactively contact a loan customer for a missed installment of an outstanding loan and decide on an action plan. The workflow applies to both business and personal loans.
locale: en-US
release: australia
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Loan Operations workflows, Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Missed Installment Repayment workflow

Learn how bank agents, using the Missed Installment Repayment workflow, proactively contact a loan customer for a missed installment of an outstanding loan and decide on an action plan. The workflow applies to both business and personal loans.

The following diagram shows how the application helps bank agents handle a missed installment payment by a borrower.

![Workflow that shows how a missed repayment is handled using the Loan Operations application.](../image/missed-repayment-workflow.png "Missed Installment Repayment workflow")

The following workflow routes the case and tasks for a Missed Repayment to agents in different departments. The agents log in to Workspace to work on the tasks in their queue.

-   **As a loan agent or via an API**

    If the system observes a default in repayment by a loan borrower, an API in the backend triggers a Missed Installment Repayment loan service case. A loan agent can also create this case.

-   **As back-office agents**

    A loan agent reviews the case details and works with the customer and finalizes the action plan.

    After the case is initiated and a loan agent updates the case details, a workflow is triggered automatically. The assignment rules route the associated tasks to the appropriate back-office teams.

    -   **Initiate a payment**
        -   If the customer makes the installment payment, the loan agent initiates the payment and fills in the payment details in the case.

            The workflow automatically generates a loan authorization task for the loan agent.

        -   A loan authorizer \(loan agent\) reviews the case details and approves it.
        -   A loan agent works on the loan update task and updates the loan information in the core banking system.

            Banks can automate this task by enabling an integration with the core baking system.

    -   **Create a remedial service case**

        If the customer is unable to make a partial or full payment, the loan agent creates one of the following service cases to resolve the case:

        -   Loan Forgiveness
        -   Partial Prepayment
        -   Loan Write Off
        -   Loan Deferment
        The new loan service case then handles this loan issue.


After the case is complete, its state and the stage are set to Closed Complete and the work notes are updated.

