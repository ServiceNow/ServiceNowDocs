---
title: Submit a loan service request as a requester
description: Help your customers by submitting a loan service request for them. As a requester in the front office, you can do this service for your customer \(consumer or business contact\).
locale: en-US
release: xanadu
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Submitting a loan service request, Using Financial Services Loan Operations, Financial Services Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Submit a loan service request as a requester

Help your customers by submitting a loan service request for them. As a requester in the front office, you can do this service for your customer \(consumer or business contact\).

## Before you begin

Role required: Based on the type of the customer that you are submitting the request for, you need the following roles:

-   For a personal loan service for a consumer: sn\_bom\_loan.b2c\_requestor
-   For a business loan service for a business customer \(account or contact\): sn\_bom\_loan\_b2b.requestor

## About this task

Business customers and consumers can also submit loan service requests from the Customer Service Portal, Consumer Service Portal, or another self-service portal. They can select service catalog items, fill out the necessary forms, and then submit these forms.

**Note:** For consumers to submit a request using the Consumer Service Portal, you must have the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\) activated.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon.](../../fso-card-operations/image/list-icon.png)\).

3.  Create a loan request from the customer record or an interaction record.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d82605e97">

Option

</th><th align="left" id="d82605e100">

Steps

</th></tr></thead><tbody><tr><td id="d82605e106">

**Personal loan service request for a consumer**

</td><td>

1.  In the **Lists** tab, under **Customer**, click **Consumers**.
2.  Click the customer record that you want to open.


</td></tr><tr><td id="d82605e133">

**Business loan service request for a business customer**

</td><td>

1.  In the **Lists** tab, under **Customer**, click **Accounts** or **Contacts**.
2.  Click the customer record that you want to open.


</td></tr><tr><td id="d82605e163">

**Loan service request from an interaction record**

</td><td>

1.  In the **Lists** tab, under **Interactions**, click **My Interactions**.
2.  Click the interaction record for the customer that you want to open.
 For information on how to create an interaction, see [Create an interaction](https://www.servicenow.com/docs/access?context=create-interactions&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Click **Create Loan Request**.

5.  From the Catalogs list, select **Banking Services**.

6.  Under **Categories**, choose whether you want a business loan service or a personal loan service:

    -   For a business loan service, click **Loan Service – Business**.
    -   For a personal loan service, click **Loan Service – Personal**.
7.  Click a loan service that you want to submit a request for.

8.  Fill in any necessary information that is related to the request.

    **Note:** Each loan service request form has a different set of fields that are based on the loan service.

9.  Click **Submit**.


## Result

-   Based on the request type, a loan service case is created in the New state. The case is assigned to an assignment group or a loan agent in the loan service department. The assignment group or user that the case is assigned to is based on the assignment rules.
-   The customer receives a pre-configured email notification about the request submission.

## What to do next

-   Click **View Details** to open the loan service case and view its details. You can also add additional information in the **Comments** field that can help the loan agent in resolving the case.
-   A loan contributor can collect customer documents, if any and submit the loan case for fulfilment.
-   A loan service agent can start working on the case and its tasks.

