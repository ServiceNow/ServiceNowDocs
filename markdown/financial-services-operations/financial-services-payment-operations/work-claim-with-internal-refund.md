---
title: Work on a claim with an internal refund
description: Work on a claim to determine if it's valid and where to get the refund from.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/financial-services-payment-operations/work-claim-with-internal-refund.html
release: zurich
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing payment claims and debit approvals, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a claim with an internal refund

Work on a claim to determine if it's valid and where to get the refund from.

## Before you begin

Role required: sn\_bom\_payment.claim\_agent or sn\_bom\_payment.claim\_agent\_connector

## About this task

An internal refund type in a claim indicates that the refund should come from the bank internally, such as from a customer or the bank itself.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(\[Omitted image "inline-data-vis-96px-list.png"\] Alt text: lists icon\).

3.  In the **Lists** tab, under **Claims**, open the case list.

    -   For your assigned cases, click **Assigned to me**.
    -   For all cases, click **All**.
4.  In the list, select the case to work on.

    -   To work on a case that is assigned to you by someone else, click **Accept**.
    -   To work on a case that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.
    The state of the case updates to Work in Progress.

    For information on the Claim form field descriptions, see [Field descriptions for a claim case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-payment-operations/claim-form-fields.md).

5.  In the **Claim type** field, review the claim type.

6.  In the **Refund type** field, select **Internal**.

    **Note:** For an external claim type that is coming from a third-party bank, **Refund type** is set by default to Internal.

7.  To get the refund from a bank or customer, update the necessary fields and [create a debit approval case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-payment-operations/create-debit-approval-case.md).

    -   The state of the case updates to Awaiting Refund.
    -   The **Debit approval** field is populated with the debit approval case number.
8.  For any ad hoc internal follow-up, create a claim task by navigating to the **Claim Tasks** tab of the case and clicking **New**.

    For more information, see [Work on a claim task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-payment-operations/work-claim-task.md).

9.  [Work on the debit approval case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-payment-operations/work-debit-approval-case-internal-refund.md) to complete the refund.

    -   The state of the claim case updates to Refund Complete.
    -   The **Outcome**, **Outcome notes**, and **Refund amount** fields on the claim are updated from the debit approval case.
10. Get an acceptance from the claim customer for the refund completion and click **Close** to complete the claim.

    For more information, see [Close a claim case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-payment-operations/close-claim-case.md).


## Result

The claim customer gets the pre-configured email notifications about the progress of the claim.

## What to do next

If it's an external claim, update the third-party bank about the claim closure.

-   **[Create a debit approval case for an internal refund](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-payment-operations/create-debit-approval-case.md)**  
Create a debit approval case for a claim so that you can request a refund internally from one of your banks or a customer.
-   **[Work on a debit approval case to complete a refund](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-payment-operations/work-debit-approval-case-internal-refund.md)**  
Work with your internal customer or bank to get the debit amount approved so that you can complete the claim refund.

**Parent Topic:**[Managing payment claims and debit approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-payment-operations/managing-payment-claims.md)

