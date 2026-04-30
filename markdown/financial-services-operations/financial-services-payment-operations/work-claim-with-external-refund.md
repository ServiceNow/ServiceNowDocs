---
title: Work on a claim with an external refund
description: Work on an internal claim to determine if it’s valid and where to get the refund from.
locale: en-US
release: zurich
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing payment claims and debit approvals, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a claim with an external refund

Work on an internal claim to determine if it’s valid and where to get the refund from.

## Before you begin

Role required: sn\_bom\_payment.claim\_agent or sn\_bom\_payment.claim\_agent\_connector

## About this task

For an internal claim, the refund type can be external or internal.

-   An external refund type indicates that the refund comes from a third-party bank.
-   An internal refund type indicates that the refund comes from the bank internally, such as from a customer or the bank itself.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Claims**, open the case list.

    -   For your assigned cases, click **Assigned to me**.
    -   For all cases, click **All**.
4.  In the list, select the case to work on.

    -   To work on a case that is assigned to you by someone else, click **Accept**.
    -   To work on a case that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.
    The state of the case updates to Work in Progress.

5.  In the **Claim type** field, verify that the claim type is set to **Internal**.

6.  In the **Refund type** field, select **External**.

7.  Request the refund from the third-party bank.

    1.  Fill in the claim details in these fields:

        -   Error type
        -   Error category
        -   Error subcategory
        -   Requested treatment
        -   Claim bank
        -   Transaction ID
        -   Refund bank
        For information on the Claim form field descriptions, see [Field descriptions for a claim case](../reference/claim-form-fields.md).

    2.  In the **State** field, change the state of the case to **Awaiting Refund** and click **Update**.

    A claim task is automatically generated and assigned to the claim agent that is working on the case. However, for any internal follow-ups, you can also create an ad hoc claim task by navigating to the **Claim Tasks** tab of the case and clicking **New**.

8.  [Work on the claim task](work-claim-task.md) to follow up with the refund bank and move it to the **Closed** state.

9.  After you've received the refund from the refund bank, complete the refund for the claim.

    1.  In the **Actual treatment** field, select the treatment type.

    2.  In the **Outcome** field, select an appropriate outcome.

    3.  In the **Outcome notes** field, enter the comments that are related to the outcome.

    4.  In the **State** field, change the state of the case to **Refund Complete** and click **Update**.

10. Get an approval from the claim customer for the refund completion and click **Close** to complete the claim.

    For more information, see [Close a claim case](close-claim-case.md).


## Result

The customer gets the pre-configured email notifications about the progress of the claim.

-   **[Work on a claim task for an external refund](work-claim-task.md)**  
Using a claim task, follow up with the third-party bank for a claim refund.

**Parent Topic:**[Managing payment claims and debit approvals](../concept/managing-payment-claims.md)

