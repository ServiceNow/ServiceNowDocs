---
title: Initiate metadata and obligation extraction from a signed contract in the Software Asset Workspace
description: Reduce manual effort by leveraging the Manage contract repository agentic workflow to extract key metadata and obligations from an uploaded signed contract, and calculate the contract reminder date.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [contract metadata and obligation extraction in SAM workspace, Initiate contract extraction, initiate contract metadata extraction in SAM workspace, initiate obligation extraction in SAM workspace]
breadcrumb: [Use manage contract repository agentic workflow, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Initiate metadata and obligation extraction from a signed contract in the Software Asset Workspace

Reduce manual effort by leveraging the Manage contract repository agentic workflow to extract key metadata and obligations from an uploaded signed contract, and calculate the contract reminder date.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller, sam\_admin/sam\_user, sn\_cm\_gen\_ai.ai\_contract\_config, and now\_assist\_panel\_user

## About this task

Use the Manage contract repository agentic workflow to extract metadata and key contractual obligations from signed contracts. After extraction, the information is mapped to the appropriate fields in the software contract record. Review the accuracy of the extracted information and make necessary corrections to the extracted field values as required.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Contracts** &gt; **Software contracts**.

2.  Select **New**.

3.  On the Create New Contract form, fill in the required **Contract model** and **Contract number** field values.

    For a description of the field values, see [Create a contract](../../contract-management/task/t_CreateAContract.md).

4.  Select **Save**.

    After saving the software contract, the **Initiate contract extraction** button is displayed.

5.  Select the Attachments icon ![](../image/extract-contract-metadat-attachment-icon.png).

6.  In the Attachments section, select **Select Files**.

7.  Select the signed contract file.

8.  In the Upload a file dialog box, select **Upload**.

    The uploaded file is displayed in the Attachments section.

9.  Select **Initiate contract extraction** and select one of these options in the confirmation message:

    -   To mark your confirmation and proceed with metadata extraction from signed contract, select **OK**.
    -   To dismiss the metadata extraction from signed contract, select **Cancel**.
    After you confirm and proceed with metadata extraction, a confirmation message appears indicating metadata extraction initiated for the signed contract.

    After metadata extraction is completed, a confirmation message appears on the contract form and **Playbook** tab is displayed.


## Result

After metadata extraction is completed, a confirmation message appears on the contract form and **Playbook** tab is displayed.

## What to do next

Review the extracted metadata, contract reminder date, and obligations record.

**Parent Topic:**[Use manage contract repository agentic workflow in the Software Asset Workspace](../concept/manage-contract-repository-workflow.md)

**Related topics**  


[Review AI-extracted metadata and contract reminder date in the Software Asset Workspace](work-with-extracted-contract-metadata.md)

[Review AI-extracted obligations Software Asset Workspace](review-extracted-obligations.md)

[Create a contract](../../contract-management/task/t_CreateAContract.md)

