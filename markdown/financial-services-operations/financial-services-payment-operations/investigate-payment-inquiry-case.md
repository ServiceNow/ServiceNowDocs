---
title: Investigate a payment inquiry case
description: Investigate the payment inquiry case so that you can get enough information about the case to resolve it.
locale: en-US
release: yokohama
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Managing payment inquiries, Payment Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Investigate a payment inquiry case

Investigate the payment inquiry case so that you can get enough information about the case to resolve it.

## Before you begin

Role required: sn\_bom\_payment.inquiry\_agent or sn\_bom\_payment.inquiry\_agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon](../../fso-card-operations/image/list-icon.png)\).

3.  In the **Lists** tab, under **Payment Inquiry Cases**, open the case list:

    -   For your assigned cases, click **Assigned to me**.
    -   For all cases, click **All**.
4.  In the list, select the case to work on.

    -   To work on a case that is assigned to you by someone else, click **Accept**.
    -   To work on a case that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.
    The state of the case updates to Work in Progress.

    For information on Payment inquiry form field descriptions, see [Field descriptions for a payment inquiry case](../reference/payment-inquiry-case-form-fields.md).

5.  Review the inquiry type in the **Inquiry type** field.

6.  If the inquiry type is set to Beneficiary Claim Non-Receipt - Internal, select the recipient type in the **Recipient type** field and a recipient bank in the **Recipient bank** field.

    The **Recipient bank** field displays the list of banks that are based on the recipient type.

7.  To request any information from the recipient bank, add your request comments in the **Additional comments** field and click **Request info**.

    The state of the case updates to Awaiting info.

    For a Beneficiary Claim Non-Receipt - Internal case with external recipient, an inquiry task is automatically generated and assigned to the inquiry agent working on the case.

8.  For any ad hoc internal follow-up, create an inquiry task by navigating to the **Inquiry Tasks** tab of the case and clicking **New**.

9.  If there's an inquiry task associated with the case, [work on the inquiry task](work-on-inquiry-task.md) and move it to the **Closed** state.

10. After you've received the required information from the recipient bank, update the necessary fields on the case as per the received information and change the state of the case to **Work in Progress**.

11. If the investigation shows that it's a valid claim, select **Valid claim** and create a claim for the inquiry.

    **Note:** You can set a case as a valid claim only if it's an internal payment inquiry case.

    For more information, see [Create a claim for a payment inquiry case](create-claim-case-inquiry-case.md).


## Result

The customer gets the pre-configured email notifications about the progress of the case.

## What to do next

If you've finished the investigation, [propose a solution](propose-solution-inquiry-case.md) for the case to resolve it.

-   **[Work on an inquiry task](work-on-inquiry-task.md)**  
Work on a payment inquiry task to request additional information that is related to an inquiry case from the recipient bank.
-   **[Create a claim for a payment inquiry case](create-claim-case-inquiry-case.md)**  
Create a claim for an internal payment inquiry case when its investigation indicates that it's a valid claim and the customer is entitled to a refund.

**Parent Topic:**[Managing payment inquiries](../concept/managing-payment-inquiries.md)

