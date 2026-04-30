---
title: Send a contract document for signature
description: After a contract document has been reviewed and finalized, send the document for signature.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reviewing and finalizing a self-serve contract document, Use a self-served contract request, Use Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Send a contract document for signature

After a contract document has been reviewed and finalized, send the document for signature.

## Before you begin

The contract document must have been reviewed and finalized, and the contract status must be set to Document ready. For more information, see [Review a contract document in your workspace](cncore-request-changes-ss-cntr.md) and [Work on a contract change request](cncore-finalize-document-ss-cntr-1.md).

Role required: sn\_cm\_core.contract\_user

## Procedure

1.  Navigate to your workspace.

2.  Select a contract request.

3.  Select the **Contract documents** tab.

4.  Select **Send for signature**.

    -   If a message is displayed containing the details of the contract document, select **Send for signature**.
    -   If a message is displayed stating that the signatories aren't synchronized:
        1.  Update and sync the signatures.
            -   For versions of Contract Management Pro starting with 1.2.1, see [Resolve the failure to send contract documents for signature \(starting with Contract Management Pro 1.2.1\)](cncore-sync-doc-user.md).
            -   For earlier versions of Contract Management Pro, see [Resolve an error during send for signature](cncore-sync-signatories-user.md).
        2.  Select **Send for signature**.
        3.  Select **Send for signature** in the confirmation message.

## Result

The document is sent for signature to the specified signatories. The activity stream displays details of the contract document that is sent for signature.

The contract request state and contract status updates to Awaiting Signature. For more information, see [Signature workflow for a contract request](../concept/cncore-signature-workflow.md).

**Parent Topic:**[Reviewing and finalizing a self-serve contract document](cncore-review-finalize-contract.md)

