---
title: Review AI-extracted obligations Software Asset Workspace
description: Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents. Approved obligations are added as obligations records in the Obligations tab of the contract repository.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use manage contract repository agentic workflow, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Review AI-extracted obligations Software Asset Workspace

Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents. Approved obligations are added as obligations records in the **Obligations** tab of the contract repository.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller, sam\_admin/sam\_user, and now\_assist\_panel\_user

## About this task

The manage contract repository agentic workflow uses AI agents to extract key contractual obligations from signed contracts. The obligations are extracted based on the applicable use case in the contract obligation extraction skill. After obligation extraction is complete, a message appears on the contract record and an email notification is sent with a link to review the extracted obligations. The playbook provides a step-by-step interface where you can review each obligation, make necessary edits, and decide whether to approve or reject it. Approved obligations are added as actionable records in the **Obligations** tab in the License operations view.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Contracts** &gt; **Software contracts**.

2.  Open a Contract record for which you want to review the extracted obligation record.

3.  Select the **Playbook** tab.

    The playbook opens, displaying a step-by-step interface to review the extracted obligations.

4.  In the playbook, under the AI extracted obligations section, navigate to the **Review obligations** step.

5.  Select **Review**.

    The extracted obligations are displayed on a new tab.

6.  Select an obligation to review the obligation details.

    -   The **Details** tab displays the extracted obligation details. Use this tab to edit, approve, or reject the obligation.
    -   The **Activity** tab displays a log of key attributes identified during the extraction process. Use this tab to review how the AI agent detected and populated the obligation, including the original text snippets and metadata extracted from the contract. The **Activity** tab helps you validate the extraction accuracy and provides transparency into the decision-making process for each obligation.
7.  On the **Details** tab, perform the required action.

    -   Edit the obligation details as needed.

        **Note:** Complete all required fields before saving the changes or approving the obligation.

        For a description of the field values, see Obligation form.

    -   To save the changes, select **Save**.
    -   To approve the extracted obligation and add it as a record in the contract repository, select **Approve**.
    -   To reject the extracted obligation, select **Reject**.

        After an obligation is rejected, it’s deactivated and can’t be reactivated again. To add an obligation later, you must create an obligation record manually. For more information, see [Create an obligation record in the Software Asset Workspace](../../software-asset-management2/task/create-obligation-record-sam.md).

8.  Repeat step 7 for all the extracted obligations.

9.  Select the **Playbook** tab.

10. Select **Mark as completed**


## Result

Approved obligations are available as records in the **Obligations** tab of the contract repository. Rejected obligations are deactivated and excluded from further processing.

If the schedule of the obligation is recurring, the obligation tasks are automatically created based on the interval specified in the **Repeats** field.

If the schedule of the obligation is adhoc, you must create obligation tasks manually. For more information, see [Create an obligation record in the Software Asset Workspace](../../software-asset-management2/task/create-obligation-record-sam.md).

**Parent Topic:**[Use manage contract repository agentic workflow in the Software Asset Workspace](../concept/manage-contract-repository-workflow.md)

