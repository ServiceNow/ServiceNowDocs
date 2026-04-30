---
title: Individual Life Claims workflows
description: The Individual Life Claims application installs automated workflows that you can configure for any individual life claims tasks. These workflows create cases and routes any tasks to different departments in your organization.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Managing Individual Life Claims, Individual Life Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Individual Life Claims workflows

The Individual Life Claims application installs automated workflows that you can configure for any individual life claims tasks. These workflows create cases and routes any tasks to different departments in your organization.

## Overview

After a claim case is initiated in the Individual Life Claims application, the workflow proceeds through phases.

The following workflow routes the case and tasks for investigating and managing individual life insurance claims to the roles in different departments. Agents can log in to Financial Services Workspace to work on the tasks in their queue. The workflow includes a decision table to triage and set the priority of a claim.

The case playbook guides agents through the process to fulfill claims:

-   Submitting first notice of loss
-   Claim triage
-   Adjuster claim evaluation
-   Claim closure

## First notice of loss \(FNOL\) claim

-   **Submitting a claim as a first-notice-of-loss representative**
    1.  In the FNOL stage, an insurance policy participant or other reporter reports a loss of life event with an FNOL representative. When the case is created, a workflow triggers automatically with playbook tasks created for managing the case to resolution.
    2.  The representative enters details of the deceased, incident details, and reporter details. A system workflow retrieves the policy snapshots for all the policies that are associated with the claim and creates a claim for each policy. The representative also collects the inbound documents, such as the death certificate. The claim is initiated when the representative submits the case.
    3.  After the representative submits the case, the business decision rules triage the claim, and the case is prioritized.

## Adjuster evaluations

-   **Validating, evaluating, and settling a claim as an adjuster**
    1.  The adjuster reviews the coverages, beneficiaries, and documents for the policies that are associated with the claim.
    2.  The adjuster assigns the reserve amounts against the coverage line items according to the following conditions:
        -   If the assigned reserve amount is within the approval authority of the adjuster, the adjuster approves the results.
        -   If the assigned reserve amount is beyond the approval authority of the adjuster, the system assigns the request to the claims manager for approval.

            If approved by the claims manager, the adjuster proceeds with the claim payment evaluation.

            If the amount isn't approved, the adjuster reevaluates and revises the reserve amount according to the recommendations from the claims manager.

    3.  The adjuster updates the claim record with either a loss reserve, expense reserve, or both.
    4.  The adjuster creates payment amounts against the created reserves that are based on the finalized evaluation:
        -   If the created payment amount is within the approval authority of the adjuster, the adjuster approves the results.
        -   If the amount is beyond the approval authority of the adjuster, the system assigns the request to the claims manager for approval.

            If the claims manager approves the payment amount, the adjuster proceeds with a claim payment evaluation.

            If the amount isn't approved, the adjuster reevaluates and creates a payment amount that is based on the recommendations from the claims manager.

    5.  The adjuster settles the claims by approving or rejecting the claims. If the adjuster approves the review task to settle the claim, the claim case is closed. If the adjuster rejects all related tasks, the claim case automatically closes.

## Claims manager approvals

-   **Approving reserve or payment amounts as a claims manager**
    1.  If an assigned reserve amount is beyond the approval authority of the adjuster, the system assigns the reserve amount request to the claims manager for approval.

        If the claims manager approves the reserve amount, the adjuster proceeds with the claim payment evaluation.

        If the claims manager rejects the reserve amount and provides a recommendation, the adjuster should revise the reserve amount as recommended.

    2.  If a created payment amount is beyond the approval authority of the adjuster, the system assigns the payment amount request to the claims manager for approval. The claims manager reviews the payment amount and claim details and approves or rejects the claim payment.

        If the claims manager approves the payment amount, the adjuster can proceed to settlement.

        If the manager rejects the request and provides a recommendation, the adjuster should revise and submit the payment amount as recommended.

        System-generated work notes stating the approvals or rejections are automatically added to the activity stream for the task and claim case.


## Closures

The case is complete when the states and stage of the case are set to Closed Complete.

**Note:** The adjuster must settle each claim before the case can be closed.

