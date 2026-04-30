---
title: Regenerate contract document after modifying request
description: As a legal user or legal fulfiller, regenerate the contract document for non-disclosure agreement contract requests when the legal request has been modified.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Regenerate contract document after modifying request

As a legal user or legal fulfiller, regenerate the contract document for non-disclosure agreement contract requests when the legal request has been modified.

## About this task

When the parent request is modified, you can use the **Regenerate** option to generate a new contract document from the contract template with the latest metadata, signatories, and tables. You can regenerate a contract document only when the State is Draft or Work in progress.

Any changes made to the signatory information in the contract request will be overwritten by the signatory information from the contract template. If the signatory information is incomplete or inconsistent after regeneration, you can manually update the signatories. For more information, see [Updating and synchronizing signatories](../../contract-mgmt-pro/task/cncore-update-sync-signatories.md).

You can regenerate a contract document only when the State is Draft or Work in progress.

## Before you begin

Role required:

-   sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user
-   sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the List icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  Navigate to **Legal Requests**.

4.  Open a legal request.

5.  Navigate to **Contract request** and open the request.

6.  Select the More Actions icon \(![More Actions icon](../../legal-request-management/image/more-button-icon.png)\) and select **Regenerate**.


## Result

The results of the regeneration depends on the initial state of the document:

-   Draft: Replaces the existing contract document revision.
-   Work in progress: Creates a new contract document revision and any changes made in the previous revision is discarded.

Note that although contract fulfillers can see all contract document revisions, a contract user can see only the latest revision.

**Parent Topic:**[Work on NDA legal requests](snlc-work-on-contract-request.md)

