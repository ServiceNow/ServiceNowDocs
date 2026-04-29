---
title: Review arbitration response
description: Review the arbitration response received from Mastercard and proceed to resolve the dispute. This step occurs in the Mastercard dispute process when you’ve escalated from pre‑arbitration to arbitration or skipped pre‑arbitration and moved directly into arbitration.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Chargeback, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review arbitration response

Review the arbitration response received from Mastercard and proceed to resolve the dispute. This step occurs in the Mastercard dispute process when you’ve escalated from pre‑arbitration to arbitration or skipped pre‑arbitration and moved directly into arbitration.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector.

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

This task displays during one of the possibilities in the chargeback stage:

-   An arbitration request is submitted after a pre-arbitration.
-   Arbitration is initiated directly, skipping pre-arbitration.

Review the ruling from Mastercard and choose whether to resolve the dispute or take further action.

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

7.  Select the **Review arbitration response** task in **Dispute Workspace**.

8.  On the form, fill in the required fields and any other related information.

9.  If the **Dispute response** isn't retrieved, select **Get arbitration response** to fetch Mastercard response.

    **Note:** In case Mastercard is providing documents with the arbitration response, check the **Activity** section for the document attachment or a download failure message.

10. If a download failure message is displayed in the **Activity** work notes, select **Get acquirer document** to fetch the arbitration response document from Mastercard.

11. In the **Response outcome** field, select one of the following options.

<table id="choicetable_p21_t5l_wfc"><thead><tr><th align="left" id="d40757e289">

Selection

</th><th align="left" id="d40757e292">

Result

</th></tr></thead><tbody><tr><td id="d40757e298">

**Unresolved**

</td><td>

Select this option if you are not happy with the arbitration response from Mastercard. The next task is displayed based on Financial adjustments 2.

For more information about Financial adjustments, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).

</td></tr><tr><td id="d40757e323">

**Resolved**

</td><td>

Select this option if you’re satisfied with the arbitration response and close the dispute. The transaction moves to Financial adjustments 1.

</td></tr></tbody>
</table>12. Select **Add file** to attach supporting documents to the task.

    **Note:** You must upload a single `.zip` file whenever you submit documents to Mastercard. For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).


## What to do next

The task is marked to closure.

**Parent Topic:**[Chargeback in Mastercard transaction disputes](../concept/chargeback-stage-mastercard.md)

