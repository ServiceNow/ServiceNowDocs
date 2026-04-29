---
title: Propose a solution for an inquiry case
description: Propose a solution that is based on your findings from the investigation of the inquiry case that you've just finished, so that you can resolve the case.
locale: en-US
release: australia
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing payment inquiries, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Propose a solution for an inquiry case

Propose a solution that is based on your findings from the investigation of the inquiry case that you've just finished, so that you can resolve the case.

## Before you begin

Role required: sn\_bom\_payment.inquiry\_agent or sn\_bom\_payment.inquiry\_agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Payment Inquiry Cases**, click **Assigned to me**.

4.  In the list, click the case that you want to resolve.

5.  If the state of the case is other than Work in Progress, change the state to **Work in Progress** in the **State** field.

6.  In the **Resolution code** field, select an appropriate resolution code that is based on the received information.

7.  In the **Resolution notes** field, enter your comments for the proposed solution.

8.  Click **Propose Solution**.


## Result

-   The state of the case updates to Resolved.
-   A pre-configured email notification about the case resolution is sent to the customer.
-   If there's a Customer or Consumer Service Portal for customers, they get a notification for the proposed solution on the portal. Buttons for accepting or rejecting the solution appear in the section of the form that shows the consumer actions on the portal.

    For more information, see [Accept or reject a case solution from the Consumer Service Portal](https://www.servicenow.com/docs/access?context=resolve-cases-consumer-portal&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

    **Note:** To use the Consumer Service Portal, activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).


## What to do next

Get an acceptance from the customer for the resolution and [close the inquiry case](close-payment-inquiry-case.md).

If the customer rejects the proposed solution, move the case back to the Open state. If the customer rejected the proposed solution from the Customer or Consumer Service Portal, the state of the case automatically updates to Open.

**Parent Topic:**[Managing payment inquiries](../concept/managing-payment-inquiries.md)

