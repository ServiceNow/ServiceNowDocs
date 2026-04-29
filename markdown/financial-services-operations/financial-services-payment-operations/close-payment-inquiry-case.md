---
title: Close a payment inquiry case
description: Close the case after you've created a claim case for the inquiry case or the customer has accepted your proposed solution.
locale: en-US
release: australia
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing payment inquiries, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Close a payment inquiry case

Close the case after you've created a claim case for the inquiry case or the customer has accepted your proposed solution.

## Before you begin

If the inquiry case is set to be a valid claim, ensure that you've [created a claim case](create-claim-case-inquiry-case.md) for it.

If you've proposed any other solution for the case, ensure that the customer has accepted your proposed solution.

Role required: sn\_bom\_payment.inquiry\_agent or or sn\_bom\_payment.inquiry\_agent\_connector

## About this task

If there's a Customer or Consumer Service Portal for customers, they get a notification for the proposed solution on the portal from where they can choose to accept or reject the proposed solution for a case. If the customer accepts the solution proposed by the agent, the case state automatically changes to Closed.

For more information, see [Accept or reject a case solution from the Consumer Service Portal](https://www.servicenow.com/docs/access?context=resolve-cases-consumer-portal&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

**Note:** To use the Consumer Service Portal, activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Payment Inquiry Cases**, click **Assigned to me**.

4.  In the list, click the case that you want to close.

5.  If you've created a claim and then plan on closing the inquiry case, fill in the resolution fields.

    1.  In the **Resolution code** field, select an appropriate resolution code.

    2.  In the **Resolution notes** field, enter your comments for the proposed solution.

6.  Click **Close**.


## Result

A pre-configured email about the case closure is sent to the customer.

**Parent Topic:**[Managing payment inquiries](../concept/managing-payment-inquiries.md)

