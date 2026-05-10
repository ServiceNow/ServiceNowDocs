---
title: Review and respond to collaboration
description: The merchant responds to the collaboration by either providing a refund, a voucher, or a First-Party Trust evidence. If the collaboration isn’t successful, then the second presentment is awaited.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Chargeback, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review and respond to collaboration

The merchant responds to the collaboration by either providing a refund, a voucher, or a First-Party Trust evidence. If the collaboration isn’t successful, then the second presentment is awaited.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector.

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

In this task, three scenarios are possible: merchant responds to collaboration by either a voucher, a refund or a First-Party Trust evidence.

-   **Voucher**:
    -   If the cardholder accepts the voucher, the dispute ends and the transaction moves to Financial adjustments 1. For more information, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).
    -   If the cardholder rejects the voucher, the process awaits a second presentment from the merchant.
-   **Refund**:
    -   If the cardholder receives and accepts the refund, the dispute ends and the transaction moves to Financial adjustments 1.
    -   If the refund isn’t received, the agent raises a **Second first chargeback** and waits for the merchant's second presentment.
-   **First-Party Trust** evidence indicating that this is a valid transaction:
    -   If the cardholder agrees with the provided First-Party Trust evidence, the dispute ends and the transaction moves to Financial adjustments 1.
    -   If the cardholder disagrees with the provided First-Party Trust evidence, the agent raises a **Second first chargeback** and waits for the merchant's second presentment.

For the second presentment:

-   If not received, the case favors the cardholder and the transaction moves to Financial adjustments 1, ending the dispute.
-   If received, the transaction progresses to the next task [Review chargeback response and decide on pre-arbitration or arbitration](review-and-decide-prearbitration.md) in the chargeback process.

If Card Data Security is installed and configured, **Attachments** in the contextual side panel will handle files differently in transaction records. For more information, see [Manage attachments in Card Data Security](../../fso-card-data-security/concept/manage-attachments-in-card-data-security.md).

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

7.  Select the **Review and respond to collaboration** task in **Dispute Workspace**.

8.  On the form, fill in the required fields and any other related information.

9.  Select **Add file** to attach supporting documents to the task.

    **Note:** You must upload a single `.zip` file whenever you submit documents to Mastercard. For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).

10. Select one of the following options from the **Merchant's Response to Collaboration** drop-down list to specify the merchant's response to the chargeback.

    **Note:** In case of integration with Mastercard's Mastercom APIs, the **Merchant's Response to Collaboration** drop-down list automatically shows the merchant response and you can't edit it.

<table id="choicetable_kzh_rp5_vfc"><thead><tr><th align="left" id="d79418e364">

Option

</th><th align="left" id="d79418e367">

Result

</th></tr></thead><tbody><tr><td id="d79418e373">

**__Refund__**

</td><td>

Select this option if a refund is provided by the merchant. The **Customer Decision** drop-down is displayed. Select one of the following options:

-   Select **Accepted** if the cardholder has agreed for the settlement in the form of a refund. The transaction moves to Financial adjustments 1 and the dispute life cycle ends.
-   Select **Denied** if the cardholder has denied the refund. Now, the second presentment is awaited from the merchant.
-   Select **Continue**.

If you select **Denied**, the **Create second first chargeback** option becomes available. Select this option to deny the refund and go for a second first chargeback.

**Note:** If an error message is displayed in the **Activity** work notes, the **Create second first chargeback** button displays again to retry.

The **Second presentment from the merchant** drop-down is displayed. Select one of these options.

    -   **Yes** to indicate that a second presentment is received from the merchant.

The [Review chargeback response and decide on pre-arbitration or arbitration](review-and-decide-prearbitration.md) task displayed.

    -   **No** if there’s no second presentment from the merchant. The case goes in the favor of the cardholder and the transaction moves to Financial adjustments 1 and the dispute life cycle ends. For more information, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).


</td></tr><tr><td id="d79418e473">

**__Voucher__**

</td><td>

Select this option if a voucher is provided by the merchant. The **Customer Decision** drop-down is displayed. Select one of these options.

-   Select **Accepted** if the cardholder has agreed for the settlement in the form of a voucher.

The **Update credit voucher** option becomes available. Select this option to accept the credit. The transaction moves to Financial adjustments 1 [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md) and the dispute life-cycle ends.

**Note:** If an error message is displayed in the **Activity** work notes, the **Update credit voucher** button displays again to retry.

-   Select **Denied** to deny the voucher and go for a second presentment chargeback. The **Update credit voucher** option becomes available. Select this option.

The **Second presentment from the merchant** drop-down is displayed. Select one of these options.

    -   Select **Yes** to indicate that a second presentment is received from the merchant.

The [Review chargeback response and decide on pre-arbitration or arbitration](review-and-decide-prearbitration.md) task displayed.

    -   Select **No** if there’s no second presentment from the merchant. The case goes in the favor of the cardholder and the transaction moves to Financial adjustments 1 and the dispute life cycle ends.


</td></tr><tr><td id="d79418e573">

**__First-Party Trust__**

</td><td>

Select this option if the merchant has responded with a First-Party Trust evidence indicating that this is a valid transaction.The **Customer Decision** drop-down is displayed. Select one of the following options:

-   Select **Accepted** if the cardholder accepts the merchant response. The transaction moves to Financial adjustments 1 and the dispute life cycle ends.
-   Select **Denied** if the cardholder disagrees with the merchant response. Now, the second presentment is awaited from the merchant.
-   Select **Continue**.

If you select **Denied**, the **Create second first chargeback** option becomes available. Select this option to go for a second first chargeback.

**Note:** If an error message is displayed in the **Activity** work notes, the **Create second first chargeback** button displays again to retry.

The **Second presentment from the merchant** drop-down is displayed. Select one of these options.

    -   **Yes** to indicate that a second presentment is received from the merchant.

The [Review chargeback response and decide on pre-arbitration or arbitration](review-and-decide-prearbitration.md) task displayed.

    -   **No** if there’s no second presentment from the merchant. The case goes in the favor of the cardholder and the transaction moves to Financial adjustments 1 and the dispute life cycle ends. For more information, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).


</td></tr></tbody>
</table>    **Note:** In case of integration with Mastercard's Mastercom APIs, if the task state changes to Document Upload Pending after you select **Create second first chargeback**, then the attached document is not uploaded to Mastercard.

11. To reupload the document, delete and replace your attachment with one that meets Mastercard's requirements then select **Upload document**.

    For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).

12. Select **Close task**.


## What to do next

Based on the collaboration with the merchant and cardholder decision, one of these tasks is displayed:

-   For the second presentment value marked as **Yes**, the next task [Review chargeback response and decide on pre-arbitration or arbitration](review-and-decide-prearbitration.md) is displayed.
-   For the second presentment value marked as **No**, outcomes depend on the policy, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).

**Parent Topic:**[Chargeback in Mastercard transaction disputes](../concept/chargeback-stage-mastercard.md)

