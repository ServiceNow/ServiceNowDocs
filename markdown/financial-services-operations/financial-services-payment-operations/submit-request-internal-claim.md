---
title: Submit a request for an internal claim
description: As a front-office worker \(branch employee or call center agent\), you can submit a claim request on behalf of a customer.
locale: en-US
release: yokohama
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing payment claims and debit approvals, Payment Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Submit a request for an internal claim

As a front-office worker \(branch employee or call center agent\), you can submit a claim request on behalf of a customer.

## Before you begin

Role required: sn\_bom\_payment.requestor

## About this task

Branch workers and customers can submit claim requests only for internal claims. For information about external claims, see [Create a case for an external claim](create-case-external-claim.md).

Internal claims can also be created by inquiry agents if the investigation of an internal payment inquiry case shows that it is a valid claim. For more information, see [Create a claim for a payment inquiry case](create-claim-case-inquiry-case.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon](../../fso-card-operations/image/list-icon.png)\).

3.  Create a claim from the customer record or an interaction record.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d58622e101">

Option

</th><th align="left" id="d58622e104">

Steps

</th></tr></thead><tbody><tr><td id="d58622e110">

**Create a claim from a consumer record**

</td><td>

1.  In the **Lists** tab, under **Customer**, click **Customers**.
2.  Click the customer that you want to create a claim for.


</td></tr><tr><td id="d58622e137">

**Create a claim from a business account record**

</td><td>

1.  In the **Lists** tab, under **Customer**, click **Accounts**.
2.  Click the account that you want to create a claim for.


</td></tr><tr><td id="d58622e164">

**Create a claim from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, click **My Interactions**.
2.  Click the interaction record that you want to create a claim from.
 For information on how to create an interaction, see [Create an interaction](https://www.servicenow.com/docs/access?context=create-interactions&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Click **Create Payment Request**.

5.  From the Catalogs list, select **Banking Services**.

6.  Under **Categories**, click **Payment Service**.

7.  Click **Claim – Internal customer**.

8.  Fill in any information that is related to the request.

9.  Click **Submit**.


## Result

-   A case is created for the claim in the New state. The case is then assigned to an assignment group or claim agent in the payment claim department. The assignment group or user to whom the case is assigned is based on the assignment rules.
-   The customer gets a pre-configured email notification about the request submission.

## What to do next

-   Click **View Details** to open the claim and view its details. You can also add additional information in the **Comments** field that can help the claim agent in resolving the case.
-   A claim agent can start working on the claim.

**Parent Topic:**[Managing payment claims and debit approvals](../concept/managing-payment-claims.md)

