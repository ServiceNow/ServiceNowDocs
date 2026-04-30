---
title: Personal Lines Claims workflows
description: The Personal Lines Claims application installs automated workflows that you can configure for any claims tasks. These workflows create cases and route any tasks accordingly.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Managing Personal Lines Claims, Personal Lines Claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Personal Lines Claims workflows

The Personal Lines Claims application installs automated workflows that you can configure for any claims tasks. These workflows create cases and route any tasks accordingly.

After a claim case is initiated, the workflow proceeds through phases. A business rules engine with baseline, configurable rules can categorize a claim as potential fraud, or as a duplicate claim, for example. Some example business rules include:

-   If the number of properties or participants submitted for the claim is greater than two, the claim is considered as high priority.
-   If the number of claims submitted by a customer for the same insurance policy is greater than four, a claim will be automatically flagged as potential fraud.
-   If the number of claims submitted by a customer is less than five, and the reported loss date relative to the policy start date is less than three days, a claim validation task is created for a processor to review.

The following workflow routes the case and tasks for investigating and managing insurance claims to roles in different departments. The front and back-office agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through these overall steps that are needed to fulfill claims:

-   Submitting first notice of loss
-   Claim validation
-   Adjuster claim evaluation
-   Fraud evaluation
-   Claim closure

![Workflow showing the claims process for a personal auto claim using the Personal Lines Claims application. For the image description, see the text that follows.](../image/claims-process-flow-personal-auto-claim.png "Claims Process Flow – Personal Auto Claim​")

## First notice of loss \(FNOL\)

-   **Submitting a claim as a first-notice-of-loss representative**
    1.  In the First notice of loss \(FNOL\) stage, an insurance policy claimant reports a loss with an FNOL representative. Once the case is created, a workflow triggers automatically with playbook tasks created for managing the case to resolution.
    2.  The FNOL representative documents the incident, property, participant, and injury details obtained for the claim, as well as the coverages available for relevant claims. The representative also collects and submits applicable inbound documents for verification, such as vehicle license, and initiates the claim by submitting the case.
    3.  Once the initiated case is submitted, business decision rules:
        -   Can prioritize the claim case, depending on the number of properties or participants reported in the claim
        -   Can trigger a task and refer a claim case to the Special Investigation Unit department for further evaluation
        -   Can trigger the claim validation task for further review
        -   Can forward the claim to an adjuster for loss evaluation

## Claim validation stage

-   **Validating and closing a claim as a claims processor**
    1.  In the Claim validation stage, the processor updates task details, and rejects or approves the claim task accordingly.
    2.  If the processor validates the task by approving it, it moves to the adjuster evaluation stage.

## Adjuster evaluation

-   **Evaluating and settling a claim as an adjuster**
    1.  In the Adjuster evaluation stage, the adjuster reviews and verifies or rejects the submitted claim documents. The adjuster also reviews coverages, and updates or adds coverages if appropriate.
    2.  The adjuster can refer the claim to the SIU department for claim investigation. Once the SIU department completes the fraud review task, the adjuster can settle or reject the claim.
    3.  The adjuster evaluates a claim and assigns a reserve amount against relevant coverage, based on loss details.
        -   If the assigned reserve amount is within the approval authority of the adjuster, the adjuster approves the results.
        -   If the assigned reserve amount is beyond the approval authority of the adjuster, the adjuster assigns the request to the claims manager for approval. If the reserve amount is approved by the claims manager, the adjuster proceeds with the claim payment evaluation. If the amount isn’t approved, the adjuster re-evaluates and revises reserve amount based on the recommendations from the claims manager.
    4.  The adjuster updates the claim record with either loss reserve, expense reserve, or both.
    5.  The adjuster creates payment amounts against the created reserves, based on finalized evaluation.
        -   If the created payment amount is within the approval authority of the adjuster, the adjuster approves the results.
        -   If the amount is beyond the approval authority of the adjuster, the adjuster assigns the request to the claims manager for approval. If the claims manager approves the payment amount, the adjuster proceeds with a claim payment evaluation. If the amount isn't approved, the adjuster re-evaluates and creates a new payment amount based on the recommendations from the claims manager.
    6.  The adjuster approves or rejects the review task. If the adjuster approves the review task to settle the claim, the claim case moves to the fulfillment stage to be closed by the claims processor. If the adjuster rejects all related tasks, the claim case automatically closes.

## Special Investigation Unit \(SIU\) tasks

-   **Investigating a potential fraud claim as a special investigation unit agent**
    1.  If business rules determine that the claim requires validation, or if the adjuster determines possibility of fraud, a task triggers to the SIU department for investigation. An SIU agent reviews the fraud task, updates details in the evaluation task record, and approves or rejects the task. An approved evaluation task indicates a determination of fraud not found. A rejected evaluation task indicates that the claim is determined to be invalid and potentially fraud.
    2.  If the task is approved, the claim is concluded as fraud not found, and can be approved by the adjuster. When the claim is approved, the case moves to the fulfillment stage, which the claim processor completes.

## Claims manager approval tasks

-   **Approving reserve or payment amounts as a claims manager**
    1.  If an assigned reserve amount is beyond the approval authority of the adjuster, the system assigns the reserve amount request to the claims manager for approval. If the claims manager approves the reserve amount, the adjuster proceeds with the claim payment evaluation. If the claims manager rejects the reserve amount and provides a recommendation, the adjuster should revise the reserve amount as per recommended.
    2.  If a created payment amount is beyond the approval authority of the adjuster, the system assigns the payment amount request to the claims manager for approval. The claims manager reviews the payment amount and claim details, and approves or rejects the claim payment. If the claims manager approves the payment amount, the adjuster can proceed to settlement. But if the manager rejects the request and provides recommendation, the adjuster should revise and submit payment amount as per recommended. System-generated work notes stating the approval or rejection automatically add to the Activity stream for the task and claim case.

## Closure

The case is complete when the states and stage of the case sets to Closed Complete.

