---
title: Close a claim case
description: Close the claim case when you've completed the claimed refund process.
locale: en-US
release: australia
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing payment claims and debit approvals, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Close a claim case

Close the claim case when you've completed the claimed refund process.

## Before you begin

Ensure that the claim customer has accepted the notification for the refund completion.

Role required: sn\_bom\_payment.claim\_agent or sn\_bom\_payment.claim\_agent\_connector

## About this task

If there's a Customer or Consumer Service Portal for customers, they get a notification for the refund completion on the portal from where they can choose to accept or reject the resolution. If the customer accepts the refund completion on the portal, the case state automatically changes to Closed. For more information, see [Accept or reject a case solution from the Consumer Service Portal](https://www.servicenow.com/docs/access?context=resolve-cases-consumer-portal&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

**Note:** To use the Consumer Service Portal, activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Claims**, click **Assigned to me**.

4.  In the list, click the case that you want to open.

5.  In the **Actual treatment** field, select the treatment type for the claim.

6.  Click **Close**.


## Result

A pre-configured email about the case closure is sent to the claim customer.

**Parent Topic:**[Managing payment claims and debit approvals](../concept/managing-payment-claims.md)

