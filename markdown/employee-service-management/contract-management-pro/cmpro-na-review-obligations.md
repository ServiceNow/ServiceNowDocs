---
title: Review AI-extracted obligations
description: Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents. Approved obligations are added as obligations records in the Obligations tab of the contract repository.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Review AI results, Use agentic workflows, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Review AI-extracted obligations

Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents. Approved obligations are added as obligations records in the **Obligations** tab of the contract repository.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

The manage contract repository agentic workflow uses AI agents to extract key contractual obligations from signed contracts. The obligations are extracted based on the applicable use case in the contract obligation extraction skill. After obligation extraction is complete, a message appears on the contract record and an email notification is sent with a link to review the extracted obligations. The playbook provides a step-by-step interface where you can review each obligation, make necessary edits, and decide whether to approve or reject it. Approved obligations are added as actionable records in the **Obligations** tab of the contract repository.

## Procedure

1.  Open a contract repository record where you want to review the extract information.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d78835e68">

Method

</th><th align="left" id="d78835e71">

Steps

</th></tr></thead><tbody><tr><td id="d78835e77">

**Contract Workspace**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon ![](../../legal-request-management/image/lsd-lcc-list-icon.png).
3.  Select **Executed contracts**.
4.  Select **All**.
5.  Select the contract repository record.


</td></tr><tr><td id="d78835e124">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open a contract request that is in the Closed complete or Contract signed state.
3.  Select the **Contract repository** tab.
4.  Select the contract repository record.


</td></tr><tr><td id="d78835e151">

**Email notification**

</td><td>

Select **Review contract** in the email notification that you receive after the obligation extraction is complete.

</td></tr></tbody>
</table>2.  Select the **Playbook** tab.

    The playbook opens displaying a step-by-step interface to review the extracted obligations.

    ![Contract playbook displaying extracted obligations details.](../image/cmpro-na-playbook.png "Contract playbook")

3.  In the playbook, navigate to the **Review obligations** step under the AI extracted obligations section.

4.  Select **Review**.

    The extracted obligations are displayed on a new tab.

    ![Form displaying the list of extracted obligations.](../image/cmpro-na-ob-extracted.png "Extracted obligations")

5.  Select an obligation to review the obligation details.

    -   The **Details** tab displays the extracted obligation details. Use this tab to edit, approve, or reject the obligation.
    -   The **Activity** tab displays a log of key attributes identified during the extraction process. Use this tab to review how the AI agent detected and populated the obligation, including the original text snippets and metadata extracted from the contract. The **Activity** tab helps you validate the extraction accuracy and provides transparency into the decision-making process for each obligation.
    ![Obligation details form displaying the information extracted by AI.](../image/cmpro-na-ob-reviewob.png "Extracted obligation details")

6.  On the **Details** tab, perform the required action.

    -   Edit the obligation details as needed.

        **Note:** Complete all required fields before saving the changes or approving the obligation.

        For more information on the fields, see [Obligation form](../reference/cncore-obligation-form.md).

    -   Select **Save** to save the changes.
    -   Select **Approve** to approve the extracted obligation and add it as a record in contract repository.
    -   Select **Reject** to reject the extracted obligation.

        Once an obligation is rejected, it’s deactivated and can’t be reactivated again. If you need to add the obligation later, you must create an obligation record manually. For more information, see [Create obligation records](cncore-create-obligations.md).

7.  Repeat step 6 for all the extracted obligations.

8.  Navigate to the **Playbook** tab in the contract repository after you have reviewed all the obligations.

9.  Select **Mark as completed**.


## Result

Approved obligations are available as records in the **Obligations** tab of the contract repository. Rejected obligations are deactivated and excluded from further processing.

If the schedule of the obligation is recurring, the obligation tasks are automatically created based on the interval specified in the **Repeats** field.

If the schedule of the obligation is adhoc, you must create obligation tasks manually. For more information see, [Create an ad hoc obligation task](cncore-adhoc-ob-task.md).

![Obligations tab displaying the list of obligations added in the contract repository record.](../image/cmpro-na-ob-added.png "Obligation records")

**Related topics**  


[Obligation Management](../concept/cncore-obligation-management.md)

[Obligation form](../reference/cncore-obligation-form.md)

[Submit obligation tasks](cncore-work-on-ob-tasks.md)

[Cancel an obligation task](cncore-cancel-ob-task.md)

[Approve or reject obligation tasks](cncore-manage-ob-tasks.md)

[Obligation Management notifications](../reference/cncore-ob-mgmt-notification.md)

