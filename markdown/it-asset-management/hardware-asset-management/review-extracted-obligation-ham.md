---
title: Review AI-extracted obligations in the Hardware Asset Workspace
description: Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/review-extracted-obligation-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 2
breadcrumb: [Manage contract repository agentic workflow, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Review AI-extracted obligations in the Hardware Asset Workspace

Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents.

## Before you begin

Role required: admin

## About this task

The Manage contract repository agentic workflow uses AI agents to extract key contractual obligations from signed contracts. The obligations are extracted based on the applicable use case in the Contract obligation extraction AI skill. After obligation extraction is complete, a message appears on the contract record and an email notification is sent with a link to review the extracted obligations. The playbook provides a step-by-step interface where you can review each obligation, make necessary edits, and decide whether to approve or reject it. Approved obligations are added as actionable records in the **Obligations** tab of the of the contract record.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Contract management**.

2.  Select the **All contracts** tab.

3.  Select a contract record for which you want to review the extracted obligation record.

4.  Select the **Playbook** tab.

    The playbook opens, displaying a step-by-step interface to review the extracted obligations.

5.  In the playbook, under the AI extracted obligations section, expand **Review extracted obligations**.

6.  Select **Review obligations**.

7.  On the Review obligations page, select **Review**.

    The extracted obligations are displayed on a new tab.

8.  Select an obligation to review the obligation details.

    -   The **Details** tab displays the extracted obligation details. Use this tab to edit, approve, or reject the obligation.
    -   The **Activity** tab displays a log of key attributes identified during the extraction process. Use this tab to review how the AI agent detected and populated the obligation, including the original text snippets and metadata extracted from the contract. The **Activity** tab helps you validate the extraction accuracy and provides transparency into the decision-making process for each obligation.
9.  On the **Details** tab, perform the required action.

    -   Edit the obligation details as needed.

        **Note:** Complete all required fields before saving the changes or approving the obligation.

        For a description of the field values, see [Obligation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-obligation-form.md).

    -   To save the changes, select **Save**.
    -   To approve the extracted obligation and add it as a record in the contract repository, select **Approve**.
    -   To reject the extracted obligation, select **Reject**.

        After an obligation is rejected, it’s deactivated and can’t be reactivated again. To add an obligation later, you must create an obligation record manually. For more information, see [Create an obligation record in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-obligation-records-ham.md).

10. Repeat step 9 for all the extracted information.

11. Select the **Playbook** tab.

12. Select **Mark as completed**.


## Result

-   Approved obligations are listed under the **Obligations** tab of the contract record.
-   Rejected obligations are deactivated and excluded from further processing.
-   For obligations with recurring schedule, the obligation tasks are automatically created based on the interval specified in the **Repeats** field.

## What to do next

For obligations with an ad hoc schedule, create obligation tasks manually. For more information, see [Create an ad hoc obligation task in Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-obligation-task-ham.md).

**Parent Topic:**[Manage contract repository agentic workflow in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/manage-contract-repo-agent-flow-ham.md)

