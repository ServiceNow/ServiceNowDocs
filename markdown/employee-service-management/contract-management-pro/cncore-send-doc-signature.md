---
title: Send a contract document for signature
description: Send the document for signature after a contract document has been reviewed and finalized.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-send-doc-signature.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Contract signature]
breadcrumb: [Signature workflow for a contract request, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Send a contract document for signature

Send the document for signature after a contract document has been reviewed and finalized.

## Before you begin

The contract document must have been reviewed and finalized. For more information, see [Review a contract document in your workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-request-changes-ss-cntr.md) and [Work on a contract change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

If the contract request is linked to a parent contract request, the parent request must be in Contract signed or Closed complete state.

Role required: sn\_cm\_core.contract\_user

## About this task

**Note:** The **Send for signature** option is not available for the offline signature. For more information see, [Initiate an offline signature for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-initiate-offline-signature-workspace.md).

## Procedure

1.  Navigate to your workspace.

2.  Select a contract request.

3.  Select **Send for signature**.

    \[Omitted image "cmpro-send-sign.png"\] Alt text: Send for signature button in a contract request

    -   If a message appears containing the details of the contract document, select **Send for signature**.
    -   If a message appears stating that the signatories aren't synchronized:
        1.  Update and sync the signatures.
            -   For versions of Contract Management Pro starting with 1.2.1, see [Resolve the failure to send contract documents for signature \(starting with Contract Management Pro 1.2.1\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-sync-doc-user.md).
            -   For earlier versions of Contract Management Pro, see [Resolve an error during send for signature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-sync-signatories-user.md).
        2.  Select **Send for signature**.
        3.  Select **Send for signature** in the confirmation message.
    -   If a message appears stating that the parent contract request is not signed, ensure the parent contract is either signed or unlinked before selecting **Send for Signature**.

        For more information, see [Remove a linked contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-remove-linked-cntr.md).


## Result

The document is sent for signature to the specified signatories. The activity stream displays details of the contract document that is sent for signature.

The contract request state and contract status updates to Awaiting signature. For more information, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-signature-workflow.md).

**Parent Topic:**[Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-signature-workflow.md)

