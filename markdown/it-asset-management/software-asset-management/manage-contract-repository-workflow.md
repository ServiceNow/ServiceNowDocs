---
title: Use manage contract repository agentic workflow in the Software Asset Workspace
description: Use the manage contract repository agentic workflow to improve productivity by extracting metadata and obligations automatically from signed contracts. Set the contract reminder dates for contract renewal or termination.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [manage contract repository workflow in the Software Asset Workspace, Initiate contract extraction]
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Use manage contract repository agentic workflow in the Software Asset Workspace

Use the manage contract repository agentic workflow to improve productivity by extracting metadata and obligations automatically from signed contracts. Set the contract reminder dates for contract renewal or termination.

## Manage contract repository overview

The manage contract repository agentic workflow uses an AI agent to do the following sequentially.

-   Extract metadata from signed contracts.
-   Calculate the contract reminder date for renewal and termination.
-   Extract obligations from signed contracts.

## Metadata, contract reminders and obligation extraction

The AI agent uses the Now Assist contract metadata extraction skill to extract key metadata from signed contracts. After the metadata extraction is complete, you can open the playbook to review the extracted information and set the contract reminder date. The AI agent uses the Now Assist obligation extraction skill to extract key contractual obligations from contracts. After obligations are extracted, you can review the obligations within the contract playbook and choose to accept or reject them. Accepted obligations are added as records in the **Obligations** tab of the contract record.

The following workflow explains the metadata extraction and contract reminder setup process.

1.  As a Contract Admin with the AI role \(sn\_cm\_gen\_ai.ai\_contract\_config\), activate the contract metadata extraction skill and the contract obligation extraction skill in the Now Assist Admin console.

    For more information, see [Configure the manage contract repository agentic workflow for Software Asset Management](../task/configure-manage-contract-repository-agentic-workflow.md).

2.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Contracts** &gt; **Software contracts** and select **New**.
3.  On the Create New Contract form, fill in the required **Contract model** and **Contract number** fields.
4.  Save the contract record.
5.  Upload a signed contract file and select the **Initiate contract extraction** button.
6.  After the contract metadata, reminders extraction and obligation extraction is complete, the Contract Manager with the AI role \(sn\_cm\_gen\_ai.ai\_contract\_fulfiller and sn\_cm\_obligation.obligation\_fulfiller\) receives a notification indicating that the metadata is ready for review.After contract metadata, reminders extraction, and obligation extraction complete, the Contract Manager with the AI role \(sn\_cm\_gen\_ai.ai\_contract\_fulfiller and sn\_cm\_obligation.obligation\_fulfiller\) receives a notification that the metadata is ready for review.
7.  Refresh the web page to view the **Playbook** tab. The extracted metadata, reminders, and obligation records appear on the **Playbook** tab for review.
8.  The Contract Manager reviews the extracted metadata and submits it to update the contract record.
9.  The contract reminder date is then calculated based on the following factors:
    -   Contract end date
    -   Presence of auto-renewal clause
    -   Notice period for contract renewal or termination

        **Note:** If the renewal notice period and termination notice period aren’t available, it uses the configured default notice period. For more information, see [Set the default notice period for the Manage contract repository agentic workflow](https://www.servicenow.com/docs/access?context=conf-sys-prop-default-np&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

10. The Contract Manager sets the contract reminders in the playbook by reviewing the calculated date and configuring the recipient list for the reminders.

    For more information about reviewing extracted metadata and contract reminders, see [Review AI-extracted metadata and contract reminder date in the Software Asset Workspace](../task/work-with-extracted-contract-metadata.md).

11. The Contract Manager reviews the extracted obligations within the contract playbook. Each obligation can be accepted or rejected based on relevance.The Contract Manager reviews extracted obligations within the contract playbook. Each obligation can be accepted or rejected based on relevance.
12. Approved obligations are automatically added as obligation records in the **Obligations** tab of the contract record.
13. Obligation tasks are created.
    -   For a recurring schedule, the obligation tasks are automatically created for the obligation record based on the defined schedule.
    -   For an ad hoc schedule, the contract manager creates an obligation task from the **Obligation tasks** tab in the contract record.
14. The assigned user is notified when the obligation task is created.
15. The assigned user works on the obligation task and submits it for review.

    The state of the obligation task changes from Open to Awaiting approval.

16. The Obligation Fulfiller reviews the task and approves or rejects it.
    -   If the obligation task is rejected, the state of the task changes to Open, and the assigned user continues to work on it.
    -   If the obligation task is approved, the state of the task changes to Completed.

For more information reviewing extracted obligations, see [Review AI-extracted obligations Software Asset Workspace](../task/review-extracted-obligations.md).

## Conditions for initiating extraction from the contract file

When a software contract is created, the **Initiate contract extraction** button appears on the contract form when the following conditions are met:

-   One of the following Now Assist skills are activated on your ServiceNow instance:
    -   Contract metadata extraction
    -   Contract obligation extraction
-   At least one of these two extraction skills hasn’t yet been executed on the contract record.

    **Note:** If both contract metadata and obligation extraction skills have already been executed on the contract record, the **Initiate contract extraction** button doesn't appear on the contract form.


## AI agents used in the manage contract repository agentic workflow

<table id="table_rpx_swm_v2c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract Repository AI agent

</td><td>

Uses various tools to perform the following:-   Retrieves the contract repository details, such as contract vendor, contract model, contract document's attachment ID, and so on from a specific contract repository record.
-   Extracts metadata from signed contact documents based on the applicable use case in the contract metadata extraction skill.
-   Extracts obligations from signed contact documents based on the applicable use case in the contract obligation extraction skill.
-   Calculates the average lead time for similar contracts.

</td></tr></tbody>
</table>-   **[Configure the manage contract repository agentic workflow for Software Asset Management](../task/configure-manage-contract-repository-agentic-workflow.md)**  
Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use the manage contract repository agentic workflow.
-   **[Initiate metadata and obligation extraction from a signed contract in the Software Asset Workspace](../task/extract-metadata-from-uploaded-contract-document.md)**  
Reduce manual effort by leveraging the Manage contract repository agentic workflow to extract key metadata and obligations from an uploaded signed contract, and calculate the contract reminder date.
-   **[Review AI-extracted metadata and contract reminder date in the Software Asset Workspace](../task/work-with-extracted-contract-metadata.md)**  
Use the contract playbook to review and update the AI-extracted metadata and contract reminder date.
-   **[Review AI-extracted obligations Software Asset Workspace](../task/review-extracted-obligations.md)**  
Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents. Approved obligations are added as obligations records in the **Obligations** tab of the contract repository.

**Parent Topic:**[Using Software Asset Workspace](../../software-asset-management2/concept/using-sam-workspace.md)

