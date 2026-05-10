---
title: Submit a payment inquiry request for an internal inquiry
description: As a front-office worker \(branch employee or call center agent\), you can submit a payment inquiry request on behalf of a customer.
locale: en-US
release: australia
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing payment inquiries, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Submit a payment inquiry request for an internal inquiry

As a front-office worker \(branch employee or call center agent\), you can submit a payment inquiry request on behalf of a customer.

## Before you begin

Role required: sn\_bom\_payment.requestor

## About this task

Business customers and consumers can create payment inquiry requests from the Customer Service Portal and Consumer Service Portal respectively or another self-service portal by selecting service catalog items, filling out the necessary forms, and then submitting these forms.

**Note:** To use the Consumer Service Portal, activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).

Branch workers and customers can submit only internal payment inquiries such as Beneficiary Claim Non-Receipt - Internal and Payment made In Error.

For information about external inquiries, see [Create a payment inquiry case for an external inquiry](create-payment-inquiry-case-external-inquiry.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Create a payment inquiry request from the customer record or an interaction record.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d72837e123">

Option

</th><th align="left" id="d72837e126">

Steps

</th></tr></thead><tbody><tr><td id="d72837e132">

**Payment inquiry request from a consumer record**

</td><td>

1.  In the **Lists** tab, under **Customer**, click **Customers**.
2.  Open the required customer record.


</td></tr><tr><td id="d72837e159">

**Payment inquiry request from a business account record**

</td><td>

1.  In the **Lists** tab, under **Customer**, click **Accounts**.
2.  Click the account that you want to create a payment inquiry for.


</td></tr><tr><td id="d72837e186">

**Payment inquiry request from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, click **My Interactions**.
2.  Open the required interaction record for the customer.
 For information on how to create an interaction, see [Create an interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-management/create-interactions.md).

</td></tr></tbody>
</table>4.  Click **Create Payment Request**.

5.  From the Catalogs list, select **Banking Services**.

6.  Under **Categories**, click **Payment Service**.

7.  Click a payment inquiry item for which you want to submit a request.

    -   To submit a request when the recipient hasn't received the payment, click **Beneficiary Claim Non-Receipt**.​
    -   To submit a request when an error occurred during payment, click **Payment made In Error**.
8.  Fill in any necessary information that is related to the request.

    **Note:** Each payment inquiry request form has a different set of fields that are based on the payment inquiry service.

9.  Click **Submit**.


## Result

-   Based on the request, a payment inquiry case is created in the New state and is assigned to an assignment group or inquiry agent in the payment inquiry department. The assignment group or user to whom the case is assigned is based on the assignment rule.
-   The customer gets a pre-configured email notification about the request submission.

## What to do next

-   Click **View Details** to open the payment inquiry case and view its details. You can also add additional information in the **Comments** field that can help the inquiry agent in resolving the case.
-   An inquiry agent can start [investigating the payment inquiry case](investigate-payment-inquiry-case.md).

**Parent Topic:**[Managing payment inquiries](../concept/managing-payment-inquiries.md)

