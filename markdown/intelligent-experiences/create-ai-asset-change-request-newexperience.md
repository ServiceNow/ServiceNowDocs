---
title: Create change requests for AI assets
description: Create a change request to modify the relationships between a deployed AI asset and its related assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-ai-asset-change-request-newexperience.html
release: zurich
topic_type: task
last_updated: "2026-04-16"
reading_time_minutes: 4
breadcrumb: [Managing your AI asset lifecycle, Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Create change requests for AI assets

Create a change request to modify the relationships between a deployed AI asset and its related assets.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] or AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can create change requests only for the AI assets that they are assigned to manage. In addition, they can only create change requests and submit them for review. They can't approve or reject requests or complete any corresponding change tasks.

## About this task

To modify the relationships between related AI assets, you can initiate the change process by creating and submitting a change request.

You can create change requests for the following AI asset types:

-   AI systems \(classic, generative, and agentic\)
-   AI models
-   Datasets

## Procedure

1.  Navigate to **All** &gt; **Al Control Tower** &gt; **Home** &gt; **Inventory**.

2.  From the list of available assets, open an asset record with a state of **Deployed** and a status of **Approved**.

3.  Initiate the change request by using one of the following navigation options.

    -   Open the asset record and select the **Actions** menu and select **Create change request**.
    -   In the Lifecycle tab, go to the Maintain sub tab and select **Create change request.**
4.  On the Change request form, fill in the fields.

<table id="table_vlt_rkm_y3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Change details

</td></tr><tr><td>

Asset in review

</td><td>

The AI Asset that you want to modify related asset relationships for.**Note:** If you initiated the change request from an AI asset record, this field populates automatically.

</td></tr><tr><td>

Asset type

</td><td>

Type of asset.

</td></tr><tr><td>

Version

</td><td>

Updated version number of the AI asset.

</td></tr><tr><td>

Due date

</td><td>

Date and time at which the request must be completed.

</td></tr><tr><td>

Justification

</td><td>

Justification for creating the request.

</td></tr><tr><td>

Attachments

</td><td>

Accepts JPG, PDF, or XLSX files up to a maximum of 10 MB.

</td></tr><tr><td colspan="2">

Sub AI systems**Note:** This form section appears only if you are creating a change request for an AI system with an Asset type of either Generative AI or Agentic AI.

</td></tr><tr><td>

Updated Sub AI systems

</td><td>

Related AI components or subsystems that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

AI models**Note:** This form section appears only if you are creating a change request for an AI system.

</td></tr><tr><td>

Updated models

</td><td>

Related AI models that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

AI prompts**Note:** This form section appears only if you are creating a change request for an AI system.

</td></tr><tr><td>

Updated prompts

</td><td>

Related prompts that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Evaluation dataset**Note:** This form section appears only if you are creating a change request for an AI system or AI model.

</td></tr><tr><td>

Updated evaluation datasets

</td><td>

Related evaluation datasets that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Tools**Note:** This form section appears only if you are creating a change request for an agentic AI system.

</td></tr><tr><td>

Updated tools

</td><td>

Related tools that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Training datasets**Note:** This form section appears only if you are creating a change request for an AI model.

</td></tr><tr><td>

Updated training datasets

</td><td>

Related training datasets that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Source**Note:** This form section appears only if you are creating a change request for a dataset.

</td></tr><tr><td>

Updated source

</td><td>

Related data source that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Base datasets**Note:** This form section appears only if you are creating a change request for a dataset.

</td></tr><tr><td>

Updated base datasets

</td><td>

Related base dataset that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Dataset card**Note:** This form section appears only if you are creating a change request for a dataset.

</td></tr><tr><td>

Updated dataset card

</td><td>

Related dataset card that you want to associate the AI asset with.

</td></tr></tbody>
</table>5.  Select **Save**, the **Actions** menu, and then select **Submit for review**.

6.  In the Submit change request dialog box, select **Submit request**.

    The Impacted assets and Change tasks related list appear. You can approve or reject the request.

7.  On the **Details** tab, set the **Assigned to** field to the user who you want to assign the change request to.

    You can assign the request to yourself or to any other user with the AI steward \[sn\_ai\_governance\_ai\_steward\] role.

8.  Approve or reject the request.

    -   To approve the request, select **Approve**.
    -   To reject the request, select **Reject**.
    -   If you approved the request, the Status changes to **Approved** and the State changes to **In progress** \(if there are impacted assets\) or **Completed** \(if there are no impacted assets\). The new AI asset is created.

        The AI Control Tower application then generates a change task for each asset that is impacted by the request except for datasets. These change tasks appear on the **Change tasks** tab and specify the actions that must be taken on the impacted assets. Each change task is assigned to a user with the AI steward \[sn\_ai\_governance\_ai\_steward\] role. If you have any concerns or need further clarification on the request, you can create additional change tasks manually only if you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role. After the assigned users complete all change tasks, the AI Control Tower application automatically creates a new AI asset record for the asset that the change request was created for. The State of the request then changes to Completed.

        **Note:** The **Impacted assets** tab is not available if the change request was created for a dataset.

    -   If you rejected the request, the Status changes to Rejected and the State changes to Completed.

**Parent Topic:**[Managing your AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/manage-lifecycle-newexperience.md)

