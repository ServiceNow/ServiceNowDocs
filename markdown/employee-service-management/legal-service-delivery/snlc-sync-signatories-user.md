---
title: Resolve an error during send for signature
description: As a legal user or fulfiller, update and synchronize signatory details when send for signature fails due to a mismatch between signatory information in the contract request and contract document.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Updating and synchronizing signatories, Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Resolve an error during send for signature

As a legal user or fulfiller, update and synchronize signatory details when send for signature fails due to a mismatch between signatory information in the contract request and contract document.

## Before you begin

Role required:

-   sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user
-   sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the List icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  Navigate to **Legal Requests**.

4.  Open the legal request.

5.  Navigate to the **Contract Requests** tab and open the request.

6.  Navigate to the **Activity** stream to find the validation error.

7.  Select the **Signatories** tab.

8.  Select the signatory and update the information.

9.  Select **Save** to save the signatory details.

10. Select the **Signatories** tab.

11. Select **Sync signatories**.

    The contract document is updated with the new signatory details.

12. Select **Save**.

13. Select **Send for signature.**

    A message appears displaying details of the contract document that is sent for signature.

14. Select **Send for signature** on the confirmation message.


## Result

A new contract document revision is created with the latest signatory details and sent for signature. The Activity stream displays details of the contract document that is sent for signature.

**Parent Topic:**[Updating and synchronizing signatories](snlc-update-sync-signatories.md)

