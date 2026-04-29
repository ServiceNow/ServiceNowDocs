---
title: Synchronize a non-disclosure agreement document after modifying a self-served contract request \(Contract Management Pro 1.2.1\)
description: Synchronize the contract document for non-disclosure agreements contract requests to create a new revision of the document with updated metadata and signatories while retaining the changes made in the previous version of the contact document.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Synchronize a non-disclosure agreement document after modifying a self-served contract request \(Contract Management Pro 1.2.1\)

Synchronize the contract document for non-disclosure agreements contract requests to create a new revision of the document with updated metadata and signatories while retaining the changes made in the previous version of the contact document.

## About this task

**Note:** The **Sync document** option is available only starting with Contract Management Pro version 1.2.1

You can synchronize a contract document only when the contract request is in the Work in progress state.

**Note:** Tables are not updated when you use the **Sync document** option. You must regenerate the document to update the tables. For more information, see [Regenerate contract document after modifying request](snlcregen-contract-doc.md).

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

6.  In the **Contracts documents** tab, select **Sync document**.


## Result

A new contract document revision is created with the update metadata and signatories. The changes made in the previous revision are retained.

**Parent Topic:**[Work on NDA legal requests](snlc-work-on-contract-request.md)

