---
title: Initiate an offline signature for a contract request
description: Initiate an offline signature when a contract is signed outside Contract Management Pro and record the signed document in Contract Management Pro.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/legal-service-delivery/snlc-initiate-offline-signature.html
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
keywords: [offline signature, contract request, Contract Management Pro]
breadcrumb: [Signature workflow for a request, Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Initiate an offline signature for a contract request

Initiate an offline signature when a contract is signed outside Contract Management Pro and record the signed document in Contract Management Pro.

## Before you begin

Role required: sn\_lg\_cnt.contract\_fulfiller and sn\_cm\_core.contract\_fulfiller

## About this task

**Note:** The **Initiate offline signature** option is not available for wet signature and electronic signature. For more information, see [Send a contract document for signature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-send-doc-signature.md).

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request where the signature type is offline signature.

3.  Select **Initiate offline signature**.

4.  In the confirmation message, select **Initiate**.


## Result

-   The contract request state updates to **Awaiting signature**.
-   The system does not send signature request emails to signatories.
-   The status of all signatories is set to **Pending**.

From this state, only the **Upload signed contracts** and **Cancel signature** actions are available.

For offline signatures, when uploading the signed contract, you don't need to select signatories. For more information, see [Upload a signed contract document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-upload-doc-wsignature.md).

To cancel the offline signature process, see [Cancel the signature process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-cancel-a-manual-signature.md).

**Parent Topic:**[Signature workflow for a request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-lsd-signature-workflow.md)

