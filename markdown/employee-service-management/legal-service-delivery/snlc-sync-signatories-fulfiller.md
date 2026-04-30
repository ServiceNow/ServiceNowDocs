---
title: Resolve the failure to submit a self-serve contract
description: As a legal user, resubmit a contract request that was not submitted due to incomplete signatory information by updating and syncing signatory information.
locale: en-US
release: yokohama
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Updating and synchronizing signatories, Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Resolve the failure to submit a self-serve contract

As a legal user, resubmit a contract request that was not submitted due to incomplete signatory information by updating and syncing signatory information.

## Before you begin

Role required:

-   sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user
-   sn\_cm\_core.contract\_fulfiller

## About this task

If the signatory information is missing, the contract request will be saved as a draft and won't be submitted. Update the signatories and synchronize them to resolve the failure.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the List icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  Navigate to **Legal Requests**.

4.  Open a legal request.

5.  Select the **Contract Requests** tab and open the request.

6.  Select the **Activity** stream to know the validation error.

7.  Select the **Signatories** tab.

8.  Select the signatory and update the information.

9.  Select **Save** to save the signatory details.

10. Select the **Signatories** tab.

11. Select **Sync signatories**.

    The contract document is updated with the new signatory details.

12. Select **Save**.

13. Select **Resubmit**.


## Result

The contract request is resubmitted and the state changes from Draft to Work in progress.

**Parent Topic:**[Updating and synchronizing signatories](snlc-update-sync-signatories.md)

