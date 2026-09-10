---
title: Modify the signing order for signatories
description: Modify the order in which signatories sign a contract document that has not yet been sent for signature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-set-signing-order.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [Signing order, Parallel signature, Parallel signing]
breadcrumb: [Use self-served contract request, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Modify the signing order for signatories

Modify the order in which signatories sign a contract document that has not yet been sent for signature.

## Before you begin

The contract request must not yet be sent for signature.

Role required: sn\_cm\_core.contract\_fulfiller or sn\_cm\_core.contract\_user

## About this task

The signing order for a signatory is set for the first time when the signatory is added to the contract request. For more information, see [Add signatories in self-served contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-update-sign-ss-cmr.md).

Modify the signing order in Contract Workspace before the contract document is sent for signature.

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request.

3.  Navigate to the **Signatories** tab.

4.  In the **Signing Order** column, select the order value for a signatory.

5.  Enter the signing order number.

    **Note:** To group two or more signatories to sign at the same time, assign them the same signing order.

6.  Select outside the field, or select **Save**.


## Result

The Signatories reflect the updated signing order.

If the signing order contains a gap, it updates automatically when the contract is sent for signature. For more information, see [Send a contract document for signature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-send-doc-signature.md).

**Parent Topic:**[Use self-served contract request]()

