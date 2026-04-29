---
title: Initiate chargeback
description: Initiate a chargeback for Mastercard transaction disputes and request collaboration from merchants.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Chargeback, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Initiate chargeback

Initiate a chargeback for Mastercard transaction disputes and request collaboration from merchants.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector.

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When you initiate a chargeback, the process follows one of these paths:

-   Mastercard attempts to resolve the dispute through the merchant-cardholder collaboration step.
    -   If **Card network collaboration** is **Yes**, the task [Review and respond to collaboration](review-respond-collaboration.md) displays, indicating collaboration has started.
    -   If the **Card network collaboration** is **No**, then the merchant has the option to proceed with a second presentment.
-   You select the proper action based on the merchant's decision on the second presentment as follows:
    -   If **Yes**, the task [Review chargeback response and decide on pre-arbitration or arbitration](review-and-decide-prearbitration.md) displays, starting the formal chargeback process.
    -   If **No**, the case favors the cardholder and, based on the policy, the transaction moves to one of the Financial Adjustments 1, ending the dispute. For more information about Financial adjustments, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).

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

7.  Select the **Initiate chargeback and recover funds from merchant** task in **Dispute Workspace**.

8.  On the form, fill in the required fields and any other related information.

9.  Select **Add file** to attach supporting documents to the task.

    **Note:**

    -   You must upload a single `.zip` file whenever you submit documents to Mastercard.
    -   When integrated with Mastercard's Mastercom APIs, the system automatically compresses multiple attachments into a single zip file. It also validates attached files against Mastercard requirements for file type and size, and alerts you when any attachment doesn’t meet Mastercard requirements. For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).
10. Select **Initiate chargeback**.

    A chargeback is initiated and a collaboration starts with the merchant, cardholder, and Mastercard.

    **Note:** In case of integration with Mastercard's Mastercom APIs:

    -   If an error message is displayed in the **Activity** work notes, the **Initiate chargeback** button displays again to retry.
    -   If the task state changes to Document Upload Pending, then the attached document isn't uploaded to Mastercard.
11. To reupload the document, delete and replace your attachment with the one that meets Mastercard's requirements then select **Upload document**.

    For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).

12. If you want to stop and revert the chargeback for any reason, select **Reverse chargeback**.

    This closes the chargeback request and ends the dispute lifecycle for the transaction.

    **Note:** This action is available only in case of integration with Mastercard's Mastercom APIs.

13. If you want to proceed, select one of the following options from the **Card network collaboration** drop-down.

    -   **Yes** if the merchant wants to proceed with a collaboration by providing a voucher or a refund. Then the [Review and respond to collaboration](review-respond-collaboration.md) task is displayed.
    -   **No** if the merchant rejects the collaboration and wants to go with a second presentment. The **Second presentment by merchant** drop-down is displayed.

        Select one of the following options:

        -   **Yes** to indicate that the acquirer came in with the second presentment. The [Review chargeback response and decide on pre-arbitration or arbitration](review-and-decide-prearbitration.md) task is displayed.
        -   **No**  if there’s no response. The case goes in the favor of the cardholder and the transaction moves to Financial adjustments 1.
14. Select **Close task**.


## What to do next

-   If the **Card network collaboration** is marked as **Yes**, the [Review and respond to collaboration](review-respond-collaboration.md) displays.
-   Otherwise, based on the second presentment done by the merchant, the appropriate task is displayed.

**Parent Topic:**[Chargeback in Mastercard transaction disputes](../concept/chargeback-stage-mastercard.md)

