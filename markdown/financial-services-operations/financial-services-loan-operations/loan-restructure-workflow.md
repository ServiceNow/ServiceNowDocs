---
title: Loan Restructure Proposal workflow
description: Learn how bank agents, using the Loan Restructure Proposal workflow, contact a loan customer for restructuring an outstanding loan which otherwise could turn into a non-performing loan. The workflow applies to both business and personal loans.
locale: en-US
release: yokohama
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Loan Operations workflows, Using Financial Services Loan Operations, Loan Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Loan Restructure Proposal workflow

Learn how bank agents, using the Loan Restructure Proposal workflow, contact a loan customer for restructuring an outstanding loan which otherwise could turn into a non-performing loan. The workflow applies to both business and personal loans.

A loan restructuring is an action to prevent a loan from being classified as non-performing. Banks modify the terms of the loans by changing the loan term, repayment amount, number of installments, or the rate of interest.

The following diagram shows how the application helps bank agents handle a loan restructure.

![Workflow that shows how a loan restructure is handled using the Loan Operations application.](../image/loan-restructure-workflow.png "Loan Restructure workflow")

The following workflow routes the case and tasks for a Loan Restructure to agents in different departments. The agents log in to Workspace to work on the tasks in their queue.

-   **As a credit agent**
    1.  A credit agent creates a Loan Restructure Proposal credit service case.
    2.  A credit agent works with the customer and finalizes the restructuring terms. The agent adds the additional details, such as the asset classification and restructure details.
        -   A workflow is triggered automatically and the assignment rules route the associated case and tasks to the appropriate back-office teams.
        -   The document processor service determines the documents that must be verified for the case. The workflow generates an inbound document verification task for the document agent.
    3.  A document agent works on the inbound document verification task to verify each document that is listed in the task. If required, this agent can request for a deferment of a specific document.

        The workflow generates a credit authorization task for the credit agent.

    4.  A credit authorizer \(credit agent\) works on the credit task to review and approve it.
-   **As a customer or credit agent**

    The customer checks the credit service case and accepts the restructuring terms. Alternatively, a credit agent can get an acceptance from the customer for the restructuring terms and close the credit service case.

    **Note:** A customer \(consumer or contact\) can view the case through the Customer Service Portal, Consumer Service Portal, or another self-service portal. For consumers to view a case using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

    After the customer agrees to the terms, the system creates a loan service case for the loan agent to implement those terms.

-   **As a loan agent**
    1.  A loan agent reviews the case details and updates it.

        The document processor service determines the documents that must be verified for the request. The workflow automatically generates an inbound document verification task for the document agent.

    2.  A document agent works on the inbound document verification task to verify each document listed in the task. If required, this agent can request for a deferment of a specific document.

        The workflow generates a loan authorization task for the loan agent.

    3.  A loan authorizer \(loan agent\) reviews the case details and approves it.
    4.  A loan agent works on the loan update task and updates the loan information in the banking system.

        Banks can automate this task by enabling an integration with the core baking system.


After the case is complete, its state and stage are set to Closed Complete and the work notes are updated.

