---
title: Resolve the failure to send contract documents for signature \(starting Contract Management Pro 1.2.1\)
description: Update signatory details in an external contract document when there is a failure in sending the document for signature due to a mismatch between the signatory information in the contract request and the contract document.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Updating and synchronizing signatories, Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Resolve the failure to send contract documents for signature \(starting Contract Management Pro 1.2.1\)

Update signatory details in an external contract document when there is a failure in sending the document for signature due to a mismatch between the signatory information in the contract request and the contract document.

## Before you begin

Role required:

-   sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user
-   sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the List icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  Navigate to **Legal Requests**.

4.  Open a legal request.

5.  Navigate to the **Contract Requests** tab and open the request.

6.  Navigate to the **Activity** stream to learn the validation error.

7.  Select the **Signatories** tab.

8.  Select the signatory and update the information.

9.  Select **Save** to save the signatory details.

10. Select the **Contracts documents** tab.

11. Select **Sync document**.

    A new contract document revision is created with the updated signatory information.

12. Select **Save** to save the contract request.

13. Select **Send for signature.**

    A message appears displaying details of the contract document that is sent for signature.

14. Select **Send for signature** on the confirmation message.


**Parent Topic:**[Updating and synchronizing signatories](snlc-update-sync-signatories.md)

