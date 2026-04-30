---
title: Using Insurance claims
description: Learn which roles use the Insurance claims application to create, investigate, and manage an insurance claim from the first notice of loss \(FNOL\) to claim closure.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2024-08-30"
reading_time_minutes: 2
breadcrumb: [Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Using Insurance claims

Learn which roles use the Insurance claims application to create, investigate, and manage an insurance claim from the first notice of loss \(FNOL\) to claim closure.

## Overview of an Insurance claims workflow

**Note:** The topics in this section describe a workflow that references the included personal and commercial travel policy products. Your workspace may display differently based on your configuration and implementation.

1.  Create an Insurance claims case.

    The FNOL representative \(sn\_ins\_gen\_claim.fnol\_representative\) creates the case and gathers the initial information on behalf of the claimant. For more information, see [Initiate an Insurance claims case](../task/create-an-insurance-claims-flow-case.md).

2.  Process an Insurance claims case.

    Processors \(sn\_ins\_gen\_claim.processor\) initiate a claim, review a claim to verify it, and complete the fulfillment tasks after an adjuster evaluates the claim. For more information, see [Process an Insurance claims case](../task/process-an-insurance-claims-flow-case.md).

3.  Work on Insurance claims adjuster tasks.

    Adjusters \(sn\_ins\_gen\_claim.adjuster\) review a claim to verify documents, evaluate claim coverages, determine claim payment details, and approve a settlement. For more information, see [Work on Insurance claims adjuster tasks](../task/manage-an-insurance-claims-flow-case.md).

4.  Approve a reserve or payment amount for an Insurance claims case.

    If adjusters submit claim reserve or payment amounts that are higher than their approval authority, a manager \(sn\_ins\_gen\_claim.manager\) receives a request to approve the amount. For more information, see [Approve a reserve or payment amount for an Insurance claims case](../task/approve-a-reserve-or-payment-amount.md).


## Claim participants

You can add any person or company as a participant for a claim. The participant can be an entity in the policy or a third-party.

The insurance processor adds participants to a claim during the First Notice of Loss activity, and can assign them a role \(such as reporter or witness\).

FSO insurance applications store claim contact information in the following Insurance Claims Core tables:

-   The Claim Participant table \[sn\_ins\_claim\_profile\] stores details about all participants involved in the claims process.
-   The Participant Role table \[sn\_ins\_claim\_participant\] stores information on the participant's role in the claim \(such as if they are the injured or insured\).

For more information, see [Insurance Claims Core tables](../../fso-common/reference/insurance-claims-core-tables.md).

