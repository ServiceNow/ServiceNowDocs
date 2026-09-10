---
title: Manage contract repository agentic workflow in the Hardware Asset Workspace
description: Automate contract management with the Manage contract repository agentic workflow. Extract metadata and obligations from signed contracts and set renewal or termination reminders automatically to reduce manual data entry and help legal and procurement teams maintain compliance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/manage-contract-repo-agent-flow-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 11
breadcrumb: [Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Manage contract repository agentic workflow in the Hardware Asset Workspace

Automate contract management with the Manage contract repository agentic workflow. Extract metadata and obligations from signed contracts and set renewal or termination reminders automatically to reduce manual data entry and help legal and procurement teams maintain compliance.

**Important:** This feature is available only with Hardware Asset Management Prime SKU, starting from Hardware Asset Management version 16.0.0 and Australia patch 6.

## Overview of Manage contract repository agentic workflow

The manage contract repository agentic workflow uses an AI agent to perform the following steps sequentially:

1.  Extract metadata from signed contracts.
2.  Calculate the contract reminder date for renewal and termination.
3.  Extract obligations from signed contracts.

## Metadata extraction and contract reminders

The AI agent uses the Contract metadata extraction skill to extract key metadata from signed contracts. After the metadata extraction is complete, you can open the playbook to review the extracted information and set the contract reminder date.

The following workflow explains the metadata extraction and contract reminder setup process:

1.  As a Contract admin with the AI role \(sn\_cm\_gen\_ai.ai\_contract\_config\), activate the Contract metadata extraction skill in the AI Admin Hub console.

    For more information, see [Configure the Manage contract repository agentic workflow for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/configure-contract-repo-agentic-workflow-ham.md).

2.  In the Contract management view of the Hardware Asset Workspace, create a contract record.
3.  On the contract record, upload a signed contract file and select **Initiate contract extraction**.
4.  After contract metadata and reminders extraction is complete, a message appears on the contract form indicating that the metadata is ready for review. If notifications are enabled by the administrator, the Contract Manager also receives an email notification. For more information, see [Enable notifications for AI extracted metadata and obligations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-na-me-agentic-ntf.md).
5.  The Contract Manager reviews the extracted metadata and submits it to update the contract.
6.  The contract reminder date is then calculated based on the following factors:

    -   Contract end date
    -   Presence of auto-renewal clause
    -   Notice period for contract renewal or termination
    **Note:** If the renewal notice period and termination notice period aren't available, the configured default notice period is used. For more information, see [Set the default notice period for the Manage contract repository agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/conf-sys-prop-default-np.md).

7.  The Contract Manager sets the contract reminders in the playbook by reviewing the calculated date and configuring the recipient list for the reminders.

For more information, see [Review AI-extracted metadata and contract reminder date in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/review-ai-extracted-metadata-ham.md).

## Obligation extraction

The AI agent uses the Contract obligation extraction skill to extract key contractual obligations from contracts. Once extracted, you can review the obligations within the contract playbook and choose to accept or reject them. Accepted obligations are added as records in the **Obligations** tab of the contract record.

The following workflow explains the obligation extraction process:

1.  As a Contract admin with the AI role \(sn\_cm\_gen\_ai.ai\_contract\_config\), activate the contract obligation extraction skill in the AI Admin Hub console.

    For more information, see [Configure the Manage contract repository agentic workflow for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/configure-contract-repo-agentic-workflow-ham.md).

2.  In the Contract management view of the Hardware Asset Workspace, create a contract record.
3.  On the contract record, upload a signed contract file and select **Initiate contract extraction**.
4.  After the obligation extraction is complete, a message appears on the contract form indicating that the obligations are ready for review. If notifications are enabled by the administrator, the Contract Manager also receives an email notification. For more information, see [Enable notifications for AI extracted metadata and obligations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-na-me-agentic-ntf.md).
5.  The Contract Manager reviews the extracted obligations within the contract playbook. Each obligation can be accepted or rejected based on relevance.
6.  Approved obligations are automatically added as obligation records in the **Obligations** tab of the contract record.
7.  Obligation tasks are created.
    -   For a recurring schedule, the obligation tasks are automatically created for the obligation record based on the defined schedule.
    -   For an ad hoc schedule, the user with the sn\_cm\_obligation.obligation\_fulfiller role creates an obligation task. For details, see [Create an ad hoc obligation task in Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-obligation-task-ham.md).
8.  The assigned user with the sn\_cm\_obligation.obligation\_user role is notified when the obligation task is created.
9.  The assigned user works on the obligation task and submits it for review.

    The state of the obligation task changes from Open to Awaiting approval. For more details, see [Create obligations manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-work-on-ob-tasks.md).

10. The user with the sn\_cm\_obligation.obligation\_fulfiller role reviews the task and approves or rejects it. For more information, see [Approve or reject obligation tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-manage-ob-tasks.md).
    -   If the obligation task is rejected, the state of the task changes to Open, and the assigned user continues to work on it.
    -   If the obligation task is approved, the state of the task changes to Completed.

For more information, see [Review AI-extracted obligations in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/review-extracted-obligation-ham.md).

## Conditions for initiating extraction from the contract file

When a hardware contract is created, the **Initiate contract extraction** button appears on the contract form when the following conditions are met:

-   The contract metadata extraction skill or the Contract obligation extraction skill is activated on your ServiceNow instance.
-   One or both extraction skills have not yet been executed on the contract record.
-   The contract type is warranty, maintenance, lease, or purchase agreements.

**Note:** If both the Contract metadata extraction skill and the Contract obligation extraction skill have already been executed on the contract record, the **Initiate contract extraction** button does not appear on the contract form.

## AI agents used in the manage contract repository agentic workflow

<table id="table_rpx_swm_v2c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract repository AI agent

</td><td>

-   Retrieves contract repository details, such as vendor, model, and document attachment ID, from a specific contract repository record.
-   Extracts metadata from signed contract documents based on the applicable use case in the contract metadata extraction skill.
-   Extracts obligations from signed contract documents based on the applicable use case in the contract obligation extraction skill.
-   Calculates the average lead time for similar contracts.

</td></tr></tbody>
</table>-   **[Initiate metadata and obligation extraction from a signed contract in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/initiate-metadata-extraction-ham.md)**  
Reduce manual effort by using the Manage contract repository agentic workflow to extract key metadata and obligations from an uploaded signed contract and calculate the contract reminder date.
-   **[Review AI-extracted metadata and contract reminder date in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/review-ai-extracted-metadata-ham.md)**  
Use the contract playbook to review and update the AI-extracted metadata and contract reminder date.
-   **[Review AI-extracted obligations in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/review-extracted-obligation-ham.md)**  
Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents.

**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Analyze hardware assets using the Generate hardware asset insights generative AI skill]()

[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Manage obligations in the Hardware Asset Workspace]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

[Hardware Asset Management integration with Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/ham-cm-pro-integration.md)

