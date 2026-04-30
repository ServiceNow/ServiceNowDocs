---
title: Contract request State and Contract document status in Contract Management Pro
description: Contract requests follow a specific life cycle and move through a series of states in Contract Management Pro. The contract request state and the contract document status are displayed in the State and the Contract status fields on the request record.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2025-05-19"
reading_time_minutes: 4
keywords: [Contract status, State, Contract Management Pro, Contract lifecycle management workflow]
breadcrumb: [Contract Management Pro reference, Contract Management Pro, Employee Service Management]
---

# Contract request State and Contract document status in Contract Management Pro

Contract requests follow a specific life cycle and move through a series of states in Contract Management Pro. The contract request state and the contract document status are displayed in the State and the Contract status fields on the request record.

For a contract request you can see the following:

-   State: Indicating the state of the contract request.
-   Contract status: Indicating the status of the contract document.

<table id="table_tn1_45f_5xb"><thead><tr><th>

State

</th><th>

Description

</th><th>

Contract status for the state

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The contract request is in draft state and not yet submitted.

</td><td>

-   Draft
-   Error

</td></tr><tr><td>

New

</td><td>

The contract request is submitted and yet to be assigned.

</td><td>

-   New
-   Changes requested

</td></tr><tr><td>

Work in progress

</td><td>

The contract request has been assigned to a contract fulfiller.

</td><td>

-   Work in progress
-   Document approved
-   Document approval rejected
-   Document approval cancelled
-   Signing declined
-   E-signature invalid
-   Signature cancelled
-   Changes requested
-   Document ready
-   Review completed
-   Review cancelled
-   Error

</td></tr><tr><td>

Awaiting review

</td><td>

An internal review task has been raised for the review of the contract document.

</td><td>

-   Awaiting review
-   Awaiting information

</td></tr><tr><td>

Awaiting approval

</td><td>

An approval request has been raised and the contract document is awaiting approval.

</td><td>

Awaiting approval

</td></tr><tr><td>

Awaiting signature

</td><td>

All signatories have signed the document.

</td><td>

-   Awaiting signature
-   Preparing for signature
-   Signature paused

</td></tr><tr><td>

Contract signed

</td><td>

The contract document has been signed by all the signatories.

</td><td>

-   Contract signed
-   Contract generation failed

</td></tr><tr><td>

Closed complete

</td><td>

All actions including approvals and signatures are complete.

</td><td>

Contract signed

</td></tr><tr><td>

Cancelled

</td><td>

Request was canceled.

</td><td>

Cancelled

</td></tr></tbody>
</table><table id="table_k1m_v1w_jfc"><thead><tr><th>

Contract document Status

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**State:Draft**

</td></tr><tr><td>

Draft

</td><td>

The contract request is in draft state and not yet submitted.

</td></tr><tr><td>

Error

</td><td>

The contract document could not be created due to missing configurations after submitting a request.

</td></tr><tr><td colspan="2">

**State:New**

</td></tr><tr><td>

New

</td><td>

The contract request is submitted and yet to be assigned.

</td></tr><tr><td>

Changes requested

</td><td>

The contract user has submitted a request giving details of the changes required in the contract document.**Note:** In the New state, the contract document status is set to Changes requested only when the contract request is unassigned.

</td></tr><tr><td colspan="2">

**State:Work in progress**

</td></tr><tr><td>

Work in progress

</td><td>

The contract request is in progress.

</td></tr><tr><td>

Changes requested

</td><td>

The contract user has submitted a request giving details of the changes required in the contract document.

</td></tr><tr><td>

Document ready

</td><td>

The change request submitted for modification in the contract document has been fulfilled.

</td></tr><tr><td>

Document approved

</td><td>

The contract document was approved by the approver.

</td></tr><tr><td>

Document approval rejected

</td><td>

The contract document was rejected by the approver.

</td></tr><tr><td>

Document approval cancelled

</td><td>

The approval task was canceled by the approver.

</td></tr><tr><td>

Signing declined

</td><td>

The signatory has declined signing the contract document.

</td></tr><tr><td>

E-signature invalid

</td><td>

There was an error in the electronic signature workflow.

</td></tr><tr><td>

Signature cancelled

</td><td>

The signature process was canceled.

</td></tr><tr><td>

Review completed

</td><td>

A contract reviewer is reviewing the document and has requested for information from the contract fulfiller.

</td></tr><tr><td>

Review cancelled

</td><td>

A contract reviewer is reviewing the document and has requested for information from the contract fulfiller.

</td></tr><tr><td>

Error

</td><td>

The contract document could not be created due to missing configurations while performing regenerate document action.

</td></tr><tr><td colspan="2">

**State:Awaiting review**

</td></tr><tr><td>

Awaiting review

</td><td>

An internal review task was raised and the contract document is under review.

</td></tr><tr><td>

Awaiting information

</td><td>

A contract reviewer is reviewing the document and has requested for information from the contract fulfiller.

</td></tr><tr><td colspan="2">

**State:Awaiting approval**

</td></tr><tr><td>

Awaiting approval

</td><td>

An approval request has been raised and the contract document is awaiting approval

</td></tr><tr><td colspan="2">

**State:Awaiting signature**

</td></tr><tr><td>

Awaiting signature

</td><td>

The contract document is awaiting signature.

</td></tr><tr><td>

Preparing for signature

</td><td>

The contract document is being prepared for signature.

</td></tr><tr><td>

Signature paused

</td><td>

Modify signatories action has been initiated and the signature workflow is paused.

</td></tr><tr><td colspan="2">

**State:Contract signed**

</td></tr><tr><td>

Contract signed

</td><td>

The contract document has been signed by all the signatories.

</td></tr><tr><td>

Contract generation failed

</td><td>

The contract has been signed, but the generation of the contract document for repository storage has failed.

</td></tr><tr><td colspan="2">

**State:Closed complete**

</td></tr><tr><td>

Contract signed

</td><td>

The contract document has been signed by all the signatories.

</td></tr><tr><td colspan="2">

**State:Cancelled**

</td></tr><tr><td>

Cancelled

</td><td>

Contract request was canceled.

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro reference](../concept/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro](cncore-comp-ccore.md)

[Components installed with Contract Workspace](cncore-comp-contract-workspace.md)

[Components installed with Analytics Pack for Contract Management Pro](cncore-comp-analytics-pack-cmpro.md)

[Clause Variation form](cncore-cv-form.md)

[Contract Configuration form](cncore-contract-config-form.md)

[Properties installed to configure expiry notifications](cncore-properties-installed.md)

[Properties installed to configure contracts integrations](cncore-properties.md)

[Expiring Contracts Condition form fields](cncore-email-notif-expcont-form.md)

[Action assignment form](cmpro-actn-assignment-form.md)

[UFX Add on Event mapping form](cmpro-ufx-event-map-form.md)

[Obligation form](cncore-obligation-form.md)

[Obligation Management notifications](cncore-ob-mgmt-notification.md)

[Contract Management Pro glossary](../concept/contract-management-pro-glossary.md#)

