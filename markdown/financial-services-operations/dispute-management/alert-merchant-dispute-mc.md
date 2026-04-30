---
title: Alert merchant regarding dispute
description: Review merchant response regarding the dispute. The merchant can choose to resolve the disputed transaction or decline to resolve, during the investigation stage.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Investigate, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Alert merchant regarding dispute

Review merchant response regarding the dispute. The merchant can choose to resolve the disputed transaction or decline to resolve, during the investigation stage.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  Select the **Alert merchant regarding dispute** task in **Dispute Workspace**.

8.  On the form, fill in the required fields and any other related information that you have gathered.

9.  In the **Merchant response** field, select one of the following options:

    -   **Accepted Dispute**: Merchant agrees to resolve the dispute with the cardholder. The dispute is resolved and the next task is displayed based on the policy. For more information, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).
    -   **Declined Dispute**: Merchant declines to resolve the dispute with the cardholder. The transaction dispute continues through the dispute process workflow stages.
10. Select **Add file** to attach supporting documents to the task.

    **Note:** You must upload a single `.zip` file whenever you submit documents to Mastercard.

11. Select **Close task**.


## Result

The task state updates to Closed Complete if the merchant resolves the dispute. If the merchant declines the dispute, the transaction continues through the dispute workflow stages.

**Parent Topic:**[Processing a Mastercard dispute](../concept/processing-mastercard-dispute-case.md)

