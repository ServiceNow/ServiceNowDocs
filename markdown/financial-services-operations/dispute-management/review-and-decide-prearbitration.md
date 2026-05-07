---
title: Review chargeback response and decide on pre-arbitration or arbitration
description: Review second presentment for the chargeback and initiate pre-arbitration or arbitration, as required for the dispute workflow of the Chargeback stage. For Mastercard transaction chargeback, you can skip raising the pre-arbitration and directly raise the arbitration request.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Chargeback, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review chargeback response and decide on pre-arbitration or arbitration

Review second presentment for the chargeback and initiate pre-arbitration or arbitration, as required for the dispute workflow of the Chargeback stage. For Mastercard transaction chargeback, you can skip raising the pre-arbitration and directly raise the arbitration request.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector.

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

This task becomes active when the merchant proceeds with a second presentment after the collaboration step is not successful. The following outcomes are possible:

-   Mark as **Resolved**: Review the second presentment, mark it as **Resolved**, and close the chargeback. The transaction moves to Financial adjustments 1.
-   Mark as **Unresolved**: If the second presentment is **Unresolved** and the cardholder decides not to proceed further with the chargeback, the transaction moves to Financial adjustments 2.
-   Escalate to pre-arbitration or arbitration: If the second presentment is **Unresolved** and the cardholder decides to proceed with the chargeback, then create a pre-arbitration or arbitration.
    -   If the merchant responds, the task progresses to the next stage.
    -   If the merchant doesn't respond within the specified time frame, a response from Mastercard displays on your **Landing page** and according to which you can manually take an action on the disputed transaction.

        **Note:** You can access this response from your **Landing Page** &gt; **Acquirer deadline expired tasks**. For more information, see [Dispute agent workspace](../concept/workspace-for-agent.md)


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

7.  Select the **Review chargeback response and decide on pre-arbitration or arbitration** task in **Dispute Workspace**.

8.  On the form, fill in the required fields and any other related information.

9.  Review the chargeback response and any received documents from the merchant and provide an outcome.

    You can also review the **Chargeback reason code and description** to review the chargeback reason codes.

    **Note:** In case the merchant is providing documents with the chargeback response, check the **Activity** section for the document attachment or a download failure message.

10. If the details of the merchant response aren't retrieved, select **Get second presentment details** to fetch the chargeback response of the merchant.

11. If a download failure message displays in the **Activity** work notes, select **Get acquirer document** to fetch the second presentment document of the merchant.

12. Select **Add file** to attach supporting documents to the task.

    **Note:**

    -   You must upload a single `.zip` file whenever you submit documents to Mastercard.
    -   When integrated with Mastercard's Mastercom APIs, the system automatically compresses multiple attachments into a single zip file. It also validates attached files against Mastercard requirements for file type and size, and alerts you when any attachment doesn’t meet Mastercard requirements. For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).
13. In the **Response outcome** field, select **Resolved** or **Unresolved**.

<table id="choicetable_sc5_fy5_vfc"><thead><tr><th align="left" id="d55157e437">

Selection

</th><th align="left" id="d55157e440">

Result

</th></tr></thead><tbody><tr><td id="d55157e446">

**Unresolved**

</td><td>

Select **Unresolved** to indicate that the chargeback is not resolved, the **Respond to second presentment** drop-down is displayed. Select one of the following options: -   **Yes** to respond to the merchant's second presentment. The **Response Type** drop-down is displayed. Select one of these options.
    -   Select **Create pre-arbitration** to create a pre-arbitration request.

        1.  Enter the **Pre-arbitration filing amount** in the appropriate currency.
        2.  Enter the **Reason for case filing**.
        3.  Select **Continue** and **Create pre arbitration**.

**Note:** If an error message is displayed in the **Activity** work notes, the **Create pre arbitration** button displays again to retry.

The **Pre arbitration response received** drop-down is displayed.

            -   If a response is received from the acquirer, then the value is set to **Yes**. You’ll be redirected to the next task [Review pre-arbitration response and escalate to arbitration](review-prearbitration-response-escalate-arbitration.md).
            -   If you don’t receive a response from the merchant, then the case goes in the favor of the cardholder and the transaction moves to Financial adjustments 1.
For Mastercard dispute transaction, you can skip raising the pre-arbitration and directly raise the arbitration request.

    -   Select **Create arbitration** to create an arbitration request.
        1.  Enter the **Arbitration filing amount** in the appropriate currency.
        2.  Enter the **Reason for case filing**.
        3.  Select **Continue** and **Create arbitration**.

**Note:** If an error message is displayed in the **Activity** work notes, the **Create arbitration** button displays again to retry.

The **Arbitration response received** drop-down is displayed.

            -   If a response is received from the acquirer, then the value is set to **Yes**. You’ll be redirected to the next task [Review arbitration response](review-arbitration-response-mc.md).
            -   If you don’t receive a response from the merchant, then the case goes in the favor of the cardholder and the transaction moves to Financial adjustments 1.
-   **No** to end the chargeback, then the transaction moves to the Financial adjustments 2. The task is then marked as Complete.


</td></tr><tr><td id="d55157e625">

**Resolved**

</td><td>

Accept the chargeback response and resolve the dispute. The transaction moves to Financial adjustments 1.

</td></tr></tbody>
</table>    When you select the pre-arbitration or arbitration, the **Chargeback reason code and description** field becomes editable enabling you to modify the reason code.

    **Note:** In case of integration with Mastercard's Mastercom APIs, if the task state is Document Upload Pending after you select **Create pre arbitration** or **Create arbitration**, then the attached document isn't uploaded to Mastercard.

14. To reupload the document, delete and replace your attachment with one that meets Mastercard's requirements, then select **Upload document**.

    For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).

15. If you want to stop and withdraw the case for any reason, such as you've selected a wrong option, select **Withdraw case**.

    The task is marked as Closed Complete and a new **Review chargeback response and decide on pre-arbitration or arbitration** task is automatically generated.

    **Note:** This action is available only in case of integration with Mastercard's Mastercom APIs.


## What to do next

Based on the option the dispute agent selects, the response received field changes accordingly.

-   **Pre-arbitration** - When a response is received from the merchant for the pre-arbitration, the **Pre arbitration response received** value is marked as **Yes**. You’ll be redirected to the next task [Review pre-arbitration response and escalate to arbitration](review-prearbitration-response-escalate-arbitration.md). If you don’t receive a response from the merchant, then the appropriate task is displayed based on the policy.
-   **Arbitration** - When a response is received from the merchant, the **Arbitration response received** value is marked as **Yes**. You’ll be redirected to the next task [Review arbitration response](review-arbitration-response-mc.md). If you don’t receive a response from the merchant, then the appropriate task is displayed based on the policy.

**Parent Topic:**[Chargeback in Mastercard transaction disputes](../concept/chargeback-stage-mastercard.md)

