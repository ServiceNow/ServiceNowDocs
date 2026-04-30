---
title: Send a contract document for signature
description: After a contract document has been reviewed and finalized, send the document for signature.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reviewing and finalizing a self-serve contract document, Use self-served contract request, Using Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Send a contract document for signature

After a contract document has been reviewed and finalized, send the document for signature.

## Before you begin

The contract document must have been reviewed and finalized, and the contract status must be set to Document ready. For more information, see [Review a contract document in your workspace](cncore-request-changes-ss-cntr.md) and [Work on a contract change request](cncore-finalize-document-ss-cntr-1.md).

If the contract request is linked to a parent contract request, the parent request must be in Contract signed or Closed complete state.

Role required: sn\_cm\_core.contract\_user

## Procedure

1.  Navigate to your workspace.

2.  Select a contract request.

3.  Select **Send for signature**.

    ![Send for signature button in a contract request](../image/cmpro-send-sign.png "Send for signature")

    -   If a message appears containing the details of the contract document, select **Send for signature**.
    -   If a message appears stating that the signatories aren't synchronized:
        1.  Update and sync the signatures.
            -   For versions of Contract Management Pro starting with 1.2.1, see [Resolve the failure to send contract documents for signature \(starting with Contract Management Pro 1.2.1\)](cncore-sync-doc-user.md).
            -   For earlier versions of Contract Management Pro, see [Resolve an error during send for signature](cncore-sync-signatories-user.md).
        2.  Select **Send for signature**.
        3.  Select **Send for signature** in the confirmation message.
    -   If a message appears stating that the parent contract request is not signed, ensure the parent contract is either signed or unlinked before selecting **Send for Signature**.

        For more information, see [Remove a linked contract](cmpro-remove-linked-cntr.md).


## Result

The document is sent for signature to the specified signatories. The activity stream displays details of the contract document that is sent for signature.

The contract request state and contract status updates to Awaiting Signature. For more information, see [Signature workflow for a contract request](../concept/cncore-signature-workflow.md).

**Parent Topic:**[Reviewing and finalizing a self-serve contract document](cncore-review-finalize-contract.md)

