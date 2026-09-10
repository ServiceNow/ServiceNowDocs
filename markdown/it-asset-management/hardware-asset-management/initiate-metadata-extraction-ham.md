---
title: Initiate metadata and obligation extraction from a signed contract in the Hardware Asset Workspace
description: Reduce manual effort by using the Manage contract repository agentic workflow to extract key metadata and obligations from an uploaded signed contract and calculate the contract reminder date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/initiate-metadata-extraction-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 2
breadcrumb: [Manage contract repository agentic workflow, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Initiate metadata and obligation extraction from a signed contract in the Hardware Asset Workspace

Reduce manual effort by using the Manage contract repository agentic workflow to extract key metadata and obligations from an uploaded signed contract and calculate the contract reminder date.

## Before you begin

For the **Initiate contract extraction** button to appear on the contract form, the following conditions must be met:

-   The Contract metadata extraction skill or the Contract obligation extraction skill is activated on your ServiceNow instance.
-   One or both extraction skills have not yet been executed on the contract record.
-   The contract type is warranty, maintenance, lease, or purchase.

Role required: contract\_manager, sn\_cm\_gen\_ai.ai\_contract\_fulfiller, and now\_assist\_panel\_user

## About this task

Use the Manage contract repository agentic workflow to extract metadata and key contractual obligations from signed contracts. After extraction, the information is mapped to the appropriate fields in the hardware contract record. Review the accuracy of the extracted information and make necessary corrections to the extracted field values as required.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Contract management**.

2.  Select **New contract**.

3.  On the Create New Contract form, fill in the required **Contract model** and **Contract number** field values.

    For a description of the field values, see [Create a contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/t_CreateAContract.md).

4.  Select **Save**.

    The **Initiate contract extraction** button is displayed.

5.  Select the Attachments icon \[Omitted image "extract-contract-metadat-attachment-icon.png"\] Alt text:.

6.  In the Attachments section, select **Select Files**.

7.  Select the signed contract file.

8.  In the Upload a file dialog box, select **Upload**.

    The uploaded file is displayed in the Attachments section.

9.  Select **Initiate contract extraction** and select one of these options in the confirmation message:

    -   To mark your confirmation and proceed with metadata extraction from signed contract, select **OK**.
    -   To dismiss the metadata extraction from signed contract, select **Cancel**.
    After you confirm and proceed with metadata extraction, a confirmation message appears indicating metadata extraction initiated for the signed contract.


## Result

After metadata extraction is completed, a confirmation message appears on the contract form and the **Playbook** tab is displayed.

## What to do next

Review the extracted metadata, contract reminder date, and obligation records. For more information, see [Review AI-extracted metadata and contract reminder date in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/review-ai-extracted-metadata-ham.md) and [Review AI-extracted obligations in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/review-extracted-obligation-ham.md).

**Parent Topic:**[Manage contract repository agentic workflow in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/manage-contract-repo-agent-flow-ham.md)

