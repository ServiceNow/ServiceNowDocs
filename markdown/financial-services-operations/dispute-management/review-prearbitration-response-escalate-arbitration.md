---
title: Review pre-arbitration response and escalate to arbitration
description: After you raised a pre-arbitration request in the Chargeback stage of Mastercard transaction dispute, review the response and decide whether to accept, reject, or escalate the pre arbitration to arbitration.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Chargeback, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review pre-arbitration response and escalate to arbitration

After you raised a pre-arbitration request in the Chargeback stage of Mastercard transaction dispute, review the response and decide whether to accept, reject, or escalate the pre arbitration to arbitration.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector.

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

If the agent is not satisfied with the merchant’s pre-arbitration response, the existing request is escalated to arbitration. One of the following scenarios is possible:

-   Accept the pre-arbitration: Review and accept the response, then close the chargeback.
-   Reject without escalation: Review and reject the response, but choose not to proceed with arbitration.
-   Escalate to arbitration: Respond by escalating the existing pre-arbitration to arbitration for further resolution.

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

7.  Select the **Review pre-arbitration response and escalate to arbitration** task in **Dispute Workspace**.

8.  On the form, fill in the required fields and any other related information.

9.  If the **Dispute response** isn't retrieved, select **Get pre arbitration response** to fetch the merchant response.

    **Note:** In case the merchant is providing documents with the pre-arbitration response, check the **Activity** section for the document attachment or a download failure message.

10. If a download failure message is displayed in the **Activity** work notes, select **Get acquirer document** to fetch the pre-arbitration response document from the merchant.

11. Select **Add file** to attach supporting documents to the task.

    **Note:**

    -   You must upload a single `.zip` file whenever you submit documents to Mastercard.
    -   When integrated with Mastercard's Mastercom APIs, the system automatically compresses multiple attachments into a single zip file. It also validates attached files against Mastercard requirements for file type and size, and alerts you when any attachment doesn’t meet Mastercard requirements. For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).
12. Select one of the following options from the **Response outcome** drop-down.

<table id="choicetable_c3f_zll_wfc"><thead><tr><th align="left" id="d37613e333">

Option

</th><th align="left" id="d37613e336">

Description

</th></tr></thead><tbody><tr><td id="d37613e342">

**Unresolved**

</td><td>

Select this option if the cardholder isn’t happy with the merchant's response on pre-arbitration and wants to escalate to arbitration. The **Escalate to arbitration** drop-down is displayed. Select one of the following options: -   **Yes** to proceed with arbitration. Select **Continue** and **Escalate to arbitration**.

**Note:** If an error message is displayed in the **Activity** work notes, the **Escalate to arbitration** button displays again to retry.

The **Arbitration response received** drop-down is displayed.

    -   Select **Yes** if you have received a response from the merchant.

The next task [Review arbitration response](review-arbitration-response-mc.md) is displayed.

    -   Select **No** if you have not received a response from the merchant. The case goes in the favor of the cardholder and the transaction moves to Financial adjustments 1.
-   **No** to end the chargeback, then the transaction moves to the Financial adjustments 2. The task is then marked as Complete.


</td></tr><tr><td id="d37613e423">

**Resolved**

</td><td>

Accept the chargeback response and resolve the dispute. The transaction moves to Financial adjustments 1.

</td></tr></tbody>
</table>    **Note:** In case of integration with Mastercard's Mastercom APIs, if the task state changes to Document Upload Pending after you select **Escalate to arbitration**, then the attached document isn't uploaded to Mastercard.

13. To reupload the document, delete and replace your attachment with one that meets Mastercard's requirements, then select **Upload document**.

    For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).

14. If you want to stop and withdraw the case for any reason, such as you've selected a wrong option, select **Withdraw case**.

    The task is marked as Closed Complete and a new **Review pre-arbitration response and escalate to arbitration** task is automatically generated.

    **Note:** This action is available only in case of integration with Mastercard's Mastercom APIs.


## What to do next

-   When you escalate the pre-arbitration to an arbitration, the request is sent to Mastercard and the state of the task changes to Awaiting External Info.
-   Once a response is received from the merchant, the **Arbitration response received** value is marked as **Yes**. The next activity [Review arbitration response](review-arbitration-response-mc.md) is displayed.
-   If you don’t receive a response from the merchant, then the case goes in favor of the cardholder and the appropriate task is displayed based on the policy.

**Parent Topic:**[Chargeback in Mastercard transaction disputes](../concept/chargeback-stage-mastercard.md)

